# Formatejar partició Linux

Quan tenim una partició creada a Linux l'hem d formatejar per poder utilitzar-la.

A l'exemple tenim dues particions:

![image](https://github.com/XaSaFa/MP04/assets/110727546/478c5d07-15e2-4d16-9485-d8e81fcafdb5)

Anem a formatejar-les de la següent forma:
- sdb1 a NTFS
- sdb2 a ext4

Per a fer-ho fem servir la comanda mkfs.

![image](https://github.com/XaSaFa/MP04/assets/110727546/0f126563-7507-40af-a843-c83be8e42d6c)

# Muntar particions

Les particions que hem creat i formatejat es muntaran a Ubuntu a la carpeta /media/usuari/.

![image](https://github.com/XaSaFa/MP04/assets/110727546/669a76db-2b20-4595-8377-9ec675bc5556)

Però potser és millor muntar-les a un directori diferent més fàcil de recordar, per a fer crearem un directori per una partició.

Anem a fer que la partició de 512MB (sdb1) es pugui accedir des del directori /disc1, per a fer-ho creem el directori.

![image](https://github.com/XaSaFa/MP04/assets/110727546/b5e09d44-3705-41e8-b6fb-dc15714fcd2f)

Desmuntem el directori a /media (de fet desmonto els dos).

![image](https://github.com/XaSaFa/MP04/assets/110727546/b9a6e412-f54c-42cd-9282-75f658c3e4e5)

I el muntem a /disc1.

![image](https://github.com/XaSaFa/MP04/assets/110727546/acfb3bd2-df1f-49cf-8533-9081c5f3311b)

# Mostrar particions i punt de muntatge

Per mostrar les particions i el seu punt de muntatge podem utilitzar la comanda lsblk (List Block Devices).

![image](https://github.com/XaSaFa/MP04/assets/110727546/e1913971-1ace-49ab-974c-1325c1eb5024)

