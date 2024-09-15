# MP04: sistemes operatius en xarxa

## UF1: sistemes operatius propietaris en xarxa

### Introducció als sistemes operatius.

Les computadores (de l'anglès computer) i els ordinadors (del francès ordinateur) tal i com les coneixem avui dia, es a dir, màquines programables de propòsit general, apareixen a meitat del s.XX amb el nom de Mainframes.

![image](https://github.com/XaSaFa/MP04/assets/110727546/a23ed4be-c847-4b68-8627-e0586ce7b624)

ENIAC - 1946

![image](https://github.com/XaSaFa/MP04/assets/110727546/a5501ba8-3637-4add-95fa-ca41172558b8)

DEC PDP 10 - 1960

![image](https://github.com/XaSaFa/MP04/assets/110727546/d9c1294c-f457-4601-be0a-abad2056a5c2)

IBM SYSTEM 370 - 1970

A partir de 1975 amb l'ordinador Altair comencen a existir ordinadors personals amb un cost assequible que pot ser comprat i utilitzat a les cases de la gent de forma còmode.

![image](https://github.com/XaSaFa/MP04/assets/110727546/11c8646d-d70e-414e-8dcd-715cf94cc3a6)

ALTAIR 8800 - 1975

Els ordinadors amb més èxit de l'època són el Apple II de 1977 i el IBM PC (Personal Computer de 1981).

Els sistemes operatius domèstics comencen amb el CP/M (Control Program/Monitor) de l'empresa Digital Research, un sistema operatiu basat en consola de teclat (sense finestres) que va servir de base per a la creació posterior del MS-DOS (Microsoft 1981).

![image](https://github.com/XaSaFa/MP04/assets/110727546/9ad71e59-c0c4-4567-a057-d85f5d2e9e1c)

CP/M - Digital Research

![image](https://github.com/XaSaFa/MP04/assets/110727546/bf0688fc-2379-4e38-b2aa-68f081a33b0f)

MS-DOS - Microsoft

Més endavant aparèixen els sistemes domèstics amb interfícies gràfiques com MacOS, Windows o Linux que adapta un sistema operatiu anterior anomenat Unix.

![image](https://github.com/XaSaFa/MP04/assets/110727546/563ff35d-ea5f-43fc-b461-92ce674e0360)

Windows 3.11

![image](https://github.com/XaSaFa/MP04/assets/110727546/8edd95dd-1932-42b2-ab7b-5b92e81ae146)

Windows 98

![image](https://github.com/XaSaFa/MP04/assets/110727546/3efc4806-2c66-4119-af16-1d481fc5d891)

Mac OS X

### Què és un sistema operatiu en xarxa (NOS - Network Operating System):

- Un S.O. s'encarrega de coordinar l'interacció entre el hardware (CPU, memòria, perifèrics) i el software (programes, aplicacions).

- Un S.O. en xarxa coordina l'interacció entre els recursos de la xarxa i els equips de la mateixa, de forma centralitzada mitjançant un ordinador principal.

- El S.O. en xarxa manté dos o més equips units mitjançant un mitjà de comunicació (Wifi, cable) amb l'objectiu de compartir recursos hardware i software.

- Els S.O. en xarxa més utilitzats són: Windows server, Unix i Linux.

- D'altres com Novell Netware o LAN Manager van ser NOS que ja no s'utilitzen.

- A una xarxa amb NOS hi ha dos tipus de rols diferenciats:
  - Servidors: Equipats amb un NOS. S'encarreguen de proporcionar recursos als clients.
  - Clients: Equipats amb S.O. monolloc. Es connecten i validen al servidor per poder treballar.

 Si no existeix un NOS tots els equips tenen la mateixa consideració (d'igual a igual).

### Software i hardware d'un NOS:

- Software als clients: Disposen de software per connectar amb els servidors.
- Software als servidors: Tenen tota mena de software específic per subministrar serveis als clients.

![image](https://github.com/XaSaFa/MP04/assets/110727546/3b1c2419-bee8-4934-ba9c-e07854585d5a)

- Els NOS actuals són multitasca (poden executar més d'una tasca a la vegada) i multiprocés (poden distribuir l'execució de programes en més d'un processador).

### Característiques d'un NOS:

- La gestió centralitzada de recursos i equips de la xarxa és realitzada per un servidor amb S.O. en xarxa.

- Apareix la figura de l'administrador de xarxa, que gestiona la
infraestructura de la xarxa.

- Connecta tots els equips i recursos de la xarxa.
  
- Coordina les funcions dels perifèrics i recursos.

- Proporciona seguretat controlant l'accés a les dades i recursos.

- Optimitza la utilització dels recursos.

### Funcionalitats d'un NOS:

- Compartir recursos:
  - Permetre diferents usuaris amb nivells d'accés diferents als recursos (privilegis)
  - Coordinació a l'accés als recursos.

- Gestió d'usuaris o grups d'usuaris que poden accedir als recursos de la xarxa:
  - Crear, esborrar, modificar usuaris o grups usuaris.
  - Atorgar permisos d'usuari a recursos de xarxa.
  - Assignar o denegar permisos d'usuari a la xarxa.

- Gestió xarxa:
  - Monitorització (congestió, fallades).
  - Seguretat.

### Serveis de xarxa d'un NOS:

Els serveis de xarxa són programes que s'executen de manera permanent als S.O. i que determinen què és el que es pot fer sobre el sistema.

- Seguretat. Polítiques de seguretat.
- Ús compartit de fitxers.
- Impressió.
- Correu electrònic i missatgeria.
- Web.
- Suports d'interoperabilitat per a connexions amb altres sistemes operatius.
- Serveis d'automatització de processos.

### Windows Server:

![image](https://github.com/XaSaFa/MP04/assets/110727546/40c274e7-8c18-4c6b-92ed-92bdf67d6c3b)

🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️

**Activitat:**

1.- Quines versions de Windows Server tenen suport actualment i quan acaben el seu suport.

2.- Característiques mínimes per utilitzar Windows Server 2016.

3.-Què significa Powershell?

4.- Quines versions de Windows Server 2016 existeixen? Explica les seves característiques.

🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️🕵🏼‍♂️
