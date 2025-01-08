# Passos

## 1.- Nom del servidor

Primer canviem el nom de la màquina:

```
sudo hostnamectl set-hostname ldapserver.dungeonofbits.com
```

Després afegim a /etc/hosts les modificacions necessàries:

```
sudo nano /etc/hosts
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/cbd1e4a7-d52e-4572-8c75-50e8007f7108)

## 2.- Actualitzem software

Actualitzarem els repositoris de software de l'equip amb la comanda següent:

```
sudo apt update
```

## 3.- Instal·la slapd i ldap-utils

Instal·lem el software necessari amb la comanda:

```
sudo apt install slapd ldap-utils
```

Ens demanarà la contrasenya d'administrador:

![image](https://github.com/XaSaFa/MP04/assets/110727546/43c0e5f4-29ef-4e99-9dc8-904cf3da978f)

## 4.- Configuració:

Introduïm la comanda:

```
sudo dpkg-reconfigure slapd
```

Ens preguntarà si volem ometre la configuració del servidor LDAP, diem que **NO**.

![image](https://github.com/XaSaFa/MP04/assets/110727546/560e6421-9af4-4ace-b1de-9d4754554800)

Escollim el nom del domini:

![image](https://github.com/XaSaFa/MP04/assets/110727546/2e7e3d28-6f98-416e-bdf5-c0584e8afe77)

I el nom de l'empresa que fa la instal·lació:

![image](https://github.com/XaSaFa/MP04/assets/110727546/ed981f1e-dc86-4cfd-bcf2-2e7e17d3b87a)

Introduim i confirmem una contrasenya:

![image](https://github.com/XaSaFa/MP04/assets/110727546/dfc7f9a3-03d5-4511-b2d1-7a13d9737c92)

Confirmem que volem que s'esborri la BBDD quan eliminem LDAP:

![image](https://github.com/XaSaFa/MP04/assets/110727546/566fd759-9d4b-42db-8592-82f293fb7e8f)

Després ens avisa que queden fitxers antics de la BBDD i que si els volem moure, diem que sí:

![image](https://github.com/XaSaFa/MP04/assets/110727546/6ae17e9e-6b29-450b-8742-ca5603155b10)

Ja estaria:

![image](https://github.com/XaSaFa/MP04/assets/110727546/90246437-56e8-459b-8336-1816638e98bc)

## 5.- Comprovem la instal·lació:

Comprovem que s'ha instal·lat bé amb la comanda:

```
sudo slapcat
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/ccff04ec-bd35-44b3-af9a-5ac4dff8dbcf)









