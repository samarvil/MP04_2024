# Usuaris i equips:

## Usuaris

![image](https://github.com/XaSaFa/MP04/assets/110727546/f275d779-ba4b-4441-8ab3-eeb8b78abe0f)

Els usuaris d'Active Directory no són estrictament usuaris, també poden representar accés a serveis o aplicacions de la màquina local o una màquina en remot.

Els comptes d'usuari també es poden dir entitats de seguretat.

El compte d'usuari permet:

- **Autenticar un usuari dins del sistema:** Només un usuari que té usuari i contrasenya podrà iniciar sessió.
- **Autoritzar o denegar accés a recursos:** Un usuari que ha iniciat sessió tindrà només accés als recursos als quals tingui permissos d'accés.

Cada compte d'usuari està identificat per un número únic al sistema que es diu SID (Security IDentifier), per seguretat cada ususari tindrà un compte diferent, no compartiran usuaris.

### Comptes per defecte:

Quan es crea el domini també es creen comptes noves:

- **Administrador:** Té control total sobre el domini i no es pot eliminar ni treure del grup Administradors (sí es podrà canviar el seu nom o deshabilitar).

- **Convidat:** Aquest compte està deshabilitat de forma predeterminada, no es recomanda habilitar-la. Serveix per donar accés a usuaris que encara no tenen compte al sistema o la tenen deshabilitada. De forma predeterminada no requereix contrasenya (això es pot canviar).
- **Assistent d'ajuda:** S'utilitza per iniciar sessions d'Assistència remota i té accés limitat a l'equip. Es cra automàticament quan es solicita una sessió d'assistència remota i s'elimina quan deixen d'existir solicituds.

Des del punt de vista de seguretat pot ser interessant canviar el nom de l'usuari administrador.

## Comptes d'Equips:

![image](https://github.com/XaSaFa/MP04/assets/110727546/253581ca-223d-4360-8851-e92ec8f20974)

Un compte d'equip serveix per autenticar els diferents equips que es connecten al domini, donant accés o denegant-lo als diferents recursos del domini.

Els comptes d'equip han de ser únics pel domini.

## Comptes de Grups:

Un compte de grup és un **conjunt d'objectes que s'administra com una unitat**, pot contenir comptes d'usuari, d'equip, contactes i altres grups.

Un compte d'usuari o d'equip que està dins d'un grup es diu membre del grup.

### Àmbit dels grups

L'àmbit indica a quines parts de la xarxa funciona un grup, els àmbits poden ser:

- **Àmbit Local:** Per accedir a serveis del mateix domini.
- **Àmbit global:** Poden tenir permís a recursos d'altres dominis.
- **Àmbit universal:** Perteneixen a qualsevol domini del bosc i poden tenir accés a recursos de qualsevol domini del bosc.

### Tipus de grups

Poden ser de dos tipus.

- **Grups de distribució:** Serveixen només per distribució de correus electrònics.
- **Grups de seguretat:** Permeten assignar permisos a comptes d'usuari, d'equips o grups de recursos compartits. Ens deixen:
  - Assignar drets d'usuari.
  - Assignar permisos per recursos als grups de seguretat.

 

