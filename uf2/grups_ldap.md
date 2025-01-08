# Crear un grup

El gidNumber dels grups solen començar-se per 10000, així els següents grups hauran de ser 10001, 10002, etc.

## 1.- Editem un fitxer

```
sudo nano grup.ldif
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/24b77833-9528-4bed-898f-dfbc5c93eb3c)

## 2.- Afegim el grup a LDAP

```
sudo ldapadd -x -D cn=admin,dc=dungeonofbits,dc=com -W -f grup.ldif
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/682a3e84-853d-4325-9ae2-a33d04e25757)

## 3.- Comprovem que s'ha introduït

Amb la comanda:

```
sudo slapcat
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/bfd79c61-15e9-458b-a229-6ba507235a8b)
