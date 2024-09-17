# UF1 - Sistemes operatius propietaris en xarxa.

# Sistemes de fitxers a Windows:

Farem un repàs als principals sistemes de fitxers de Windows.

![image](https://github.com/XaSaFa/MP04/assets/110727546/7574af42-8d5f-4902-b2b0-a8388c902caf)

### FAT (File Allocation Table):

Format admès pràcticament per tots els sistemes operatius existents per ordinador personal.

S'utilitza com a mecanisme d'intercanvi de dades entre sistemes operatius distints que coexisteixen en el mateix
ordinador, el que es coneix com entorn multiarranc. També s'utilitza en targetes de memòria i dispositius similars.

Però:
- Tamany màxim de fitxers i discos molt limitat.
- Fragmentació (alenteix lectures i escriptures).

### FAT 32

Va ser la resposta per superar el límit de grandària de FAT al mateix temps que es mantenia la compatibilitat amb MS-DOS.

La grandària màxima d’un fitxer en FAT32 segueix resultant insuficient avui dia per aplicacions de captura i edició de vídeo, les quals superen fàcilment aquest límit.

### NTFS (New Technology File System)

És un sistema d'arxius dissenyat específicament per Windows NT, amb l'objectiu de crear un sistema d'arxius eficient, robust i amb seguretat incorporada des de la seva base.

És adequat per particions de molta grandària requerides en estacions de treball d'alt rendiment i servidors.

Si passem de FAT 32 a NTFS, el procés no es pot tornar a invertir.

### ExFAT (Extensible File Allocation Table)

Un sistema de fitxers que permet manipular fitxers molt grans i incrementar la velocitat d'escriptura i lectura.

Son utilitzar-se en unitats flash con discos externs o pendrives.  

# Sistemes de fitxers a Linux:

![image](https://github.com/XaSaFa/MP04/assets/110727546/5e864f1b-48d3-4857-ac51-e2891cb99565)

### EXT 2 (Second Extended File System)

És un sistema d'arxius molt més avançat que el MSDOS, amb suport de correcció i detecció d'errors, compressió d'arxius, major tolerància a la fragmentació d'arxius i amb uns temps de resposta molt superiors, encara que a un cost superior d'utilització de memòria.

Aquest sistema d'arxius el trobarem a estacions amb sistemes operatius Linux (Red Hat, Fedora, Debian), o Unix en general.

### EXT 3 i EXT 4

Sistema de fitxers amb un registre diari (bitàcora) dels arxius del sistema (journaling filesystem).

Restableix el sistema molt ràpidament en cas d'una fallada, perquè els processos d'escriptura són protocol·litzats durant l'ús del sistema.

Molt eficaç a l'hora de treballar amb grans quantitats d'arxius petits.

Igual que EXT2 trobarem aquest sistema d'arxius en equips amb sistemes operatius Linux o Unix.

### Altres

Existeixen altres sistemes fitxers per a Linux com ReiserFS, XFS, JFS i d'altres però són menys utilitzats.

# Journaling file system

El Journaling és una tècnica per la qual el sistema, quan ha de modificar fitxers (fer una transacció), guarda certa informació sobre els canvis a efectuar en un "journal", un diari i es bloquegen les estructures afectades.

En cas d'haver una fallada del sistema que impedeix finalitzar la transacció el sistema operatiu utilitza el journal per restablir els fitxers a l'estat anterior a la mateixa (desfer els canvis).

Quan ha acabat una transacció s'esborra el journal i es desbloquegen les estructures de dades afectades.

Així s'eviten fer moltes comprovacions sobre el sistema de fitxers i colapsar-lo.


🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️

**Activitat:**

1.-Tenint en compte els sistemes de fitxers següents: FAT16, FAT32, NTFS, ExFAT, Ext2, Ext3, Ext4 fes una taula on es vegi:

a.- El tamany de fitxer màxim.

b.- El tamany de volum màxim.

c.- El tamany màxim de nom de fitxer.

d.- Sistema operatiu que el soporta.

e.- Si el sistema de fitxers suporta Journaling o no.

2.- Quin sistema de fitxers ha de tenir un disc per instal·lar els següents sistemes operatius?

a.- Windows 10. 

b.- Windows 2016 Server. 

c.- Ubuntu 22 Desktop. 

d.- Ubuntu 22 Server.

🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️
