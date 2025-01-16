# Configurar client LDAP

Per a configurar un equip client i que es pugui autenticar mitjançant LDAP seguirem els següents passos:

## 1.- Actualitzar els repositoris

```
sudo apt update
```

## 2.- Instal·lar software

Instal·lem els paquests necessaris:

```
sudo apt install libnss-ldap libpam-ldap ldap-utils
```

Substituïm ldapi:/// per ldap:// i afegim la IP del servidor que hem configurat abans.

![image](https://github.com/XaSaFa/MP04/assets/110727546/137a71ee-1c49-4cc0-92f5-e2ba821d25c8)

Afegim el domini de LDAP:

![image](https://github.com/XaSaFa/MP04/assets/110727546/05237816-0cba-44f4-8bed-5d33f14a84ed)

Escollim la versió de LDAP (3):

![image](https://github.com/XaSaFa/MP04/assets/110727546/b6417d30-2938-4fff-b0ac-158447faadf1)

Escollim SI:

![image](https://github.com/XaSaFa/MP04/assets/110727546/dac39de2-a796-49c6-8eb3-6136cc93bfb7)

Després escollim NO:

![image](https://github.com/XaSaFa/MP04/assets/110727546/0cfe0a26-b2bc-470b-b85b-ba298cb0fefe)

Introduïm el compte administrador que vam crear al configurar el servidor:

![image](https://github.com/XaSaFa/MP04/assets/110727546/8a336709-bd13-4c0a-b604-eceacaaeae02)

I la contrasenya:

![image](https://github.com/XaSaFa/MP04/assets/110727546/e09eaa03-1a42-4a31-bda8-630a697184de)

A continuació seguirà la instal·lació.

![image](https://github.com/XaSaFa/MP04/assets/110727546/b848cb76-d63b-40ef-b50d-1fa7a6b0fc7f)

## Si ens equivoquem al configurar:

Executem la següent comanda i tornem a configurar.

```
sudo dpkg-reconfigure ldap-auth-config
```

## 4.- Editar els fitxers de configuració

### 4.1.- Editar /etc/nsswitch.conf

El fitxer per defecte és així:

![image](https://github.com/XaSaFa/MP04/assets/110727546/65dea226-fd8d-41ed-b8c9-1f07aec2071a)

En aquest fitxer hem de fer la següent modificació:

![image](https://github.com/XaSaFa/MP04/assets/110727546/cf6847ef-a1a6-4584-b13b-4e36b762701a)

Comprovem que tenim accés als usuaris de LDAP amb la comanda següent.

```
sudo getent passwd
```

On veurem els usuaris creats anteriorment.

![image](https://github.com/XaSaFa/MP04/assets/110727546/c067e6fd-b7f1-4871-9126-c5cf3ef8e3ca)

### 4.2.- Editar /etc/pam.d/common-session

Aquest fitxer estableix una serie de regles PAM per a l'inici de sessió.

Aquí serà on indicarem que s'ha de crear un directori home durant el primer inici de sessió d'un usuari també per als usuaris autenticats mitjançant LDAP.

Afegirem una última línia al fitxer:

![image](https://github.com/XaSaFa/MP04/assets/110727546/e1e8c7cb-b4d8-4923-944a-979d6a825917)

```
session optional       pam_mkhomedir.so skel=/etc/skel umask=077
```

Per comprovar que tot funciona bé fem una consulta per terminal i comprovem que tenim accés a les dades del servidor LDAP:

```
ldapsearch -x -H ldap://192.168.1.100 -b "dc=dungeonofbits,dc=com"
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/06d249cd-0b3d-4674-9488-0bd827bfce45)

# Provem que podem autenticar-nos amb un usuari de LDAP des del client:

Crea un usuari al servidor anomenat kerrigan. Una vegada creat, provarem a accedir al client com un usuari LDAP amb la comanda:

```
sudo su - kerrigan
```

El sistema mostra que està creant el directori /home/kerrigan, això només passarà la primera vegada.

![image](https://github.com/XaSaFa/MP04/assets/110727546/233301c6-884c-41cf-ae01-2d69bdaf3c29)

# 5.- Iniciar sessió des de la pantalla d'inici

# 5.1.- Instal·lar nslcd

Instal·larem el software nslcd, un servei que interactua entre LDAP i processos locals.

```
sudo apt install nslcd
```

La instal·lació ens pregunta la informació del nostre servei LDAP.

![image](https://github.com/XaSaFa/MP04/assets/110727546/39fc3fe9-9ec0-46e7-9786-f356a7176718)

![image](https://github.com/XaSaFa/MP04/assets/110727546/480c5f63-8a0e-4450-8ab8-a890b9a79a43)

Després reiniciem l'equip:

```
sudo reboot
```

A partir d'ara ja podem utilitzar usuaris creats a LDAP per iniciar sessió des del nostre equip.

# 5.2.- Permetre login manual a Linux Mint

Per defecte no es permet el login manual a Linux Mint, per activar-lo anem a:

![image](https://github.com/XaSaFa/MP04/assets/110727546/b39f6f1a-3bdf-4555-9b20-06ba7db511ab)

Inici->Administración->Ventana de inicio de sesión.

Activem l'opció d'inici manual.

![image](https://github.com/XaSaFa/MP04/assets/110727546/f778af3e-38ae-48d6-bf1f-000e2e484753)

# 5.3.- Inici de sessió amb usuari LDAP

Reiniciem l'equip i ens sortirà l'inici de sessió.

![image](https://github.com/XaSaFa/MP04/assets/110727546/ce5f86fd-f653-4a94-8168-c990c6c7715b)

Introduim el nom d'usuari LDAP.

![image](https://github.com/XaSaFa/MP04/assets/110727546/ba031162-5118-483a-9114-b064bf3739b4)

I la seva contrasenya i ja estarem dintre de la nostra sessió:

![image](https://github.com/XaSaFa/MP04/assets/110727546/39c69302-5d8d-46ae-8d36-d80a75991c94)




