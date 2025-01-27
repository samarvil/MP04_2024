# Crear carpetes personals per als usuaris de Domini.

Windows ens permet tenir una carpeta situada al servidor amb accés personal per a cada usuari del domini.

Això significa que cada usuari dispossarà d'espai al servidor el qual percebrà com una unitat compartida.

## Crear la carpeta contenidora al servidor:

Dins del servidor crearem l'espai d'emmagatzematge per als usuaris, a l'exemple ho farem sobre la unitat C:.

La carpeta que creem servirà per contenir les carpetes personals dels usuaris.

![image](https://github.com/XaSaFa/MP04/assets/110727546/a7005000-8f58-4288-9a37-346702689574)

## Canviar els permisos sobre la carpeta a compartir

Hem de canviar els permisos d'usuaris sobre la carpeta creada, per a fer-ho cliquem botó dret i seleccionem "propiedades".

![image](https://github.com/XaSaFa/MP04/assets/110727546/dea90b70-a238-4374-93c0-c97ff346a570)

Anem a la segona pestanya "Compartir".

![image](https://github.com/XaSaFa/MP04/assets/110727546/7104f28d-96db-4b27-a6b0-ce07c5c5a9fe)

Seleccionem "Uso compartido avanzado":

![image](https://github.com/XaSaFa/MP04/assets/110727546/f306b557-c345-4203-af5d-6f8b495c6754)

"Compartir esta carpeta":

![image](https://github.com/XaSaFa/MP04/assets/110727546/cf6523e0-e954-4233-a35f-a5190016deb6)

Aquí podem escollir el nom del recurs compartit o deixar el que té per defecte que és el nom de la carpeta.

![image](https://github.com/XaSaFa/MP04/assets/110727546/71bdfe6d-eac6-469a-8f71-5c4e0a67c604)

![image](https://github.com/XaSaFa/MP04/assets/110727546/af8ed95b-4e5e-4955-a2ae-9ce2d42ff257)

Ara hem de canviar els permisos.

**Per defecte els permisos estan definits per a Tots els usuaris**.

Anem a canviar-ho per a que només els usuaris del domini tinguin permisos.

![image](https://github.com/XaSaFa/MP04/assets/110727546/54766f34-a78c-4477-b8ee-80e17011474f)

![image](https://github.com/XaSaFa/MP04/assets/110727546/76bb4c3b-8a0f-4888-a243-24bef8b9b1b5)

![image](https://github.com/XaSaFa/MP04/assets/110727546/b6ce7e80-69c9-4c89-af43-029a06b19e1b)

![image](https://github.com/XaSaFa/MP04/assets/110727546/33afe756-4f40-41b9-a06b-165783348f70)

![image](https://github.com/XaSaFa/MP04/assets/110727546/78d95a51-a2ef-4f7e-9af6-cb4614c461da)

![image](https://github.com/XaSaFa/MP04/assets/110727546/a56be4c2-91ef-4376-80d6-4e392e3722ac)

![image](https://github.com/XaSaFa/MP04/assets/110727546/a30b3c73-9755-48d8-bf0f-4399faa2a424)

![image](https://github.com/XaSaFa/MP04/assets/110727546/8e6ba5ea-cc64-4086-b0be-2f57fc290f2d)

![image](https://github.com/XaSaFa/MP04/assets/110727546/d881635c-9956-4669-8b98-926108121979)

![image](https://github.com/XaSaFa/MP04/assets/110727546/3aff1845-efb9-48f9-959f-1e67da91a5c9)

![image](https://github.com/XaSaFa/MP04/assets/110727546/e897c626-f6b1-4e67-95d9-31060384b143)

## Configurar les carpetes personals

Ara que ja tenim configurada la carpeta contenidora hem de configurar l'accés dels usuaris.

Anem a "Administrador del Servidor->Herramientas->Usuarios y Equipos de Active Directory"

![image](https://github.com/XaSaFa/MP04/assets/110727546/5be8da9b-cc68-481e-a07d-53055a081215)

![image](https://github.com/XaSaFa/MP04/assets/110727546/e366b417-f4ca-466d-91dd-4077724ac8d6)

Seleccionem amb SHIFT els usuaris que volem que tinguin carpeta personal.

![image](https://github.com/XaSaFa/MP04/assets/110727546/e72151fb-7893-462d-9a0a-9edbc69ae6ea)

Fem click dret i seleccionem "Propiedades".

![image](https://github.com/XaSaFa/MP04/assets/110727546/d3e3df61-6efd-49d0-ae1e-1b98816ceb10)

Seleccionem "Perfil":

![image](https://github.com/XaSaFa/MP04/assets/110727546/fd1ebea6-727a-456d-a85a-0a576ffa27f1)

![image](https://github.com/XaSaFa/MP04/assets/110727546/8074e196-fd25-4584-a9e4-f2e3a3663f15)

Aquí tenim dues opcions, podem seleccionar una ruta i llavors la carpeta compartida es veuria com una carpeta del sistema.

Si seleccionem conectar veurem la carpeta com una unitat de xarxa.

![image](https://github.com/XaSaFa/MP04/assets/110727546/bb2baf99-1534-4d31-a295-c0f2c88e5cce)

Seleccionem conectar com unitat de xarxa:

![image](https://github.com/XaSaFa/MP04/assets/110727546/89dcedf5-ea5f-40cd-bf92-82a0efdf0f28)

Una unitat de xarxa té dues dades:

- Lletra de la unitat. Es crearà una unitat nova al sistema amb la lletra assignada.
- Ruta al recurs: És la ruta a la carpeta compartida.

### Establir la ruta:

La ruta té el format següent:

\\servidor\carpeta_contenidora\carpeta_compartida

- Servidor és el nom de l'ordinador servidor. En aquest cas: 
- carpeta_contenidora és el nom de la carpeta que hem creat al server.
- carpeta_compartida és el nom que tindrà la carpeta personal de l'usuari.

En el nostre exemple els dos primers valors els podem agafar de la carpeta que hem creat al server, botó dret:

![image](https://github.com/XaSaFa/MP04/assets/110727546/eac22a4a-c6c6-48ce-af36-4026050e75f2)

I per al tercer valor utilitzarem la variable d'entorn **%username%** que és el nom d'usuari.

Per tal en l'exemple quedarà així:

```\\WIN-DPMGFEH4FMF\Personal\%username%```

![image](https://github.com/XaSaFa/MP04/assets/110727546/c1ad571b-4a46-4540-a3bc-44c7a7f118f8)

## Obrir carpeta personal des de l'ordinador del client.

Ara podem accedir des d'un usuari de Windows 10 i veure que té una carpeta personal a la unitat Z:.

![image](https://github.com/XaSaFa/MP04/assets/110727546/2394311f-3ade-41b8-b00d-73ed7f3c4f25)

![image](https://github.com/XaSaFa/MP04/assets/110727546/077b4d5c-a805-40d2-b7a8-5f53770c98a5)

![image](https://github.com/XaSaFa/MP04/assets/110727546/915a1e47-7379-4fd7-a1cc-2916ff862961)

![image](https://github.com/XaSaFa/MP04/assets/110727546/75ecd621-e759-4ca6-bbe4-1c99748b98bd)

Podem crear un fitxer:

![image](https://github.com/XaSaFa/MP04/assets/110727546/b8e462f1-002f-4b14-99f5-30cd74c4a3da)

### Al server es veuen les modificacions

![image](https://github.com/XaSaFa/MP04/assets/110727546/0b01c101-1fa1-4b4d-bc96-8ca9ec3368c1)

![image](https://github.com/XaSaFa/MP04/assets/110727546/0b4a6b6c-3cb1-46e4-97e1-226a747e0654)
