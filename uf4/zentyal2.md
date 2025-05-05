# Users and Computers

Per accedir a la llista d'elements del domini hem d'anar a l'apartat "Users and Computers" del panell de control.

Aquí es pot observr l'estructura actual del domini.

![image](https://github.com/user-attachments/assets/ef03538a-96fa-44e0-8b14-33c554316f6d)

## Computers

Es crearà una entrada cada vegada que unim un equip nou al domini. En aquest cas només tenim l'equip Windows1.

![image](https://github.com/user-attachments/assets/35189286-a7c9-49ec-88f0-6fee9574cdb9)

## Groups

Aquí podem veure els grups d'usuaris del domini.

![image](https://github.com/user-attachments/assets/38f21f18-59e0-4165-94f3-a455ec978537)

Per crear un nou grup hem de clicar el botó + a la part de sota del panell i escollir Group.

![image](https://github.com/user-attachments/assets/55bc1744-2336-4d67-91f3-db29c8b41ddf)

![image](https://github.com/user-attachments/assets/09fba630-f18b-40ae-a973-0af151dc90c2)

![image](https://github.com/user-attachments/assets/46f3a071-bbe6-4037-a6d3-6774b150c100)

Per eliminar el grup només cal seleccionar-lo i clicar la paperera vermella a la part de sota del panell.

![image](https://github.com/user-attachments/assets/5fb11b3a-575d-4252-8b53-3b6277ad0260)


## Users

Si cliquem sobre Users podem veure els usuaris del domini, per defecte estaran creats Administrator i Guest.

L'usuari Administrator és l'administrador del domini i necessitem afegir-li una contrasenya.

![image](https://github.com/user-attachments/assets/e851edb2-6ff2-43e0-9247-213fb6f5ea1e)

Per afegir un usuari cliquem sobre el signe + a sota del panell.

Anem a afegir un usuari nou que serà membre del grup sales.

![image](https://github.com/user-attachments/assets/bb7bd28e-fa9b-48eb-a702-3e8da3087006)

Quan el tenim creat podem consultar-lo a la llista d'usuaris clicant sobre la icona del llapis.

![image](https://github.com/user-attachments/assets/2469cba4-a166-4f68-a8fc-a02e5a04072a)

Aquí podem canviar la seva informació, gestionar els grups als que pertany, limitant l'espai del seu directori home, canviar la seva contrasenya o deshabilitar el compte d'usuari.

![image](https://github.com/user-attachments/assets/502f3278-5ca7-48e7-a213-51b68e29f954)

## User Template

La plantilla d'usuari a la versió de prova de Zentyal només permet modificar la quota dels usuaris del domini.

![image](https://github.com/user-attachments/assets/96232b15-ff0b-40b1-9e88-0a222917d1c1)

Si es modifica aquest límit només quedaran afectats els usuaris que es crein posteriorment a la modificació, per modificar els anteriors hem d'anar directament a la seva fitxa d'usuari.

## Import/Export

Zentyal deixa importar i exportar contactes utilitzant fitxers per evitar fer-ho de forma manual, aquesta funcionalitat no està habilitada a la versió de prova.

![image](https://github.com/user-attachments/assets/bd0a7926-ae2a-404a-8c51-f195f8f90aac)

## LDAP Settings

A la part de LDAP veiem la informació LDAP del sistema i, a més, podem habilitar PAM.

PAM serveix per fer que quan es crei un nou usuari del domini també es crei un usuari local al server, cos que permetria, per exemple, connectar-se al server per ssh.

![image](https://github.com/user-attachments/assets/6fd26ae2-21cf-43c5-b974-77703ddea025)





