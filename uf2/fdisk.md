# fdisk i gdisk

Són comandes similars, fdisk es fa servir per discos amb taules de particions MBR, gdisk per discos amb taules de particions GPT.

Només veurem fdisk.

## fdisk

fdisk (Format Disk) és una comanda que ens permet manipular particions dels nostres discs durs.

Podem fer servir fdisk per veure el tamany d'un.

![image](https://github.com/XaSaFa/MP04/assets/110727546/de394410-3102-4da2-ac7c-c28ea8296a12)

Per veure les particions d'un disk podem utilitzar la comanda fdisk -l nom de disc, per exemple:

![image](https://github.com/XaSaFa/MP04/assets/110727546/b23566cb-ed90-45c9-9082-294d3d0af309)

Per manipular un disc concret escrivim la comanda sudo fdisk nom de disc, per exemple:

![image](https://github.com/XaSaFa/MP04/assets/110727546/4aa52999-f590-4cbe-a3d7-5b2acea16dff)

Les comandes de fdisk apareixen al escriure m:

![image](https://github.com/XaSaFa/MP04/assets/110727546/64460ac3-99c6-49b4-be25-095fbe2d338e)

Per veure l'espai lliure escriurem F:

![image](https://github.com/XaSaFa/MP04/assets/110727546/31885fbb-2fa9-4060-aac1-d9d5348b23a1)

Aquí es veu que no hi ha espai lliure.

## Crear una nova partició

Utilitzem un disc buit que estarà muntat a /dev/sdb i per a la nova partició escrivim **n**.

Les particions no es crearan realment fins que introduïm la comanda **w**.

![image](https://github.com/XaSaFa/MP04/assets/110727546/1fe252cc-ce23-4b61-b3dd-302f970065f8)

Es pot veure la nova partició amb sudo fdisk -l:

![image](https://github.com/XaSaFa/MP04/assets/110727546/ce3c74cc-2d5f-4fa6-bfed-46c92102f416)

## Mostrar particions

Amb **p** podem veure les particions creades:

![image](https://github.com/XaSaFa/MP04/assets/110727546/9c8ed257-ae67-4801-ad5e-f0afd5f1ca82)

## Canviar el sistema de fitxers d'una partició

Amb t podem canviar el sistema de fitxers d'una partició, a l'exemple canviem a FAT16

![image](https://github.com/XaSaFa/MP04/assets/110727546/3a900f3f-828e-4bf1-90f9-d090b54e9d64)

Quan ho fem podem llistar els sistemes de fitxers amb L:

![image](https://github.com/XaSaFa/MP04/assets/110727546/7bbb89ea-493e-43e4-a67e-201befb9f0ec)

## Esborrar una partició

Hem creat les següents particions al disc /dev/sdb:

![image](https://github.com/XaSaFa/MP04/assets/110727546/f782c6a4-7074-47bf-bffa-0c43bad5031a)

Per esborrar la segona partició, o sigui /dev/sdb2, farem servir la comanda **d** dins de fdisk:

![image](https://github.com/XaSaFa/MP04/assets/110727546/df6e631a-cc39-4c29-91ea-e9bf5b500da5)



