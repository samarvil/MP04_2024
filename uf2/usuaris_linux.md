# Crear usuaris a Linux

A Linux per crear un usuari podem utilitzar la comanda useradd o adduser.

## useradd

![image](https://github.com/XaSaFa/MP04/assets/110727546/68828220-b603-4e0e-9ab5-5a9fb53a176e)

## Afegir usuari amb useradd

És una comanda nativa de Linux que serveix per afegir usuaris al sistema.

![image](https://github.com/XaSaFa/MP04/assets/110727546/b1711172-ff7e-4e60-96f8-8fcbea317cfd)

La comanda crea un usuari anomenat manolo i un grup anomenat manolo.

![image](https://github.com/XaSaFa/MP04/assets/110727546/c3e07684-9f40-44b5-86cc-881daaa29880)

Però no crea un directori personal a home, per a fer-ho hem d'afegir el paràmetre m.

![image](https://github.com/XaSaFa/MP04/assets/110727546/e46712da-9cdb-4de2-9a68-b3138505e23b)

![image](https://github.com/XaSaFa/MP04/assets/110727546/8e930959-ce5d-4aa7-a29c-8f03d223aab8)

## Afegir usuari amb caducitat

Podem fer que un usuari es crei però que expiri el seu compte en una data concreta afegint el paràmetre -e i la data en que volem que expiri l'usuari.

![image](https://github.com/XaSaFa/MP04/assets/110727546/8ba98e7d-d791-4785-b978-f07ace76a8d7)

## Canviar la contrasenya a un usuari amb passwd

Per canviar el password o afegir password a un usuari utilitzem la comanda passwd.

![image](https://github.com/XaSaFa/MP04/assets/110727546/4c0235b4-f3da-4302-8b3b-c5370925a550)

## Eliminar usuari amb userdel

La comanda esborra l'usuari.

![image](https://github.com/XaSaFa/MP04/assets/110727546/d76a2882-eb5b-4cf8-a8e7-ef3c7baff3a1)

## adduser

adduser és un script de Linux que crea un usuari, li crea un directori a home i ens pregunta la contrasenya.

![image](https://github.com/XaSaFa/MP04/assets/110727546/e0bce68a-70b2-4a78-9d3d-ff7f5395e6a0)

# Canviar un nom d'usuari de Linux

Podem canviar el nom d'un usuari de Linux, però a Linux hi ha altres aspectes a més del nom d'usuari i la contrasenya que hem de tenir en compte:

- El grup de l'usuari.
- El directori home de l'usuari.

![image](https://github.com/XaSaFa/MP04/assets/110727546/39896bc1-004d-4016-885d-4b27520d8663)

Si volem canviar del tot un nom d'usuari per un altre farem:

1. Canviar el nom d'usuari.
![image](https://github.com/XaSaFa/MP04/assets/110727546/2e31dcd6-3b34-458e-b745-8f3984699f1a)
2. Canviar el directori home de l'usuari.
![image](https://github.com/XaSaFa/MP04/assets/110727546/74a448a3-d5fe-4a85-ad65-1cf05ca42687)
![image](https://github.com/XaSaFa/MP04/assets/110727546/9687ad05-f821-4edf-8f51-40314f37749c)
3. Canviem el grup.
![image](https://github.com/XaSaFa/MP04/assets/110727546/c8a986b0-ce9d-4f3c-87ab-ad81dca5986e)
