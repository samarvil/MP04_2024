# Protocol SAMBA

<img src="https://github.com/XaSaFa/MP04/assets/110727546/50a63ab0-b038-4d70-baa2-c60a2c135e2f" width=500px/>

## Abans de SAMBA (SMB/CIFS)

El protocol SAMBA és una reimplementació de codi lliure del protocol SMB/CIFS.

SMB (Session Message Block) va ser desenvolupat inicialment a IBM per facilitar compartir fitxers i impressores mitjançant la xarxa.

A 1998 Microsoft va adaptar el protocol a les seves necessitats afegint noves característiques i canviant el nom a CIFS (Common Internet File System), segons Microsoft CIFS és un dialecte de SMB.

La documentació oficial de Microsoft sobre el protocol la podeu trobar [aquí](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cifs/d416ff7c-c536-406e-a951-4f04b2fd1d2b).

## El protocol SAMBA

<img src="https://github.com/XaSaFa/MP04/assets/110727546/08da469e-67a5-4711-9712-f088d1a717e2" width=500px/>

Samba neix de la necessitat de l'enginyer australià Andrew Tridgell qui un dia es va veure en la obligació de compartir un recurs d'un ordinador amb sistema UNIX amb el seu PC amb DOS, cosa que va aconseguir fer amb NFS...

Però el problema és que necessitaba utilitzar un programa que feia servir el protocol [NetBIOS](https://es.wikipedia.org/wiki/NetBIOS) entre els ordinadores UNIX i DOS, així que agafant les especificacions del protocol SMB, va començar a desenvolupar SAMBA, una alternativa de codi lliure per compartir recursos entre ordinadors amb Linux i Windows.

Un parell d'anys després va necessitar compartir la impressora que tenia connectada al seu PC amb Linux amb el PC de la seva dona que tenia DOS i va utilitzar SAMBA.

A dia d'avui el protocol és molt utilitzat quan es volen compartir recursos a xarxes d'ordinadors amb diferents sistemes operatius.

[Web oficial de Samba.](https://www.samba.org/samba/)

![image](https://github.com/XaSaFa/MP04/assets/110727546/64261277-9858-41e6-96b2-649353ffd81f)

