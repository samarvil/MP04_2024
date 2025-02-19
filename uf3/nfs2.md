# Instal·lar NFS al client

# Pas 1.- Xarxa

El client estarà dins de la mateixa "Xarxa NAT" que el server.

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
