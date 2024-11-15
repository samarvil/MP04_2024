# Canviar el nom de l'equip.

A Ubuntu es pot canviar el nom de l'equip per terminal o per mode gràfic, mirem com fer-ho per terminal.

## Comanda hostnamectl

La comanda hostnamectl dona informació del nom de l'equip i més info com l'arquitectura, SO i, en el cas de la nostra MV, ens diu que és una màquina virtualitzada.

![image](https://github.com/XaSaFa/MP04/assets/110727546/48e1bc87-85fa-455f-92a1-f4475ef94b64)

Per canviar el nom de l'equip introduïm la comanda sudo hostnamectl set-hostname NOUNOM.

![image](https://github.com/XaSaFa/MP04/assets/110727546/6284dc32-5bdd-4235-b34c-d43f3361afc8)

Quan reiniciem el terminal sortirà el nom nou.

![image](https://github.com/XaSaFa/MP04/assets/110727546/83276907-9532-44f1-836d-e309895d651b)

Però per a que el canvi sigui correcte hem de modificar el nom del DNS de la màquina local al fitxer /etc/hosts

El fitxer està així:

![image](https://github.com/XaSaFa/MP04/assets/110727546/96b589a5-a49d-4d5a-8ba7-71d213845377)

I el deixarem amb el nou nom de la Màquina:

![image](https://github.com/XaSaFa/MP04/assets/110727546/904bd73b-78a1-4603-86ee-d06afa4207e6)
