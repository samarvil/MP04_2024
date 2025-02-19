# Accedir a la carpeta compartida des d'un client

Ara configurem els ordinadors clients per tal d'accedir als continguts de la carpeta compartida.

# Pas 1.- Crear un punt de muntatge

Les carpetes compartides hauran d'estar dins del sistema d'arxius de l'ordinador client, per aquest motiu fa falta crear un punt de muntatge.

Crearem **A L'ORDINADOR CLIENT** una subcarpeta dins de /mnt que anomenarem nfs i dins ficarem els recursos compartits.

```
sudo mkdir -p /mnt/nfs/shared
```

També li donarem permisos als usuaris sobre aquestes carpetes:

```
sudo chmod -R 777 /mnt/nfs
```

# Pas 2.- Muntar la carpeta del server al punt de muntatge

Hem de muntar el recurs original al punt de muntatge anterior, per a fer-ho escrivim:

```
sudo mount 192.168.1.10:/shared /mnt/nfs/shared
```

Podem comprovar que l'ancoratge ha funcionat bé amb la comanda:

```
df -h
```

I veurem que, efectivament, tenim l'ancoratge correctament establert.

![image](https://github.com/XaSaFa/MP04/assets/110727546/bf9bcba2-6a7f-41fe-be8a-338ef4d9d387)

Amb la comanda mount també podem veure el punt d'ancoratge:

![image](https://github.com/XaSaFa/MP04/assets/110727546/49ff01f2-60c4-4b5e-89bc-8f6b65bf02d3)

# Pas 3.- Comprovar accés al recurs compartit

Ara hem de comprovar que tenim accés als fitxers de la carpeta compartida.

Primer mirem l'accés de lectura:

```
ls /mnt/nfs/shared
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/faeb938b-eb70-4344-a660-35d2d857f42c)


Després comprovem si podem escriure, per això crearem un fitxer:

```
touch /mnt/nfs/shared/caracola.txt
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/3606dc0e-67a8-474f-adcd-07237d80b31e)
