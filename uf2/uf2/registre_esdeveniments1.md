# Registre d'esdeveniments

A Linux tots els processos que registren informació ho fan al directori **/var/log** en forma de fitxers.

Aquests fitxers contenen informació amb el següent format:

- Data del succés.
- Hora.
- Nom de l'equip on s'ha produït.
- Programa o servei que ha originat el succés.
- Opcionalment pot aparèixer el PID del procés.
- Missatge infotmatiu que descriu el succés.

Els fitxers normalment són molt extensos, així que pot ser interessant buscar només els últims (amb tail) o específicament els que volem (amb cat i grep).

Exemple:

Si només volem veure les últimes 10 línies d'un fitxer utilitzem ```tail -f nomFitxer```.

Si només volem buscar línies amb un text determinat utilitzem ```cat nomFitxer | grep textABuscar```.

## Veure els registres per terminal

Els registres de sistema són al directori /var/log

Per exemple el fitxer auth.log tindrà els intents d'inici de sessió o autoritzacions de comandes com usuari root.

Podem observar totes les operacions que es van fent amb la següent comanda:

![image](https://github.com/XaSaFa/MP04/assets/110727546/3d18f1c3-d797-456d-943b-d33024920b8d)

Proveu a iniciar sessió a un altre terminal mentre funciona la comanda per veure en viu els intents d'accés.

```sudo tail -f /var/log/auth.log```

Podeu mirar els esdeveniments de sistema mirant e fitxer /var/log/syslog.

![image](https://github.com/XaSaFa/MP04/assets/110727546/4512601b-1838-4480-9243-8d9ea6adec36)

```sudo tail -f -n4 /var/log/syslog```

Podeu buscar paraules clau al fitxer:

![image](https://github.com/XaSaFa/MP04/assets/110727546/6e401eac-3ca2-4bf1-85d7-45353fb8d357)

```sudo tail /var/log/syslog | grep firefox```

## Escriure un registre amb logger

Linux té una instrucció anomenada logger que permet crear registres a /var/log/syslog per terminal, com a l'exemple següent:

![image](https://github.com/XaSaFa/MP04/assets/110727546/eb577230-4fca-4f1f-a194-c352d2b840e8)

## Mostrar missatges de sistema amb dmesg

A Linux també existeix la comanda **dmesg** que mostra informació del sistema.

La comanda mostra informació d'aquestes categories:

- emerg: The system is unusable.
- alert: Action must be taken immediately.
- crit: Critical conditions.
- err: Error conditions.
- warn: Warning conditions.
- notice: Normal but significant condition.
- info: Informational.
- debug: Debug-level messages.

![image](https://github.com/XaSaFa/MP04/assets/110727546/11c89a3a-b984-4ea8-b8b3-8eb9a878585b)

## Veure els registres en entorn gràfic

Podem veure els registres del sistema des de l'entorn gràfic, l'aplicació es diu "registres".

![image](https://github.com/XaSaFa/MP04/assets/110727546/e09e1ac1-9794-4d7f-aa92-42819d367790)

Es poden veure els registres de diferents apartats:

![image](https://github.com/XaSaFa/MP04/assets/110727546/a2f3cfe1-2ce5-45b3-a3dd-8c43cdf96231)

Per exemple a seguretat veurem els inicis de sessió.

![image](https://github.com/XaSaFa/MP04/assets/110727546/41322e7a-ca4b-4f62-8d17-03eb0eb9578a)

Fem un status del servei ssh i queda registrat a Aplicacions...

![image](https://github.com/XaSaFa/MP04/assets/110727546/c053d84e-88c1-49bd-bf21-8b90ebfdc32c)

Dins de registres podem cercar per mots.

![image](https://github.com/XaSaFa/MP04/assets/110727546/b3cf0f20-5386-4b33-b351-7357b54c5e6e)

També podem exportar els registres a un fitxer de text:

![image](https://github.com/XaSaFa/MP04/assets/110727546/f950edf3-3c20-4ec8-ade9-ab6a21972410)

