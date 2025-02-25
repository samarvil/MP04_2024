# Instal·lar NFS al server

# Pas 1.- IP fixa

Al servidor jo utilitzaré una connexió de xarxa "Xarxa Interna" amb la següent configuració:

![image](https://github.com/XaSaFa/MP04/assets/110727546/6e44eed9-302c-4c2e-a5bc-07d17f0ea1b9)

![image](https://github.com/XaSaFa/MP04/assets/110727546/4d5cabe7-d960-40aa-b02a-7cab67be1376)

La qual em dona accés a Internet i al gateway de la xarxa:

![image](https://github.com/XaSaFa/MP04/assets/110727546/13f0240f-dfb9-4832-bf2b-f53c16ccf28e)

# Pas 2.- Actualitzem els repositoris

```
sudo apt update
```

# Pas 3.- Instal·lem NFS

Primer instal·lem els paquets necessaris:

```
sudo apt install nfs-kernel-server
```

Després comprovem la instal·lació:

```
sudo service nfs-server status
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/aefdfecc-3fe3-4717-9469-4b770dd1bc4d)

