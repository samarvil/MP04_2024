# Active Directory Domain Services (AD DS).

![image](https://github.com/XaSaFa/MP04/assets/110727546/96b83f77-7006-469e-8aae-1a0988dae804)

## Què és Active Directory?

Es tracta d'un directori jeràrquic d'objectes d'un sistema informàtic que utilitza Microsoft.

Els objectes que es guarden al directori poden ser equips, usuaris, serveis, vòlums d'emmagatzematge, grups...

Active Directory permet crear polítiques de grup o realitzar operacions com la instal·lació de programes, de forma simultània i centralitzada, a diferents equips o aplicar actualitzacions crítiques.

Active Directory funciona gràcies a protocols de xarxa com LDAP. Kerberos, DHCP o DNS.

## Directori

És un **repositori per a la informació relativa als usuaris i recursos d'una organització**.

Active Directory és un directori que conté informació sobre les propietats i ubicació dels diferents tipus de recursos de la xarxa.

## Domini

Un domini és una **colecció d'objectes dins del directori** que formen un subconjunt administratiu.

Els dominis tenen noms que utilitzen el protocol DNS, per aquest motiu Active Directory necessita almenys un servidor DNS a la xarxa.

## Objecte

Objecte és un nom genèric per als components que formen part del directori, com una impressora, una carpeta compartida, un usuari o un grup.

En general hi ha tres categories d'objectes:

- Usuaris: Identificats amb el seu nom d'usuari i contrasenya. Es poden organitzar en grups per simplificar l'administració.
- Recursos: Diferents elements accesibles pels usuaris que tinguin privilegis, com carpetes compartides, impressores...
- Serveis: Funcionalitats a les que pot tenir accés un usuari, com per exemple el correu electrònic.

## Controlador de domini

Un controlador de domini **conté la base de dades dels objectes del directori**, inclosa la informació relativa a la seguretat.

Dins d'un domini poden coexistir diferents controladors de domini.

**Quan instal·lem Active Directory a Windows Server l'ordinador es converteix en un controlador de domini.**

## Arbres

Un arbre és una **col·lecció de dominis que depenen d'una arrel comú organitzats en jerarquia**.

La jerarquia estarà indicada amb un espai de noms DNS comú.

Per exemple els dominis GONDOR.COM y OSGILIATH.GONDOR.COM forman part del mateix arbre.

Per altra banda els dominis MORDOR.ES y GONDOR.COM no són part del mateix arbre.

L'objectiu de crear aquesta estructura es fragmentar les dades del Active Directory, de tal manera que es serveix només la informació de les parts necessàries, estalviant amplada de banda.

Si un usuari es creat dins d'un domini, l'usuari serà conegut automàticament a tots els dominis que depenguin jeràrquicament del domini al que pertany.

![image](https://github.com/XaSaFa/MP04/assets/110727546/d19467a1-c73e-4a7c-a6c4-90e50a0e9e0c)

## Bosc

És el contenidor més gran d'un Active Directory.

Si un arbre és un conjunt de noms de domini dependents de la mateixa arrel, un bosc és un conjunt d'arbres, per tant no tindran una arrel comuna entre ells.

Un bosc ha de tenir, com a mínim, un arbre. Això vol dir que quan creem un Active Directory estem creant un arbre i un bosc, de forma predeterminada.

El domini arrel del bosc tindrà l'esquema del bosc que es compartirà amb la resta de dominis del bosc.

![image](https://github.com/XaSaFa/MP04/assets/110727546/0adfc8a8-1fa2-4082-b8b7-d3b5c5475d32)

## Unitats organitzatives

Una Unitat Organitzativa (UO) és un contenidor que permet crear subconjunts d'objectes dins del domini per tal d'administrar-los de forma conjunta.

![image](https://github.com/XaSaFa/MP04/assets/110727546/9342cd6c-9dfd-4f56-ba1d-98aadcee2472)

## Esquema

A Active Directory un esquema és l'estructura de la base de dades, utilitzarem la paraula atribut per referir-nos a cadasqun dels tipus d'informació emmagatzemats.

També podem parlar de classe per referir-nos a determinats tipus d'objectes.

Un objecte en concret rep el nom d'instància.

Per exemple la classe usuari serà com una plantilla que defineix els tipus d'usuari, mentre que un usuari concret serà una instància.

## Llocs

Es tracta d'un grup d'ordinadors que es troben relacionats, de forma lògica, a una localització geogràfica particular.

En realitat també poden estar connectats mitjançant una connexió amb una amplada de banda adequada.

![image](https://github.com/XaSaFa/MP04/assets/110727546/3ab83a45-615e-4956-9a02-704aa8fee73b)

## Relacions de confiança 

Són un mètode de comunicació segura entre dominis, arbres i boscos, **permeten als usuaris d'un domini del Active Directory autenticar-se a un altre domini del directori**.

Existeixen dos tipus de relacions de confiança: unidireccionals i bidireccionals, a més les relacions poden ser transitives o no.

Al següent exemple un usuari de Tree 1 pot accedir als recursos dels dominis de Tree 2 i un usuari de Tree 2 també pot accedir als recursos de Tree 1 (sempre que tinguin privilegis).

![image](https://github.com/XaSaFa/MP04/assets/110727546/c0a32a61-2cf9-4a97-8f47-8abc9eeadec6)

### Unidireccionals

Un domini que conté recursos confia en un altre domini que conté els usuaris, els usuaris poden accedir als recursos, però un usuari que formés part del domini de recursos no podria accedir al domini d'usuaris.

![image](https://github.com/XaSaFa/MP04/assets/110727546/319d1d6f-9d9d-485f-bcab-e82dc303901e)

### Bidireccionals

Els usuaris dels dos dominis poden accedir a recursos de l'altre domini.

![image](https://github.com/XaSaFa/MP04/assets/110727546/7153368b-4574-4231-957e-d081f06d837c)

### Transitivitat

Si una relació de confiança és transitiva la confiança s'hereta, en cas contrari no.

![image](https://github.com/XaSaFa/MP04/assets/110727546/dc3a709e-4f0c-42fb-bd6e-d53dd31f66a8)

## Mestre d'operacions

En un domini poden coexistir diferents controladors de domini, per evitar situacions en les que dos controladors de domini alterin informació vital del domini, com per exemple l'esquema, existeix la figura del Mestre d'operacions.

El mestre d'operacions és l'únic que pot fer certes accions com, per exemple:

- Administrar els canvis de l'esquema del directori.
- Inscriure els dominis al bosc.
- Administrar la nomenclatura del domini.
- Administrar el moviment d'objectes d'un domini a un altre
- ...





