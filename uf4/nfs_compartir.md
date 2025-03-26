# Compartir recursos de Linux a Windows amb NFS

Per comprobvar que tenim accés als recursos del servidor des de Windows fem el següent:

## Pas 1.- Mostrar els recursos compartits del servidor

Per a mostrar els recursos compartits des de Windows anem a una finestra i introduïn la ip del server d'aquesta manera:

```\\IP_servidor``` (en el nostre exemple és \ \192.168.1.10)

![image](https://github.com/XaSaFa/MP04/assets/110727546/2585f4b3-b988-4ebf-8932-faf9e71ce27d)

# Muntar una unitat amb un recurs del servidor

Potser interessant deixar una unitat muntada al client que ens doni accés a una carpeta compartida del servidor.

Per a fer-ho escriurem la següent instrucció al terminal del client.

## 1.- Muntar la unitat des de terminal client

Obrim un terminal a Windows i escrivim la següent comanda:

```
mount -o anon 192.168.1.10:/shared N:
```

Amb aquesta instrucció agafem la carpeta **shared** del servidor, que té la IP **192.168.1.10** i la muntem a la unitat **N:**.

La opció -o anon és per què la connexió sigui anònima.

[Aquí podeu consultar les opcions de la comanda mount a Windows](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/mount%20).

## 2.- Fes que la unitat es munti automàticament quan s'iniciï l'ordinador

Si volem que l'usuari/a tingui accessible automàticament quan iniciï sessió ho hem d'indicar a les opcions d'inici de Windows.

### Pas 1.- Anem a Inici

Al client utilitzem la tecla Windows+R i escrivim "shell:startup":

![image](https://github.com/XaSaFa/MP04/assets/110727546/f2f38eff-dece-4830-80e1-2d49b4e90e57)

Això obrirà la carpeta inici de l'ordinador:

![image](https://github.com/XaSaFa/MP04/assets/110727546/6d011e06-a6aa-4869-8d06-9f5b0132911f)

### Pas 2.- Canviem les opcions de vista

Activem la opció de mostrar extensió de fitxers:

![image](https://github.com/XaSaFa/MP04/assets/110727546/67602028-a224-48b2-a13e-d831737c0ea3)

Creem un nou document de text

![image](https://github.com/XaSaFa/MP04/assets/110727546/a63ec605-7f52-4596-88ef-b19d0d6ec609)

L'anomenem nfs1.bat i l'editem amb la comanda per muntar una unitat de xarxa:

![image](https://github.com/XaSaFa/MP04/assets/110727546/1a267a13-3e5e-4a6d-a248-feaf7554d1cc)

Reiniciem i comprovem que la unitat es munta automàticament.

![image](https://github.com/XaSaFa/MP04/assets/110727546/0ac554a0-89ac-4de9-b004-a7c8c7e03903)


