# Compartició de carpetas des de Linux a Windows amb SAMBA

## Compartir les carpetes del directori home

### Pas 1.- Instal·lar Samba

```
sudo apt install samba
```

### Pas 2.- Afegir usuaris locals a Samba

Hem d'afegir a Samba tants usuaris locals com volem que tinguin accés als recursos mitjançant Samba.

Els usuaris **han d'existir prèviament al sistema Linux**.

Possem d'exemple l'usuari xavi.

```
sudo smbpasswd -a xavi
```

### Pas 3.- Editar el fitxer de configuració de Samba

Editem /etc/samba/smb.conf

```
sudo nano /etc/samba/smb.conf
```

Afegim al final.

```
[homes]
   comment = Home Directories
   browseable = yes
   read only = no
   create mask = 0700
   directory mask = 0700
   valid users = %S
```

### Pas 4.- Reiniciem samba

```
sudo service smbd restart
```

### Pas 5.- Creem un fitxer a la carpeta compartida

Per tal de comprovar que tenim accés a la carpeta compartida i als fitxers crearem un fitxer a dins.

```
touch /home/xavi/fitxer-home 
```

### Pas 6.- Accedir des de Windows 

Comprovem l'adreça IP de l'ordinador Linux.

![image](https://github.com/XaSaFa/MP04/assets/110727546/fc3d3d37-b31f-4683-b470-5bb8604ba69a)

És **MOLT IMPORTANT** que les dues màquines **estiguin a la mateixa xarxa** i puguin fer ping entre elles. Si fa falta **desconnecteu el Firewall de Windows**.

A Windows anem a Equip.

![image](https://github.com/XaSaFa/MP04/assets/110727546/1f0d190a-223c-47cd-886d-8527047c3f7f)

Introduïm la ip i, com a recurs compartit, el nom del directori home, en aquest cas xavi. 

Seleccionem "conectar con otras credenciales".

![image](https://github.com/XaSaFa/MP04/assets/110727546/d865832a-984e-4154-b590-5152ca49e65f)

Escrivim les credencials de l'usuari propietari del home al que volem accedir i accedirem a la carpeta.

Com podem observar aquí està el fitxer que hem creat abans a la màquina Linux.

![image](https://github.com/XaSaFa/MP04/assets/110727546/05c5465b-77dd-4c7e-999d-2abef430a931)

## Compartir una carpeta pública per usuaris anònims

### Pas 1.- Instal·lar Samba

```
sudo apt install samba
```

### Pas 2.- Crear una carpeta per als usuaris anònims

Per exemple aquesta.

```
sudo mkdir /var/samba
sudo chmod 777 /var/samba/
```
### Pas 3.- Editar el fitxer de configuració de SAMBA

Editem /etc/samba/smb.conf i afegim el recurs compartit que es dirà **Public**.

```
sudo nano /etc/samba/smb.conf
```

```
[public]
  comment = public anonymous access
  path = /var/samba/
  browseable =yes
  create mask = 0660
  directory mask = 0771
  writeable = yes
  guest ok = yes
```

### Pas 4.- Reiniciar SAMBA

Reiniciem samba.

```
sudo service smbd restart
```

### Pas 5.- Creem un fitxer a la carpeta compartida

Per tal de comprovar que tenim accés a la carpeta compartida i als fitxers crearem un fitxer a dins.

```
touch /var/samba/fitxer-public 
```

### Pas 6.- Accedir des de Windows 

Hem d'activar la compartició anònima a Windows 10.

Entrem a gpedit.msc

![image](https://github.com/user-attachments/assets/3af2d9db-e654-4627-ac5d-77a5c3de4f4e)

Activem la compartició anònima.
![image](https://github.com/user-attachments/assets/747f2ba9-f74c-42be-baa1-9011e87779de)

Comprovem l'adreça IP de l'ordinador Linux.

![image](https://github.com/XaSaFa/MP04/assets/110727546/fc3d3d37-b31f-4683-b470-5bb8604ba69a)

És **MOLT IMPORTANT** que les dues màquines **estiguin a la mateixa xarxa** i puguin fer ping entre elles. Si fa falta **desconnecteu el Firewall de Windows**.

A Windows anem a Equip.

![image](https://github.com/XaSaFa/MP04/assets/110727546/1f0d190a-223c-47cd-886d-8527047c3f7f)

Introduïm la ip i, com a recurs compartit, el nom del directori Public que és el que té la carpeta a la que volem accedir al fitxer de configuració de samba. 

![image](https://github.com/XaSaFa/MP04/assets/110727546/6179f28e-ef03-4aa6-9000-4e19758c5377)

Ja tenim accés al directori i podem observar el fitxer que hem creat abans.

![image](https://github.com/XaSaFa/MP04/assets/110727546/aef9fe82-15e5-413b-a247-fb123ed98cca)
