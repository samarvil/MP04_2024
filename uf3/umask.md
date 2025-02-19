# Permisos per defecte a Linux:

A l'exemple següent l'usuari elvis crea un fitxer dins la carpeta:  

![image](https://github.com/XaSaFa/MP04/assets/110727546/6c9d8549-9807-41c1-a7f1-fb62a2d2c2ed)

Però com veieu els permisos del fitxer creat són rw-rw-r--, és a dir: 664.

Això és perquè per defecte els usuaris de Linux creen els fitxers amb permisos 664 i els directoris amb 775.

![image](https://github.com/XaSaFa/MP04/assets/110727546/554cd602-0060-42d8-af26-1fe0cd8bace2)

## umask:

La comanda umask ens permet canviar els permisos per defecte d'un usuari. 

Per consultar els permisos per defecte escrivim: 

```umask```

![image](https://github.com/XaSaFa/MP04/assets/110727546/bae4b1df-98d8-4a27-9c14-02a82660be56)

Per interpretar com funciona la màscara hem de tenir en compte que els valors per defecte són:

- A fitxers: 666 - 002 de la màscara: 664, és a dir rw-rw-r--.
- A directoris: 777 - 002 de la màscara: 775, és a dir rwxrwxr-x.

Si volem canviar el comportament hem de modificar la màscara.

## Modificar el valor per defecte:

Per canviar els valors per defecte hem de modificar la màscara, això es fa calculant el valor final que volem de permisos sobre un fitxer:

### Directori:

Per exemple, si volem un directori amb permisos 410 agafem el valor màxim 777, li restem 410 i obtenim el valor de la màscara:

- Màxim: 777
- Permisos que volem: 410
- Valor de màscara: 777-410 = 367 = 0367 (AFEGIM UN 0 DAVANT)

![image](https://github.com/XaSaFa/MP04/assets/110727546/94acfada-0d0d-42c1-9eff-1548267fab53)

### Fitxer:

**La màscara no ens permet donar permisos d'execució als fitxers**.

Si volem un fitxer amb permisos 644, calculem així:

- Màxim: 666
- Permisos que volem: 644
- Valor de màscara: 666-644 = 022 = 0022 (AFEGIM UN 0 DAVANT)

![image](https://github.com/XaSaFa/MP04/assets/110727546/ad1fd8ae-bbd9-4730-8937-1181079a977c)

Per a donar permisos d'execució a un fitxer utilitzarem chmod.

![image](https://github.com/XaSaFa/MP04/assets/110727546/69862493-5632-449c-94ee-2fa8dadf0a85)
