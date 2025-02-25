# Instal·lar NFS al client

# Pas 1.- Xarxa

El client també tindrà dos adaptadors de xarxa:
1. Adaptador de xarxa NAT amb configuració DHCP
2. La mateixa xarxa interna del server. Recorda afegir la IP del server al DNS principal de la red.

![image](https://github.com/XaSaFa/MP04/assets/110727546/ea533192-45ea-4c89-be7d-a6df9abb57d4)

I pot fer ping al server:

![image](https://github.com/XaSaFa/MP04/assets/110727546/91d53a02-7e69-4a2f-8ce0-414fabe2fda1)

# Pas 2.- Actualitzem repositoris

```
sudo apt update
```

# Pas 3.- Instal·lem els paquets necessaris

```
sudo apt install nfs-common rpcbind
```
