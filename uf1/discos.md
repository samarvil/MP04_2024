# Afegir un disc nou a la màquina virtual (MV):

Anem a afegir un disc dur de 10GB a la nostra màquina virtual, això ho farem amb la MV apagada:

![image](https://github.com/XaSaFa/MP04/assets/110727546/56fd5caa-0459-4c6d-bfdd-ca1a5a32b509)

![image](https://github.com/XaSaFa/MP04/assets/110727546/50311426-d863-4933-ab45-9697b1937278)

![image](https://github.com/XaSaFa/MP04/assets/110727546/f814b192-12d7-4e18-b3b7-a0c6801d4789)

Veurem que a Windows no surt el nou disc perquè no té cap volum formatat.

![image](https://github.com/XaSaFa/MP04/assets/110727546/e5863a3d-2bf1-4caf-9e90-ac251e95fe5e)

Si obrim l'administrador d'equips des del menú de Windows o, directament amb la comanda **compmgmt.msc** podem accedir a l'administració de discos:

![image](https://github.com/XaSaFa/MP04/assets/110727546/0a34e681-8470-4d0d-9eb3-20ccd128d490)

Aquí veiem que tenim el disc nou assignat al PC amb el codi Disco 1:

![image](https://github.com/XaSaFa/MP04/assets/110727546/86228d3e-5a7d-4646-99ed-cce0da3ff5db)

Una altra manera de veure els discos d'un equip és mitjançant el panell d'administrador del servidor:

![image](https://github.com/XaSaFa/MP04/assets/110727546/330c1029-912e-4ae9-8420-abb244b0f22a)

I seleccionem "Discos" per veure'ls:

![image](https://github.com/XaSaFa/MP04/assets/110727546/8403c78f-f6bd-4010-ab7e-edcd4203dc2f)

# Utilització del símbol de sistema:

A vegades, durant el procés d’instal·lació us manquen dades que necessiteu per continuar la instal·lació. En el moment en què l’assistent de la instal·lació us pregunta ¿Dónde desea instalar Windows?.

![image](https://github.com/XaSaFa/MP04/assets/110727546/f63730b3-1466-4523-a788-5b170155aa92)

Si es denega el permís per executar una comanda hem d'iniciar el símbol del sistema com administrador.

# Gestió i creació de particions - Diskpart:

El gestor de línia de comandes de discs i particions es diu **diskpart**.

Per veure les comandes disponibles escrivim a dins de diskpart **help**

![image](https://github.com/XaSaFa/MP04/assets/110727546/56568931-f654-4acf-bc33-e723de0a6230)
![image](https://github.com/XaSaFa/MP04/assets/110727546/d3eb0cd1-2349-4583-8fb9-bc6bb1be0f0d)

## Mostrar els discos de l'equip (list disk):

![image](https://github.com/XaSaFa/MP04/assets/110727546/6060997c-26e3-48b8-b255-1b9320d818e9)

## Seleccionar un disc (select disk #):

![image](https://github.com/XaSaFa/MP04/assets/110727546/38fabf2c-77e7-428e-99fb-ecb00f67c05f)

## Disc, Volum, partició seleccionat:

**Quan escrivim ordres de diskpart hem d'estar segurs que ho fem al disc, partició o volum que toca, quan fem un list disk, list volume o list partition el que està seleccionat tindrà un ```*``` davant.**

## Crear una partició:

Es fa servir la comanda **create partition tipus size=X** on X és el tamany en MB de la partició i tipus indica si la partició serà:

- primària: primary
- estesa: extended
- lògica: logical

 En aquest exemple estem creant una partició primària de 5GB (5120MB):

![image](https://github.com/XaSaFa/MP04/assets/110727546/da712de6-74bc-46f5-a07f-8d4c197d79fb)

**Important:** Recordeu que per crear particions lògiques primer heu de crear una partició estesa.

## Assignar lletra a una partició:

La lletra d'unitat serveix per identificar la ruta a la partició des del S.O.

S'utilitza la comanda **assign leter=X** on X és la lletra d'unitat.

![image](https://github.com/XaSaFa/MP04/assets/110727546/6a56c7da-cd6e-47b5-86fd-0e012270058a)

## Formatejar partició:

Formatejar una partició li assigna un format, un tipus de sistema de fitxers: FAT, FAT32, exFAT, NTFS, UDF o ReFS.

Durant el formatejat es pot assignar una etiqueta a la partició. 

El següent exemple formateja la partició a format NTFS, li assigna l'etiqueta "PartyZ" i fa el format ràpid.

![image](https://github.com/XaSaFa/MP04/assets/110727546/7b895a94-916e-4af6-8372-09cbd2a26c0d)

I aquí els detalls de la partició:

![image](https://github.com/XaSaFa/MP04/assets/110727546/421fde10-998e-4c30-a3a0-a1be23753e27)

Quan el disc estigui formatejat ens sortirà a l'explorador de fitxers de Windows:

![image](https://github.com/XaSaFa/MP04/assets/110727546/07b3ff97-ef8f-4499-8e32-c86744bcf146)

I, després d'actualitzar, també al Panell d'administració de Windows:

![image](https://github.com/XaSaFa/MP04/assets/110727546/6b4b0885-54d4-4646-bf8b-09f753ab948c)

## Ampliar el tamany d'una partició:

Per a ampliar el tamany d'una partició utilitzem la comanda extend seguida del tamany a ampliar, per exemple si volem ampliar 1GB la partició fem:

![image](https://github.com/XaSaFa/MP04/assets/110727546/d92cd18c-a041-40b1-86a2-28c8372e39d2)

## Reduir el tamany d'una partició:

Per a reduir el tamany d'una partició utilitzem la comanda shrink seguida del tamany que volem treure (restar) a la partició, per exemple si volem treure 4GB de la partició fem:

![image](https://github.com/XaSaFa/MP04/assets/110727546/ed10e250-c345-487a-bd43-e73732d1e527)

## Eliminar partició/volum:

Per eliminar una partició es fa servir la comanda delete.

Primer ens assegurem que tenim seleccionada la partició que volem esborrar.

A l'exemple següent esborrem el volum 4:

![image](https://github.com/XaSaFa/MP04/assets/110727546/ee35864a-c7ba-4a51-b8ff-f3693cbece8d)

## Esborrar disc:

**PRECAUCIÓ** aquesta comanda elimina tots els volums i particions d'un disc, assegureu-vos d'haver seleccionat el disc correcte.

La comanda és **clean all**, al següent exemple esborrem un disc que tenia una partició.

![image](https://github.com/XaSaFa/MP04/assets/110727546/b7a94065-33ff-4d07-bfa5-4432032aee0d)
