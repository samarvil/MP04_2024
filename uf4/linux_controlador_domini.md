# Utilitzar un servidor Linux com controlador de domini.

## Pas 1.- Preparar el servidor

Quan un equip amb Windows server actúa de controlador de domini Active Directory es configura el rol AD de forma automàtica, en canvi a Linux hem d'instal·lar una serie de programes de forma manual:

- Samba: Necessitarem Samba amb versió 4 com a mínim.
- DNS: permet obtenir informació sobre els objectes del domini a partir del seu nom dins del domini (per exemple, l'adreça IP d'una màquina a partir del seu nom). En un cas senzill com el nostre, el mateix Samba farà de servidor DNS.
- Servei Kerberos: és un protocol d'autenticació entre ordinadors d'una xarxa perquè tant el client com el servidor puguin comprovar de forma fiable la identitat de l'altre.

## Pas 1.1.- Actualitzem els repositoris

```
sudo apt update
```

## Pas 1.1.- Canviem el nom al servidor

Canviem el nom del controlador de domini a AKIRA
```
sudo hostnamectl set-hostname AKIRA
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/6226bf83-5113-48b5-9f41-ab356b58468a)

També modifiquem el nom del servidor al fitxer /etc/hosts editant-lo.

![image](https://github.com/XaSaFa/MP04/assets/110727546/9ba93fc8-1174-4fef-898d-77126a3b89e4)

També afegirem el nom AKIRA.neotokyo.local ja que el domini serà NEOTOKYO.LOCAL.

![image](https://github.com/XaSaFa/MP04/assets/110727546/d25f7db2-1c08-454b-926b-d379403a5f75)

## Pas 1.2.- Configurar IP fixa al servidor

El servidor tindrà IP fixa.

![image](https://github.com/XaSaFa/MP04/assets/110727546/19ca95be-ef4d-4417-ba95-646fde7e2758)

![image](https://github.com/XaSaFa/MP04/assets/110727546/2846e5ec-d5f9-42d5-874d-06fda673c5c5)

## Pas 1.3.- Instal·lar software

Instal·larem una serie de paquets.

```
sudo apt install samba krb5-config winbind smbclient
```

La instal·lació de Kerberos ens demanarà informació, primer el regne:

![image](https://github.com/XaSaFa/MP04/assets/110727546/2132ac2d-e194-4f8e-aef8-d5b5e602098e)

Després els servidors del regne:

![image](https://github.com/XaSaFa/MP04/assets/110727546/c777817d-1f9a-4f77-bc8e-cdf2c9ede126)

Després el nom del servidor administratiu del regne, que és el mateix:

![image](https://github.com/XaSaFa/MP04/assets/110727546/9ccef6d5-d604-4d53-a0ae-056c0322be83)

## Pas 1.4 Fer una còpia de seguretat del fitxer de configuració de SAMBA

Esborrarem la configuració de Samba i guardarem el fitxer de configuració per si alguna cosa falla.

```
sudo mv /etc/samba/smb.conf /etc/samba/smb.conf.OLD
```

## Pas 1.5 Promoure el servidor a controlador de domini

```
sudo samba-tool domain provision
```

El programa ens pregunta la informació necessària i ens ofereix els valors per defecte que seran els que utilitzarem:

![image](https://github.com/XaSaFa/MP04/assets/110727546/698b6ba2-ff8d-49f2-9688-a8077bfe9e4e)

També ens demana una contrasenya robusta.

La configuració crea un fitxer per a Kerberos:

![image](https://github.com/XaSaFa/MP04/assets/110727546/c6c925fc-3bef-42d3-bf29-12b26c23a284)

El qual copiem a /etc.

```
sudo cp /var/lib/samba/private/krb5.conf /etc/
```

## Pas 1.6.- Configurar el servei samba-ad-dc

Parem els serveis següents:

```
sudo systemctl stop smbd nmbd winbind systemd-resolved
```

I els deshabilitem:

```
sudo systemctl disable smbd nmbd winbind systemd-resolved
```

Ens assegurem de que es podrà executar samba-ad-dc.

```
sudo systemctl unmask samba-ad-dc
```

Eliminem el fitxer resolv.conf.

```
sudo rm /etc/resolv.conf
```

I el tornem a crear amb les dades del nostre domini:

```
sudo nano /etc/resolv.conf
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/91813fdc-065e-442a-8481-7d898a47fcaa)

Reiniciem i habilitem samba-ad-dc:

```
sudo systemctl start samba-ad-dc
```

```
sudo systemctl enable samba-ad-dc
```

## Pas 1.7.- Comprovar el nivell del controlador de domini

```
sudo samba-tool domain level show
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/57d1556a-3d63-47b6-925d-ab9cff0bbf33)

Hem de comprovar que tenim nivell de controlador de domini, en aquest cas nivell Windows 2008 R2.

## Pas 1.8 Crear un usuari de domini

Crearem un usuari del domini anomenat kaneda.

```
sudo samba-tool user create kaneda
```

Reiniciem l'equip.

[Aquí teniu més opcions de la comanda samba-tool.](https://samba.tranquil.it/doc/en/samba_config_server/samba_commands_utils.html)

![image](https://github.com/XaSaFa/MP04/assets/110727546/0676ce45-18f1-422b-8dd6-4c27e4873d43)

## Pas 1.9 Comprovar que el servei de DNS de Samba funciona correctament:

Comprovem el servei LDAP sobre TCP:

```
host -t SRV _ldap._tcp.NEOTOKYO.LOCAL
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/12c0ff37-3d16-4bbf-9754-a5b6818997be)

Comprovem el servei Kerberos sobre UDP:

```
host -t SRV _kerberos._udp.NEOTOKYO.LOCAL
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/12bd300d-281d-4c4f-aeca-20f8089a295c)

Comprovem que el nom del server es resol correctament.

```
host -t A AKIRA.NEOTOKYO.LOCAL
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/f9139d6d-b339-4a47-9fa2-b648116bde66)

## Pas 1.10 Comprovar el funcionament de Kerberos

Comprovem l'accés a serveis que té l'usuari administrador (utilitzant la contrasenya d'instal·lació de controlador de domini).

```
sudo smbclient -L AKIRA.NEOTOKYO.LOCAL -U 'administrator'
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/8bc22b07-002a-492b-8177-14ada38dcc80)



