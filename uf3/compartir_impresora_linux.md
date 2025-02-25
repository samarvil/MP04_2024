# Compartir impressora a Linux 

![image](https://github.com/user-attachments/assets/e6bb3464-6716-4165-98ef-e250dfa7038d)

Compartir una impressora entre diferents equips amb Linux permet economitzar recursos, una de les formes d'aconseguir que una impressora pugui ser utilitzada des d'un equip diferent al que està instal·lada és utilitzant CUPS (Common UNIX Printing System) que permet utilitzar un ordinador com a servidor d'impressió. 

En aquest tutorial instal·larem una impressora PDF virtual a un ordinador que farà de servidor i la afegirem a un equip que farà de client. 

## 1.- Instal·lem CUPS

```
sudo apt update
sudo apt install cups
```

## 2.- Instal·lem impressora PDF virtual

```
sudo apt install printer-driver-cups-pdf
```

## 3.- Compartim la impressora per CUPS

Obrim el **navegador** i anem a l'adreça  ```http://localhost:631```.

![image](https://github.com/user-attachments/assets/74db4eb0-cd4c-4a49-9527-16202cf53a1f)

![image](https://github.com/user-attachments/assets/2c978f01-79f4-4da2-ba2c-8855ab110cab)

![image](https://github.com/user-attachments/assets/32bfb549-29f9-4f7a-8217-0cab91e579f5)

![image](https://github.com/user-attachments/assets/f384bccf-face-4654-9852-0d862f2c58ef)

![image](https://github.com/user-attachments/assets/02eb9b25-59d5-4d3a-ba44-308dc0f12795)

![image](https://github.com/user-attachments/assets/d162713f-04fa-4941-aaae-50ea41d520d0)

![image](https://github.com/user-attachments/assets/5356d665-b06c-4260-b1ba-4a9f49e102f9)

![image](https://github.com/user-attachments/assets/54cdee2d-e86b-4c42-b063-421bc00cec8f)

## 4.- Canviar el fitxer de configuració de CUPS

Afegir, si no està ja, aquestes línies al fitxer de configuració ```/etc/cups/cupsd.conf```

```
# Permitir acceso desde otros equipos
Listen 0.0.0.0:631
Listen [::]:631

# Permitir acceso a la configuración de CUPS desde cualquier IP de la red
<Location />
  Order allow,deny
  Allow @LOCAL
</Location>

<Location /admin>
  Order allow,deny
  Allow @LOCAL
</Location>

<Location /printers>
  Order allow,deny
  Allow @LOCAL
</Location>

```

## 5.- Reiniciar el servei CUPS

```
sudo systemctl restart cups
```

## 6.- Afegir impressora a l'ordinador CLIENT

![image](https://github.com/user-attachments/assets/4385ec6c-4012-4546-9746-202e81394bff)

Ja està detectada

![image](https://github.com/user-attachments/assets/bc97b7f8-2458-4c02-963d-6b6504aad196)

Els fitxers PDFs queden guardats a l'ordinador servidor:

![image](https://github.com/user-attachments/assets/6eafc33b-d8d9-4ca4-9e7a-21d15a2ba452)

# Ampliació:

1. Fes que la carpeta del server on estan els PDFs es comparteixi mitjançant NFS a la carpeta /PDF de l'ordinador client.
2. Munta la carpeta /PDF del client a la carpeta /home/usuari/Documents/PDF de l'usuari actual.
