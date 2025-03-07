# Instal·lar NFS a Windows

## Pas 1.- Activar NFS a Windows

Aquest pas es fa a la MV client amb SO Windows 10.

Anem a "Panel de Control" i canviem la vista:

![image](https://github.com/XaSaFa/MP04/assets/110727546/5e732a37-b495-4c98-aa57-f4c25073bb15)

![image](https://github.com/XaSaFa/MP04/assets/110727546/f4a91ee1-d6cc-44ca-8967-c51721088c8a)

Escollim "Programas y características":

![image](https://github.com/XaSaFa/MP04/assets/110727546/dfcce148-ae75-43e4-8da1-549a3c6d7b83)

Cliquem a "Activar o desactivar características de Windows":

![image](https://github.com/XaSaFa/MP04/assets/110727546/6ce765fb-ae32-4423-b622-5558e229bec5)

A "Servicios para NFS" seleccionem tots els ítems i instal·lem:

![image](https://github.com/XaSaFa/MP04/assets/110727546/11727ad5-fc49-4568-82fe-2effcb19a41f)

![image](https://github.com/XaSaFa/MP04/assets/110727546/63d6eb44-3493-4a57-80be-b55d3776a4e1)

## Pas 2.- La MV client i la MV servidor han d'estar a la mateixa xarxa.

Les dues MV han d'estar a la mateixa xarxa, podem fer servir una xarxa NAT i comprovar amb ping si es "veuen".

## Pas 3.- Mostrar els recursos compartits del servidor

Per a mostrar els recursos compartits des de Windows anem a una finestra i introduïn la ip del server d'aquesta manera:

```\\IP_servidor``` (en el nostre exemple és ```\\192.168.1.10```)

![image](https://github.com/XaSaFa/MP04/assets/110727546/2585f4b3-b988-4ebf-8932-faf9e71ce27d)

