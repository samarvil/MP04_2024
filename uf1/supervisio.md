# Supervisió de Windows Server

La supervisió del sistema és una de les tasques més importants dels administradors de sistemes.

L'administrador/a ha de vigilar:

- L'estat de la xarxa.
- L'ús correcte dels recursos del sistema
- L’estat dels serveis.
- L’espai físic dels sistemes d’emmagatzematge.
- Els problemes generats pel programari.
- L’ús que els usuaris fan del sistema.
- L’estat dels equips.

## L'administrador de tasques

![image](https://github.com/XaSaFa/MP04/assets/110727546/f43e9f88-ce38-4bcf-82c1-31c2eecaed61)

L'administrador de tasques permet controlar des d'una finestra l'estat de les aplicacions que s'estan executant, processos actius, memòria utilitzada o rendiment de l'equip.

L'administrador de tasques és l'eina principal per administrar processos i aplicacions del sistema.

Per accedir a l'administrador de tasques podem:

1. Utilitzar les tecles Control, Majúscules i Esc.
2. Utilitzar les tecles Control, Majúscules i Suprimir i escollir Iniciar el administrador.
3. Clicar a Inicio i escriure taskmgr en el quadre de text i clicar sobre Administrador de tareas.
4. Clicar amb el botó dret a la barra d'eines i seleccionar Administrador de tareas.

L'administrador de tasques té diferents pestanyes.

### PROCESSOS

![image](https://github.com/XaSaFa/MP04/assets/110727546/0511df52-a953-4eb3-a228-4df8350e7d0b)

La pestanya processos ens mostra informació referent a aplicacions i processos del sistema en execució.

La pestanya està dividida entre Aplicacions i processos.

Aplicacions ens mostra els programes que té iniciats l'usuari/a amb el % de CPU i memoria que està fent servir.

Processos ens mostra la mateixa informació sobre processos que estan en segon pla, normalment programes de sistema operatiu, però també de tercers que s'estan executant en segon pla.

### RENDIMENT

![image](https://github.com/XaSaFa/MP04/assets/110727546/e8ab746a-2416-4ed9-ad5d-0e4f1ccf0f2d)

Rendiment ens mostra de manera visual l´ús de la CPU, memòria, xarxa...

#### CPU

Mostra informació sobre el model de CPU, perxentatge d'ús, velocitat, nuclis, memoria cau (cache) de la CPU...

#### MEMORIA (RAM)

Mostra informació sobre quantitat de memoria instal·lada i % d'ús, així sabrem si podem executar més aplicacions.

#### ETHERNET (XARXA)

![image](https://github.com/XaSaFa/MP04/assets/110727546/3176d2bc-e93a-4f8d-96ef-2cd3bcc69be1)

Mostra tots els adaptadors que estigui utilitzant el sistema i veureu el % d'ús, velocitat de descàrrega i d'enviament.

#### Monitor de recursos

![image](https://github.com/XaSaFa/MP04/assets/110727546/dd321312-e648-473c-8338-8bae5be95223)

El monitor de recursos ens permet veure informació més detallada del maquinari de l'ordinador

#### USUARIS

![image](https://github.com/XaSaFa/MP04/assets/110727546/0f73bbe1-d169-4616-9e21-f7abc4975501)

Aquí podem veure els usuaris connectats, els processos que estan executant i el % de recursos que empra.

Podem desconnectar un usuari del server des d'aquí.

![image](https://github.com/XaSaFa/MP04/assets/110727546/33ad1a2d-dedb-4f75-8406-bf6d5898ed3a)

#### DETALLS

![image](https://github.com/XaSaFa/MP04/assets/110727546/4373a93d-e810-465e-9254-f81aea9156ba)

Aquesta pestanya és una continuació de la pestanya de processos amb més informació, com per exemple quin usuari està executant una tasca o el seu **PID** (Process IDentifier).

![image](https://github.com/XaSaFa/MP04/assets/110727546/108f6894-4073-4961-9cfc-a3268ad1aa69)

Sempre que volguem parar l'execució d'una tasca ho podem fer amb el botó dret del ratolí a sobre seu.

#### SERVEIS

![image](https://github.com/XaSaFa/MP04/assets/110727546/c777fa79-82f7-4f80-959b-c49531a37f1d)

Aquí podem veure informació dels serveis que executa l'ordinador, com el nom PID, descripció breu i estat.

Des d'aquí podem parar o pasar en marxa un servei, identificar el procés que té associat o obrir l'administrador de serveis.

#### Administrador de serveis

![image](https://github.com/XaSaFa/MP04/assets/110727546/5c090d28-3814-476d-891e-f47ff1bf76f7)

El plafó de serveis us mostra la informació següent:

- **Nom.** Identifica el servei mitjançant el nom. Per defecte, únicament hi apareixen els serveis que ja estan instal·lats.
- **Descripció.** Es descriu de manera breu i directa el servei donat.
- **Estat.** Mostra l’estat actual del servei. Els serveis poden estar funcionant, aturats o en pausa.
- **Tipus d’inici.** Indica com s’iniciaran els serveis, és a dir, de manera automàtica o manual.
- **Iniciar sessió com.** Marca el compte que s’utilitzarà en l’inici de sessió.

**Tipus d'inici**

- **Automàtic:** el servei es posarà en marxa quan s’iniciï el sistema operatiu.
- **Automàtic (inici retardat):** el servei es posarà en marxa quan s’iniciï el sistema i la resta de serveis automàtics (no retardats) s’hagin iniciat.
- **Manual:** el servei es posarà en marxa manualment.
- **Deshabilitat:** el servei restarà desactivat.

![image](https://github.com/XaSaFa/MP04/assets/110727546/9fe62105-2af4-4ed0-b39d-b880a418cba3)
