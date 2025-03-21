# Compartir una carpeta al grup de treball des de Linux

Ja hem vist com compartir una carpeta des de Windows al grup de treball, però ara ho farem des d'un ordinador amb Linux instal·lat.

## Pas 1.- Crear una carpeta per compartir

Com exemple a la carpeta personal de l'usuari de Linux creem una carpeta anomenada "documents_de_grup".

**Li canvieu els permisos a la carpeta a 777 (Tothom té accés).**

![image](https://github.com/XaSaFa/MP04/assets/110727546/c88e5b35-de99-4c26-8d77-0e2b8e9c73ed)

## Pas 2.- Instal·lar i Configurar SAMBA

Per instal·lar SAMBA escriurem la següent comanda:

```
sudo apt install samba
```

Per compartir la carpeta hem de modificar el fitxer de SAMBA  ```/etc/samba/smb.cnf```.

Canviarem el nom del grup de treball que està per defecte a "WORKGROUP" per el que necessitem, en aquest exemple "SMX2"

![image](https://github.com/XaSaFa/MP04/assets/110727546/12a01b97-49f1-495f-87a5-7b2477b31d71)

![image](https://github.com/XaSaFa/MP04/assets/110727546/9f686a5e-a2e1-4cb1-9df2-08c5ab380604)

Sense sortir del fitxer anem a la part inferior i creem un text que defineix el nostre recurs compartit.

![image](https://github.com/XaSaFa/MP04/assets/110727546/89e6f47e-0618-4d67-91bb-035fa5792729)

Aquest text significa:

- [doc_grup] -> Nom del recurs compartit.
- path -> Ruta al recurs que compartim.
- guest ok = no -> No admetre usuaris no identificats.
- writeable = yes -> Els ususaris poden modificar els continguts.
- write list = xavi -> Usuaris que poden modificar (en aquest cas l'usuari xavi).
- browseable = yes -> El recurs té permís de lectura.
- create mask = 0775 -> Permisos dels fitxers que es crein dins la carpeta compartida.
- force create mode = 0775 -> Necessari per a que funcioni create mask.
- directory mask = 0755 -> Permisos de les carpetes que es crein dins la carpeta compartida.

## Pas 3.- Afegir usuari de SAMBA

Al fitxer de configuració hem dit que l'usuari xavi pot accedir als continguts de la carpeta, tot i que xavi és un usuari local hem d'afegirlo com usuari de SAMBA.

**IMPORTANT:** Només podem afegir a SAMBA a usuaris que ja existeixen.

Farem servir la instrucció ```smbpasswd```.

![image](https://github.com/XaSaFa/MP04/assets/110727546/83de6b2c-2d9b-4f96-9a4e-ae2a82caabef)

## Pas 4.- Reiniciar el servei SAMBA

Reiniciem el servei smbd.

![image](https://github.com/XaSaFa/MP04/assets/110727546/b440be51-bbf0-4010-91ac-511b4a786d66)

## Pas 5.- Afegim algun fitxer a la carpeta

A Linux afegim un fitxer dins la carpeta compartida.

![image](https://github.com/XaSaFa/MP04/assets/110727546/c9a84a30-e781-4812-8392-b1e74c4d4c62)

