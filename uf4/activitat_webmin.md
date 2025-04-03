# Utilitzant webmin per administrar el servidor

- Entregueu link a un repositori **públic** (un link per alumne) de Github on feu les següents tasques.
- Expliqueu el que feu amb text i captures.
- **Fer tot des de webmin**
- Rúbrica:
  - 2 punts - Estructura del document (portada, índex, captures correctes, text ben formatat...).
  - 1 punt - Exercici 1.
  - 1 punt - Exercici 2.
  - 1 punt - Exercici 3.
  - 1 punt - Exercici 4.
  - 1.5 punt - Exercici 5.
  - 1.5 punt - Exercici 6.
  - 1 punt - Exercici 7.

## 1.- Crear i modificar usuaris

**Fer tot des de webmin**

- Has de crear dos usuaris bakalao_X i techno_X on (X és el vostre cognom).
- Els usuaris et passaran el hash de la seva contrasenya, no la contrasenya real. (podeu fer servir openssl).
- Cada usuari tindrà un directori a home igual al seu nom d'usuari.
- Utilitzaran bash com a shell.
- Els usuaris estaran dins del grup que tingui el seu mateix nom i dins del grup usuaris_empresa.
- L'usuari techno no podrà fer login després del dia 31-03-2025.
- Comproveu que els usuaris poden iniciar sessió.
- Canvia la data del sistema (utilitzant webmin) i comprova que techno no pot iniciar sessió si estem a dia 01-04-2025.

## 2.- Programar tasques

- Programa una tasca que neteja els paquets de Linux que ja no s'utilitzen una vegada al mes.
- Programa una tasca diaria que apaga l'ordinador a les 14:00.
- Comprova que funcionen (canvia dia i hora del sistema mitjançant webmin).
  
## 3.- Instal·lació de software

- Utilitza webmin per mostrar quins paquets de software es podrien actualitzar.
- Des de webmin actualitza un paquet.
- Utilitza webmin per instal·lar un joc de apt.
- Utilitza webmin per instal·lar gimp de apt.
- Utilitza webmin per desinatl·lar el joc que heu instal·lat abans.

## 4.- Serveis

- Utilitza webmin per mostrar els serveis que s'inicien amb el sistema.
- Utilitza webmin per mostrar els serveis que estan actius.
- Utilitza webmin per mostrar l'estat del servidor Apache.
- Utilitza webmin per aturar Apache.
- Utilitza webmin per mostrar l'estat del servidor Apache apagat.
- Utilitza webmin per reiniciar Apache.
- Utilitza webmin per mostrar l'estat del servidor Apache reiniciat.

## 5.- Quotes de disc

Activa les quotes de disc pels usuaris amb la comanda: 

```
sudo apt install quota quotatool
```

- Utilitza webmin perquè l'usuari bakalao_X no pugui tenir més de 2 MB d'informació al disc.
- Comprova que el límit de la quota funciona.
- Utilitza webmin perquè l'usuari techno no pugui tenir més de 10 fitxers al disc.
- Comprova que el límit de la quota funciona.

## 6.- Còpies de seguretat

- Utilitzant el mòdul de Webmin Filesystem Backup fes una còpia de seguretat del directori /home al directori /backups (l'haureu de crear si no existeix).
- Modifica alguns fitxers de /home.
- Recupera la còpia de seguretat.
- Comprova que els fitxers de /home són els correctes.
- Programa una còpia de seguretat de /home/bakalao_X per els divendres a les 21:00.
- Esborra la còpia de seguretat programada anteriorment.

## 7.- Compartició

- Crea un recurs a webmin que, utilitzant samba, comparteixi una carpeta anomenada "area_public_X" per a usuaris sense autenticar en forma de lectura i escriptura.
- Crea un recurs a webmin que, utilitzant samba, comparteixi una carpeta anomenada "pontaeri_privat_X" per a usuaris _X i techno només de lectura.
- Comprovar des de Windows que aquests recursos funcionen.

## Grups
1.- Raul i Francesc

2.- Aleix i Zulema

3.- Jordi i Marc

4.- Sergi i David

5.- Javi i Edgar

6.- Leo

7.- Jan i Unai

8.- Iker
