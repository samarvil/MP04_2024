# Crear un usuari

## 1.- Evitar que la contrasenya de l'usuari es guardi en text pla

Les dades dels usuaris s'introdueixen des de un fitxer de text pla, per tal que la contrasenya no la pugui veure qualsevol utilitzem la comanda **slappasswd**.

Aquesta comanda produeix un hash utilitzant la'lgorisme SHA-1 (es pot canviar l'algorisme utilitzat).

```
sudo slappasswd
```

La comanda ens retorna el codi hash de la contrasenya introduida:

![image](https://github.com/XaSaFa/MP04/assets/110727546/5cc018ba-14a0-4bbd-9432-9e2efef69cbc)

## 2.- Creem el fitxer d'usuari

```
sudo nano usuari.ldif
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/2c34effe-50db-458a-a039-902623085f14)

- La contrasenya a userPassword és la que hem generat anteriorment.
- El gidNumber és el del grup que hem creat abans.
- Els ususaris comencen amb uidNumber a partir del 2000.

## 3.- Afegim l'usuari a la BBDD LDAP

```
sudo ldapadd -x -D cn=admin,dc=dungeonofbits,dc=com -W -f usuari.ldif
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/3ee868d5-c8e7-4adc-9a22-6250f51b33f5)

## 4.- Comprovem

```
sudo slapcat
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/a97eadec-d373-4e78-a45b-299c7b33eb12)

## Observacions:

- uidNumber i homeDirectory ha de tenir valors diferents per a cada usuari.
- gidNumber ha de ser el del grup al que pertany l'usuari.
- Els valors uidNumber i gidNumber no han de coincidir amb els UID i GID dels usuaris i grups locals (els podeu consultar a /etc/passwd i /etc/group  respectivament).

  

