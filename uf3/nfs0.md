# NFS - Network File System

![image](https://github.com/XaSaFa/MP04/assets/110727546/52079fa1-70bc-4f78-8699-de72d98f0065)

NFS significa Sistema d'arxius en xarxa i és un protocol implementat l'any 1984 per l'empresa Sun Microsystems.

Aquest protocol s'utilitza en xarxes d'àrea local per crear un sistema de fitxers distribuït.

Va ser implementat com un estàndard obert i es va incloure a la publicació RFC per què tothom pogués implementar-lo.

## Objectiu

L'objectiu de NFS és que tothom pugui accedir a fitxers de xarxa com si fossin fitxers locals del mateix ordinador.

D'aquesta manera existeixen dos rols:

- Un ordinador servidor que emmagatzema els fitxers compartits.
- Un ordinador o, normalment més, que fan de clients i permeten als seus usuaris accedir als fitxers compartits pel servidor com si fossin locals.

Actualment, el protocol NFS és inclòs a la majoria de distribucions de Linux i a diferents versions d'altres sistemes operatius.

![image](https://github.com/XaSaFa/MP04/assets/110727546/821b5a03-478f-4f84-b8ba-fc1ed55de16c)


## Avantatges

- Al facilitar l'accés centralitzat a la informació, s'evita la duplicitat a diferents punts de la xarxa.
- De forma predeterminada obliga a que totes les operacions d'escriptura relacionades amb una actualització finalitzin abans de continuar, per assegurar la integritat de les dades.
- Permet emmagatzemar tot el perfil dels usuaris en el server.
- Permet compartir dispositius d'emmagatzemament complerts (com unitats òptiques, discs externs, memòries flash, ...).
