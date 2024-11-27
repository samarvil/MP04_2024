# Usuaris a Linux

## Superusuaris (root)

![image](https://github.com/XaSaFa/MP04/assets/110727546/a768d4ca-2a09-4d59-935a-1d8c94aa3be4)

A Linux els usuaris que tenen el control total sobre el sistema operatiu (instal·lar aplicacions, crear i esborrar carpetes i directoris a qualsevol punt de muntatge, crear usuaris, ...) es diuen **root** o **superusuaris**.

A Ubuntu l'usuari root per defecte està desactivat.

### sudo

La forma de fer que el sistema operatiu utilitzi els permisos de root a l'hora d'executar una comanda és afegint la paraula **sudo** davant de la instrucció, per exemple per instal·lar el servidor apache escriurem:

```
sudo apt install apache2
```

Llavors el sistema demanarà la contrasenya de root, la qual haurem d'escriure per poder executar la instrucció.

Quan fem servir la comanda sudo **el sistema estarà sense demanar la contrasenya de root durant 15 minuts**, per evitar que estiguem escrivint la contrasenya continuament.

### sudo su

Una altra forma d'executar comandes restringides al superusuari és transformar el nostre usuari a root, això s'aconsegueix amb la instrucció sudo su

![image](https://github.com/XaSaFa/MP04/assets/110727546/7df6b037-b79e-4f8e-a219-900fb1cf9266)

D'aquesta manera l'usuari serà root, però haurem de sortir de root quan volguem tornar a ser un usuari normal amb la comanda **exit**.

![image](https://github.com/XaSaFa/MP04/assets/110727546/391385c2-89a4-48ec-a96e-804e6e02c1bb)

### sudo visudo

Ubuntu té una instrucció anomenada **sudo visudo** que permet editar el fitxer amb els usuaris root del sistema /etc/sudoers

Quan executem la instrucció s'edita el fitxer /etc/sudoers.tmp, quan sortim de l'edició es guardan els canvis a /etc/sudoers

![image](https://github.com/XaSaFa/MP04/assets/110727546/f00476cd-0c25-4a01-9d9b-6dd468273fcc)

Editant aquest fitxer podem fer algunes coses:

#### Canviar el temps que triga el sistema en tornar a demanar la contrasenya amb les instruccions sudo

Si editem a sudo visudo i canviem:

```
Defaults env_reset
```

Per:

```
Defaults env_reset , timestamp_timeout = 2
```

Fem que el sistema demani la contrasenya quan passin 2 minuts de la darrera vegada que s'ha introduït.

Si canviem 2 per 0 es demanarà la contrasenya a cada instrucció sudo.

#### Afegir un usuari root

Creem un usuari anomenat xavi2 que no té permisos de root.

![image](https://github.com/XaSaFa/MP04/assets/110727546/1cb19925-048a-482b-8fe9-5e660f3f5e8b)

![image](https://github.com/XaSaFa/MP04/assets/110727546/ff6ca41f-ec12-4dea-aef1-c45899d0823b)

Editant el fitxer podem afegir usuaris superusers.

![image](https://github.com/XaSaFa/MP04/assets/110727546/3a4832f5-bc6d-4fce-9989-a658d8721947)

Aquí afegim l'usuari anomenat xavi2 com a root.

![image](https://github.com/XaSaFa/MP04/assets/110727546/51024a6a-1d16-417b-b743-46fb2d4d79c9)

Ara xavi2 tindrà permisos de root.

![image](https://github.com/XaSaFa/MP04/assets/110727546/771766f7-fe03-40f5-8d1d-555ea2190bb5)


També podem afegir un usuari al grup sudo per a què tingui poders de root.

![image](https://github.com/XaSaFa/MP04/assets/110727546/dce89a3c-0f46-49a4-afc7-985ecd3aee9d)
