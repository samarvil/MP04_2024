# Instal·lació d'Ubuntu

## Versions d'Ubuntu

Ubuntu disposa de dues versions:

### Desktop: 

Versió d'escriptori. És la versió estàndard per a usuaris que volen utilitzar aplicacions amb interfície gràfica.

![image](https://github.com/XaSaFa/MP04/assets/110727546/dcf479c7-878a-455b-8943-0eaeac01accc)

[Link per descarregar versió desktop.](https://ubuntu.com/download/desktop/thank-you?version=22.04.3&architecture=amd64)

### Server: 

Versió de text, versió lleugera sense interfície gràfica que s'utilitza per gestionar serveis.

![image](https://github.com/XaSaFa/MP04/assets/110727546/fa8f17c9-20c0-46f2-838b-7dbbfb780e3c)

Com estem tenint problemes amb la configuració de xarxa de VirtualBox utilitzarem la versió Desktop.

## Modes d'instal·lació

Ubuntu ens deixa instal·lar-lo a un disc dur que tingui un altre sistema operatiu instal·lat com podria ser Windows.

Però tenint en compte que al fer-lo servir de servidor estarà sempre en funcionament no té sentit tenir dos sistemes operatius instal·lats en el disc dur.

## Particions

**IMPORTANT**: Utilitzarem la taula de particions MBR. 

![image](https://github.com/XaSaFa/MP04/assets/110727546/a096702e-0a10-4ad7-8941-0c1327301be7)

Les particions són blocs en els que dividim una unitat física d'emmagatzematge (disc dur, unitat flash, ...), cada partició funciona com si fos un disc independent amb el seu propi sistema de fitxers.

Les particions poden ser de 3 tipus:

- Particions primàries: En un disc poden haver com a màxim 4 particions primàries i com a mínim 1 on estarà instal·lat el SO si utilitzem el disc per arrencar Ubuntu.
- Particions esteses:  Només pot haver una per disc com a màxim. Si existeix ocupa l'espai d'una partició primària, així que, com a màxim, hi podran haver 3 particions primàries i una estessa en un disc. Una partició estessa només serveix per contenir unitats lògiques.
- Particions lògiques: Sempre estaran incloses dins una partició estessa, a una partició estessa poden haver fins a 23 particions lògiques.

**Important**: Linux només permet fins 15 particions en total per disc.

## Identificadors de disc a Linux

A Linux els discos s'identifiquen amb una codificació que depèn del tipus de disc utilitzat (IDE, SATA o SCSI).

Així **els discos IDE tenen el prefix hd**, mentre que **els discos SATA i SCSI tenen el prefix sd**.

Després s'utilitza **una lletra per identificar el disc**, per ordre alfabètic, així el primer disc SATA serà sda, el segon serà sdb...

Finalment s'afegeix **un número que identifica la partició**, els números 1 a 4 identifiquen particions primàries, a partir del número 5 identifiquen particions lògiques.

Exemples de nomenclatura de particions:
![image](https://github.com/XaSaFa/MP04/assets/110727546/9b9fd5e0-b283-44d7-81d1-0877d38c8c9f)

Es pot veure que quan existeixen particions lògiques no hi ha una partició sda4 perquè el 4 correspondria a la partició estessa que no és accesible.

## Sistema de fitxers

A Linux el sistema de fitxers habitual és Ext4, que serà el que utilitzarem per instal·lar Ubuntu.

## Requisits d'instal·lació d'Ubuntu

Els requisits d'Ubuntu 22.04LTS són:

![image](https://github.com/XaSaFa/MP04/assets/110727546/aaa3a719-19c9-4273-932d-3cd3830036cc)






