# Crear el recurs compartit

El recurs compartit serà una carpeta del servidor anomenada /shared i que, com es veu, farem a l'arrel del sistema.

# Pas 1.- Crear la carpeta

```
sudo mkdir /shared
sudo chown nobody:nogroup /shared
sudo chmod -R 777 /shared     
```


quedarà a l'arrel / això:

![image](https://github.com/XaSaFa/MP04/assets/110727546/aabe4d7d-e88d-45b8-9f77-165b561f17d9)

# Pas 2.- Exportar el contingut de la carpeta

En NFS compartir equival a exportar, per això haurem d'editar el fitxer **/etc/exports**

Cada carpeta exportada s'ha d'escriure en una línia diferent del fitxer.

El format de línia serà:

**ruta client_1(opcions) client_2(opcions)...**

És **important** no ficar espais entre client i opcions, només entre ruta i client1 i entre els diferents clients.

## Nom del client:

Per a descriure el nom de client podem utilitzar:

- La seva IP o un nom DNS.
- Caràcters comodí per representar el nom sencer del client o una part com:
  -  '?' - Per representar un únic caràcter qualsevol.
  -  '*' - Per representar un conjunt de caràcters qualsevols.
- Intervals d'adreces IP: Per exemple 192.168.1.0/30 permet l'accés a les 30 primeres adreces de la xarxa 192.168.1.0 començant per 192.168.1.0.
- Netgropus - Si dispossem d'un servidor NIS.

## Opcions:

Les opcions de cada client són independents i es refereixen a com es comparteix el recurs.

- ro (read-only): La carpeta compartida és de lectura només. És l'opció predeterminada.
- rw (read-write): L'usuari podrà modificar els continguts de la carpeta.
- wdelay: El servidor NFS no escriu a disc si espera una altra sol·licitud imminent. És l'opció predeterminada però només funciona quan utilitzem l'opció sync.
- no_wdelay: Deshabilita la característica anterior.
- root_squash: Evita que els ususaris amb privilegis administratius els mantinguin sobre la carpeta compartida quan es connecten remotament. Quan això ocurreix es comporten com un usuari remot més. És l'opció predeterminada.
- no_root_squash: Deshabilita la característica anterior.
- sync: Evita respondre peticions abans d'escriure els canvis pendents a disc. És l'opció predeterminada.
- async: Deshabilita la característica anterior. Millora el rendiment però pot provocar corrupció en fitxers i/o disc en cas de bloqueig o parada del sistema.
- subtree_check: Quan el directori compartit és un subdirectori d'un sistema superior, NFS comprova els directoris superiors per verificar els permisos i característiques. És l'opció predeterminada.
- no_subtree_check: Deshabilita la característica anterior, redueix la seguretat però augmenta la velocitat de transmisió d'arxius.

En el nostre cas utilitzarem aquestes opcions:

/shared *(rw,sync,no_subtree_check)

I el fitxer quedarà així:

![image](https://github.com/XaSaFa/MP04/assets/110727546/0473d086-5d37-4c2b-a772-201dd7dc9ad3)

# Pas 3.- Reiniciar el servidor NFS

Un cop fets els canvis hem de reiniciar el servidor NFS:

```
sudo service nfs-kernel-server restart
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/eaf73264-9f63-46e3-bf69-840eba799012)

# Pas 4.- Creem algun fitxer a la carpeta compartida

Per comprovar que podem accedir a la carpeta compartida i el seu contingut anem a crear un fitxer de text dincs de /shared

```
cd /shared
touch hola.txt
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/d96bebdd-3187-4ad1-80a0-1707b6410134)

