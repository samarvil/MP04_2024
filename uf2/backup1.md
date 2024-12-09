# Crear còpies de seguretat

Una de les coses més importants dels ordinadors és la informació que contenen, per això és important tenir una bona política de còpia de seguretat o backup.

MIREM la [política de còpies de seguretat](https://www.incibe.es/sites/default/files/contenidos/politicas/documentos/copias-seguridad.pdf) de l'INCIBE (Instituto Nacional de Ciberseguridad).

## La regla del 3-2-1

Aquesta norma es recomana per evitar perdre la informació i, sobretot, no tenir aturada l'empresa en cas de problemes.

![image](https://github.com/XaSaFa/MP04/assets/110727546/0e1f8e2d-bd35-4a91-8dd2-17b99c23e908)

Es tracta de fer:

- **3** còpies de seguretat diferents.
- Emmgatazemar totes les còpies a **2** mitjans físics diferents.
- Emmagatzemar totes les còpies a **1** mitjà fora de la pròpia empresa, al núvol per exemple.

Es pot ampliar també així.

![image](https://github.com/XaSaFa/MP04/assets/110727546/b382be3b-6588-4549-9fa9-440d26d0afb3)

- Tenir una còpia a un mitjà immutable (DVDs) o desconnectat de Internet.
- Verificar que les còpies s'han fet correctament.

## Còpies de seguretat per terminal

Hi ha moltes formes de fer còpis de seguretat per terminal, per exemple podem utilitzar la comanda **dump**.

Per veure les opcions de dump executem:

```
man dump
```

## Fer un backup amb dump

Aquesta comanda farà un backup del directori /var/www a un fitxer anomenat backup_web.bak del directori /tmp:

```
dump -0aj -f /tmp/backup_web.bak /var/www
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/6fb232ea-135c-4bbc-9288-0c90327c1b90)

El paràmetre 0 és el nivell, indica que es fa una còpia sencera, un número superior seria una còpia incremental, és a dir: només es copiarien fitxers més nous o modificats des de la última còpia amb un nivell inferior.
El paràmetre a indica que es faci la còpia de seguretat sense comprovar el tamany del destí.
El paràmetre j indica que es comprimiran les dades.
El paràmetre f indica que la còpia es farà a un fitxer i s'ha d'indicar el nom del fitxer.

## Recuperar un backup amb restore

La comanda restore serveix per recuperar un backup, la següent comanda recuperarà la còpia de l'exemple anterior.

```
cd /
sudo restore -xf /tmp/backup_web.bak
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/9f14707a-f185-4438-b769-6d921284771a)

## Altres comandes

Existeixen altres comandes per fer backups com per exemple tar o rsync. També la comanda dd fa còpies però d'unitats senceres.

🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎

**Activitat:**

1. Crea i explica les comandes per fer còpia de seguretat i restaurar el directori /var/www amb la comanda tar.

- sudo tar -czvf /home/xavi/mohaguapo.tar /var/www
- sudo tar -xzvf /home/xavi/mohaguapo.tar -C /
   
4. Crea i explica les comandes per fer còpia de seguretat i restaurar el directori /var/www amb la comanda rsync.

🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎



