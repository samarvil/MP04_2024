# Els permisos a Linux

![image](https://github.com/XaSaFa/MP04/assets/110727546/1e655b60-c973-48cf-9640-ab623e8f6067)

A Linux els permisos es refereixen a les capacitats que té un usuari de manipular un fitxer o directori.

Els fitxers i directoris tenen tres tipus de permisos:

- **Lectura**: (r: read) Capacitat de veure els continguts d'un fitxer i copiar-lo.
- **Escriptura**: (w: write) Capacitat de modificar els continguts d'un fitxer o esborrar-lo.
- **Execució**: (x: eXecute) Capacitat d'executar un fitxer si el fitxer és executable.

## Exemple:

![image](https://github.com/XaSaFa/MP04/assets/110727546/29f1f3f8-e179-45a8-bbd3-360432160dc5)

Aquí tenim dues línies de fitxers del sistema operatiu. La primera "vulkan" correspon a un directori i per això la línia comença per d.
Després de la d venen els següents caràcters: **rwx r-x r-x**.
Aquests caràcters van en grups de 3 i representen els permisos de l'usuari propietari, del grup propietari i de altres usuaris respectivament.
Com veiem a la línia hi ha la paraula root que significa que root és el propietari del directori i després la paraula root una altra vegada, que significa que el grup root és propietari del directori.

Si ordenem la informació de la línia tenim:

- Usuari root té permisos rwx (lectura, escriptura i execució).
- Grup root té permisos r-x (lectura i execució només, el guió al mig significa que no té permisos d'escriptura).
- Altres usuaris i grups d'usuaris diferentes de root (lectura i execució només, el guió al mig significa que no té permisos d'escriptura).

Esquema de permisos sobre fitxers:

![image](https://github.com/XaSaFa/MP04/assets/110727546/dfa96ad9-7ce5-400e-b51d-f6674714160a)

## Modificar el propietari i grup propietari d'un directori o fitxer:

Per canviar el propietari i grup propietari d'un directori o fitxer utilitzem la comanda **chown**.

Exemple:

![image](https://github.com/XaSaFa/MP04/assets/110727546/00184931-9bfe-47ca-b1dd-22ab6dec64b0)

Aquí tenim un directori anomenat "cliente" dins la carpeta /var/www/html, aquesta carpeta és propietat de root, però necessitem que un usuari anomenat elvis sigui capaç d'afegir fitxers dins la carpeta.

Amb la comanda chown ho aconseguirem:

```
sudo chown -R elvis:elvis cliente/
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/7d1a53c9-0a0b-48bd-a412-f19f7cd172b3)

IMPORTANT: El paràmetre -R fa que el canvi afecti a tots els elements dins de la carpeta clientes també.

Imaginem que enlloc d'un únic usuari ens interessa que més d'un usuari pugui editar el contingut, llavors enlloc d'un usuari el que farem serà crear un grup d'usuaris i afegir els usuaris editors al grup.

Per exemple farem que elvis sigui un usuari del grup editors.

- Generem el grup editors: ```sudo addgroup editors```.
- Afegim elvis al grup editors: ```sudo addgroup elvis editors```.
- Canviem el propietari de la carpeta clientes a root i el grup propietari a editors: ```sudo chown -R root:editors cliente/```

I obtenim:

![image](https://github.com/XaSaFa/MP04/assets/110727546/d204e65a-ce57-47b5-bb39-73b6f0bc7b2b)

Però encara tenim un problema, el grup propietari té permisos r-x sobre la carpeta cliente, hem de modificar els permisos.

## Modificar els permisos de fitxer:

![image](https://github.com/XaSaFa/MP04/assets/110727546/ca8422c0-f231-40fc-807b-3186ab8edf2b)

Per tal de canviar els permisos d'un fitxer o directori utilitzem la comanda **chmod**.

chmod utilitza una notació basada en el binari per establir els permisos sobre un fitxer o directori.

Si tenim la carpeta anterior cliente així:

![image](https://github.com/XaSaFa/MP04/assets/110727546/e68068d9-eb6b-4409-9801-50e317afebe8)

Podem fer que el propietari només tingui els permisos complerts (rwx) i la resta cap:

```
sudo chmod -R 700 cliente/
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/cd7e5fb3-f3a7-477c-ac76-0e524e54f60b)

O que el grup propietari "editors" tingui permisos totals i la resta cap:

```
sudo chmod -R 070 cliente/
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/6ca223fd-ab76-420b-933b-cb8b0da1f895)

O que sigui qualsevol altre usuari qui tingui permisos totals:

```
sudo chmod -R 007 cliente/
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/3309c9eb-6914-4350-af51-0e4f41029e5f)

O, el que és més habitual, una combinació:

```
sudo chmod -R 755 cliente/
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/ce386a65-27b3-412d-bab2-710ee96c2514)

En el cas actual, com volem que els usuaris del grup "editors" puguin modificar els continguts de la carpeta cliente els donarem permisos plens:

```
sudo chmod -R 775 cliente/
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/9e24740a-5a89-43aa-a4e8-532c732a4274)

Així un usuari del grup editors podrà crear, modificar i esborrar fitxers dins de la carpeta cliente.
