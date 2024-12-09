# Programar tasques a Linux

![image](https://github.com/XaSaFa/MP04/assets/110727546/ff8ddfe4-f2ff-4050-8175-8398974e963c)

A Linux normalment s'utilitza el programa **cron** per programar tasques, aquest programa consta del dimoni crond i uns fitxers de configuració.

En principi cron s'inicialitza amb el sistema operatiu i s'activa cada minut per comprovar si hi ha tasques per executar.

## Crear una tasca

Per a crear una tasca utilitzarem la comanda crontab amb l'argument -e.

```
crontab -e
```

La primera vegada que el fem servir ens farà escollir un editor de textos:

![image](https://github.com/XaSaFa/MP04/assets/110727546/00d018b7-161e-4185-848d-5bbe530efcf3)

En aquest cas jo faré servir nano i em sortirà aquest fitxer de text:

![image](https://github.com/XaSaFa/MP04/assets/110727546/0ee5329e-09ec-49de-901d-131780e738f1)

Les següents vegades que fem servir la comanda farà servir el mateix editor de text, si alguna vegada volem canviar l'editor podem utilitzar la comanda:

```
sudo update-alternatives --config editor
```

El fitxer de text ens permet introduïr línies amb les tasques que volem programar, **CADA LÍNIA ÉS UNA TASCA**.

Les línies es composen de sis dades:

1. Minut: entre 0 i 59.
2. Hora: entre 0 i 23.
3. Dia del mes: Entre 1 i 31.
4. Mes de l'any: Entre 1 i 12.
5. Dia de la setmana: Pot escriure's de dues formes:
  - Valor entre 0 i 7: 0 i 7 = diumenge, 1 = dilluns, 2 = dimarts...
  - Valors en text: sun, mon, tue, wed, thu, fri i sat.    
6. Ordre a executar-se al shell: Qualsevol cosa entre el dia de la setmana i el final de la línia s'envia a la shell, si hi ha un símbol de percentatge % es talla la línia, així que si hem d'enviar un símbol de percentatge haurem d'escriure'l amb un caràcter de barra inversa davant (\%).

Els primers 5 valors es poden expressar com:

- Valors individuals: Per exemple minut 5 -> 5.
- Rang de valors: Per exemple minuts 5 a 10 -> 5-10.
- Llista de valors: Separats per comes, per exemple minuts 1,3 i 5: -> 1,3,5.
- Tots els valors possibles: Un asterisc -> *.

Exemple: Programem l'apagat diari de l'ordinador a les 20:15.

| Minut | Hora | Dia del mes | Mes | Dia de setmana | Ordre |
|----------|----------|----------|----------|----------|----------|
| 15    | 20   | *   | *    | *   | /sbin/poweroff   |

![image](https://github.com/XaSaFa/MP04/assets/110727546/e158755f-c9ef-486a-b5c1-cbf2f87c13fe)

Quan guardem el fitxer el sistema comprova que sigui correcte, si es així es guardarà dins la carpeta **/var/spool/cron/crontabs** a un fitxer amb el nom de l'usuari.

![image](https://github.com/XaSaFa/MP04/assets/110727546/3fa0de89-9980-4cb9-a954-46a51a268e24)


## Observacions

- Si una tasca s'ha d'executar però l¡ordinador està apagat LA TASCA NO S'EXECUTARÀ.
- Es recomana ficar sempre la ruta sencera de la comanda per si no estigués disponible a la variable $PATH.
- La comanda s'executarà amb els privilegis del compte d'usuari que l'ha creat, si ha de tenir privilegis de root per executar-se i no els té... No s'executarà.


## Eliminar tasques 

Per eliminar les tasuqes programades podem executar crontab -e i editar totes les tasques.

Si el que volem és eliminar totes les tasques programades utilitzem la comanda:

```
crontab -r
```

Tenint en compte que si hem utilitzat sudo per crear una tasca també haurem d'utilitzar sudo al esborrar-la.

## Consultar les tasques

Per consultar les tasques fem servir la comanda:

```
crontab -l
```

Tenint en compte que si hem utilitzat sudo per crear una tasca també haurem d'utilitzar sudo al consultar-la.

## Comanda crontab d'altre usuari

Podem crear tasques, consultar-les i eliminar-les per a qualsevol usuari del sistema utilitzant el paràmetre -u seguit del nom d'usuari.

Per exemple si vull llistar les tasques d'un usuari anomenat kerrigan utilitzaré la comanda:

```
sudo crontab -u kerrigan -l
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/b25c1def-f74d-4c8d-a6b0-9def2128f2d0)

## Permetre o denegar cron a usuaris

Per defecte tots els usuaris del sistema poden programar tasques, si volem que això no sigui així podem crear dos fitxers:

### /etc/cron.deny

Tots els usuaris que no volem que puguin programar tasques els escriurem dins d'aquest fitxer, un usuari per línia, per exemple:

![image](https://github.com/XaSaFa/MP04/assets/110727546/7cc67f43-4e2b-4d5d-a5c4-73168574c919)

I comprovem que l'usuari kerrigan ja no podrà programar tasques:

![image](https://github.com/XaSaFa/MP04/assets/110727546/f46ba791-16be-42a3-b8f1-20793fd990e2)

### /etc/cron.allow

Si creem aquest fitxer només els usuaris que estiguin escrits en ell podran programar tasques.

🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎

**Activitat:**

1. Fes una tasca programada que faci un reinici de l'equip (reboot) els dilluns i dimarts a les 12:45.
2. Fes una tasca programada que faci una còpia de seguretat d'una carpeta (amb pocs fitxers) d'un usuari a un fitxer anomenat backup.bak de la carpeta /tmp els dies 1 i 15 de cada mes a les 15:45.
3. Fes una tasca que obri firefox el dia 1 de gener a les 12:11.
4. consulta les tasques.
5. Elimina les tasques.

🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎🔎



