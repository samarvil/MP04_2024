# Webmin
Webmin és un programa administrador per a servidors de forma visual i a navegador que inclou alguna eina per configurar SAMBA.

# Instal·lar Webmin:

**Podeu anar a la web de webmin.com i seguir el tutorial o seguir els següents passos...**

## Pas 1.- Instal·lar Apache.

```
sudo apt install apache2
```

## Pas 2.- Afegir repositori de webmin a apt.

Editarem el llistat de repositoris.

```
sudo nano /etc/apt/sources.list
```

Afegim aquesta línia al final del fitxer i guardem.

```
deb http://download.webmin.com/download/repository sarge contrib
```

Descarreguem la key perquè Ubuntu confiï en el nou repositori.

```
wget -q -O- http://www.webmin.com/jcameron-key.asc | sudo apt-key add
```

## Pas 3.- Actualitzer paquets dels repositoris.

Actualitzem paquets.

```
sudo apt update
```

## Pas 4.- Instal·lar webmin.

Instal·lem webmin.

```
sudo apt install webmin
```

## Pas 5.- Accedir a webmin

Obrim un navegador al servidor i introduïm a la barra d'adreces:

```
localhost:10000
```

Acceptem el risc i ens dortirà la pantalla de login.

![image](https://github.com/XaSaFa/MP04/assets/110727546/a2a5faa5-5c61-4ed9-a130-5df27679e269)

Introduim credencials d'un usuari administrador i ja veurem webmin funcionant.

![image](https://github.com/XaSaFa/MP04/assets/110727546/1b5c3f64-5e5c-49df-8e43-fbefd0929c7e)

## Pas 5.- Actualitzar webmin.

Webmin ens avisa que tenim una versió vella de la clau de signatura i que l'actualitzem.

![image](https://github.com/XaSaFa/MP04/assets/110727546/8cc845ba-1b46-4ae8-866e-8a3ee5b949bc)



