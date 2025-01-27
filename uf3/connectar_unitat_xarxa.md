# Connectar una unitat de xarxa

## net use

Hi ha diferents formes de connectar una unitat de xarxa, una d'elles és mitjançant la comanda net use.

Per fer servir net use necessitem un terminal de CMD de Windows.

Partim de la base de que tenim una carpeta compartida anomenada **public** al servidor anomenat **WIN-DPMGFEH4FMF**.

![image](https://github.com/XaSaFa/MP04/assets/110727546/c603ea50-b6da-4281-b1d7-e956f455ce53)

La comanda net use té els següents paràmetres:

net use <lletra unitat> <\\nom servidor\nom recurs compartit> </usuari>

El nom del servidor pot ser també la seva IP. Exemple:

![image](https://github.com/XaSaFa/MP04/assets/110727546/9f4af515-ae41-4543-bced-b5c3239adcb9)

## Connectar a una unitat de xarxa una única vegada:

Podem connectar a un recurs compartit així:

```
net use f: \\WIN-DPMGFEH4FMF\public /PERSISTENT:NO
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/d6a22411-e966-45c4-a80d-6c48d6556316)

Una vegada es reiniciï l'ordinador és desconnectarà la unitat.

## Connectar a una unitat de xarxa de forma permanent:

Si volem que la unitat es connecti sempre que iniciem sessió utilitzarem el paràmetre permanent mb valor YES.

```
net use f: \\WIN-DPMGFEH4FMF\public /PERSISTENT:YES
```

## Desconnectar unitat de xarxa:

Per desconnectar una unitat de xarxa utilitzem el paràmetre DELETE.

Per desconnectar la unitat F: fem:

```
net use f: /delete
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/f3c63e39-d806-4e0f-8237-bd42ee99d528)

## Connectar a un recurs utilitzant nom d'usuari i contrasenya:

Si estem utilitzant un recurs al qual només podem accedir mitjançant permisos d'usuari utilitzarem el parèmetre user.

A l'exemple següent tenim la carpeta public a la qual volem accedir amb l'usuari pere del domini 2SMX i que té la contrasenya Admin1234, per això fem servir la comanda:

```
net use f: /delete
net use f: \\WIN-DPMGFEH4FMF\public /user:pere@2SMX "Admin1234"
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/c13a4785-ebc1-483f-ade7-8182970837aa)
