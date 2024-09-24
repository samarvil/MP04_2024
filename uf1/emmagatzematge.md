# Emmagatzematge a Windows

![image](https://github.com/XaSaFa/MP04/assets/110727546/bfc99412-52dd-4119-9ce5-52b2d524bdd0)

L'emmagatzematge a Windows es fa en els discos durs, els quals solen ser SSD (Solid State Disk) o HDD (Hard Disk Drive) i estan connectats per SATA a l'ordinador.

Al disc dur es guarden els fitxers del Sistema Operatiu, de les aplicacions i dels usuaris.

# Taules de partició:

Existeixen dos models generals actualment per a les taules de partició dels discos durs, MBR i GUID.

## MBR (Master Boot Record): 

El MBR servia per identificar el bloc d'arrencada del disc dur i iniciar el sistema operatiu als ordinadors amb BIOS, degut a que és un sistema antic té una serie de limitacions degut als bits que es feien servir per indicar les direccions accessibles al disc.

Les principals són la de no poder tenir particions superiors en tamany a 2TB i la de tenir com a màxim 4 particions primàries.

## GPT (GUID Partition Table): 

És el sistema de taula de particions i arrencada que està substituint a MBR, necessita un ordinador amb UEFI per a arrencar el sistema operatiu.

Al utilitzar direccions de disc de 64 bits la mida màxima d'un disc és de 9,4ZB (Zettabytes).

![image](https://github.com/XaSaFa/MP04/assets/110727546/21262373-91ac-4446-b3bf-e1ec49c6a46c)

GPT admet 128 particions com a màxim per disc amb una mida màxima de 18 Exabytes cadascuna.

# Particions:

![image](https://github.com/XaSaFa/MP04/assets/110727546/69ec5f04-9028-4866-9a35-c23b6f478d53)

- El disc dur es pot dividir en compartiments anomenats particions.
- Cada partició té un sistema de fitxers, que pot ser NTFS, FAT32...
- La partició primària que conté el MBR té una limitació de tamany de 


Hi ha 3 tipus de particions:

- **Primària:** Només poden haver 4 particions primàries a un disc o 3 primàries i una extesa. Si el S.O. reconeix el format d'aquestes particions serà capaç d'accedir. És el tipus de partició on sol estar instal·lat el S.O.
- **Estesa:** Aquesta partició serveix per trencar el límit de 4 particions en un disc. Només pot existir una partició estesa per disc. Serveix per contenir particions lògiques.
- **Lògica:** Aquestes particions només es poden fer a una partició estesa, serveixen per guardar informació o aplicacions, no el S.O. A Windows hi ha un límit de 23 particions lògiques, a Linux només poden haver 15 particions en total de tots els tipus.

# Volums:

![image](https://github.com/XaSaFa/MP04/assets/110727546/98d605a0-ad94-49bb-9351-4e06f24777fd)

Els volums serveixen per indicar al sistema operatiu quines unitats d'emmagatzematge té disponibles, el seu nom, lletra d'accés i tipus de sistema de fitxers.

Un volum pot estar format per una part d'un disc dur, més d'una part del mateix disc dur o la suma de parts de diferents discos durs.

Això vol dir que un volum pot ser més gran en tamany que un dels discos durs que el formen.

Hi ha diferents tipus de volums, els més habituals a un disc dur d'usuari és el Volum simple que és una part del disc que funciona com una unitat físicament independent.
