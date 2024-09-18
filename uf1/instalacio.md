# Instal·lació de Windows Server

## Requisits mínims:

A l'hora d'instal·lar Windows Server em de mirar els requisits mínims del maquinari on s'ha d'instal·lar:

![image](https://github.com/XaSaFa/MP04/assets/110727546/07e156c0-5768-4053-9d22-79b9e10b1257)

## Tipus d'instal·lació:

![image](https://github.com/XaSaFa/MP04/assets/110727546/b7d71b39-b933-4693-a85b-2eb2cb8ef7a6)

El tipus d'instal·lació poty ser:

- **Sense experiència d’escriptori.** Aquesta opció omet la major part de l’escriptori gràfic de Windows. L’administració es porta a terme amb el símbol del sistema, amb el PowerShell o de forma remota. Aquesta opció és interessant per estalviar els recursos gràfics.
- **Amb experiència d’escriptori.** Aquesta opció instal·la l’entorn gràfic de Windows, consumint els recursos corresponents. És interessant si es vol fer ús de l’escriptori de Windows, o es vol aprendre el funcionament.

Quan ja sabem el tipus d'instal·lació escollim entre:

- **Instal·lació des de zero.** El sistema operatiu que hi hagi a l’equip se substituirà completament, de manera que les configuracions i les aplicacions es perdran. També és l’opció a triar si teniu un disc dur sense sistema operatiu.
- **Actualització.** En aquest cas, el sistema operatiu s’instal·la i es fa una migració de les configuracions, els documents i les aplicacions que els usuaris tenien instal·lats en la versió anterior del Microsoft Windows.

### Procés d'instal·lació des de zero

Per instal·lar el Microsoft Windows Server des de zero, podeu veure el vídeo amb l’instal·lació de Windows Server 2019 o seguir els passos següents:

- Comenceu el procés d’instal·lació arrancant l’equip amb l’USB bootejat amb l’ISO, o amb el DVD d’instal·lació del Microsoft Windows Server 2019.
- Seleccioneu l’idioma.
- Cliqueu a Instalar ahora.
- Decidiu quina versió necessiteu instal·lar (en mode text o amb experiència d’escriptori, i Standard o Datacenter).
- Si esteu d’acord amb els termes de la llicència, accepteu-los.
- Seleccioneu el tipus d’instal·lació que voleu fer: per instal·lar des de zero, trieu Personalizada: instalar solo Windows (avanzado).
- Indiqueu on voleu fer la instal·lació.
- A partir d’aquí, s’inicia la còpia de fitxers des de la imatge del disc.

[Vídeo d'instal·lació](https://player.vimeo.com/video/745716866)

### Procés d'actualització

Si us cal fer una actualització des d’un Windows Server anterior fins al Windows Server 2019, i migrar la configuració d’usuaris, documents i aplicacions de la versió anterior del Windows, la solució és fer una actualització. Per actualitzar el sistema operatiu actual en el Microsoft Windows Server 2019 convindria que seguíssiu els passos següents:

- Inicieu una sessió de Microsoft Windows amb permisos d’administrador.
- Executeu l’ISO o introduïu el DVD amb l’instal·lador del Microsoft Windows Server 2019.
- Si no arranca automàticament, executeu el fitxer que hi ha en el DVD que porta l’etiqueta Setup i l’extensió exe.
- Cliqueu a Instalar ahora.
- Si necessiteu obtenir actualitzacions per mitjà d’Internet, ara ho podreu indicar.
- Decidiu quina versió necessiteu instal·lar (en mode text o amb experiència d’escriptori, i Standard o Datacenter).
- Si esteu d’acord amb els termes de la llicència, accepteu-los.
- Seleccioneu el tipus d’instal·lació a Actualización.
- Després de copiar la imatge del disc s’instal·laran les característiques que depenguin de la configuració i el maquinari detectats en l’equip.
