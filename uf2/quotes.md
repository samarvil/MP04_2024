# Quotes de disc

![image](https://github.com/XaSaFa/MP04/assets/110727546/5603e8d2-5a76-44f7-a315-802cdba4ddb4)

Les quotes de disc serveixen per limitar l'espai que pot utilitzar un usuari del sistema.

Existeixen diferents tipus de limitacions:

- Podem limitar l'espai de blocs de disc, d'aquesta manera limitem l'espai màxim que es pot ocupar.
- Podem limitar els i-nodes, és a dir, el nombre d'objectes d'emmagatzematge (fitxers o directoris).

A més les limitacions poden ser rígides o flexibles:

- Les rígides (o hard) fan que el sistema operatiu impideixi que el límit es sobrepassi.
- Les flexibles (soft) fan que el sistema operatiu avisi quan es sobrepassin els límits.

## Instal·lar el servei de quotes

Instal·larem el servei de quotes orientat a limitra l'ús de disc al directori **home** dels usuaris.

Comencem per instal·lar els paquets per a gestionar quotes a Linux:

```
sudo apt install quota quotatool
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/7ecfcd08-eea2-48c4-bac5-5d8c97272b53)

Després hem d'indicar que utilitzarem quotes al directori /home editant el fitxer **/etc/fstab**

El canviarem de:

![image](https://github.com/XaSaFa/MP04/assets/110727546/fe054819-12f6-4106-af4b-d9e7c673f630)

a: 

![image](https://github.com/XaSaFa/MP04/assets/110727546/544d9a3d-3070-4498-8705-2b2679b137d0)

on usrquota indica que utilitzarem quota d'usuari i grpquota quota de grup.

**Després reiniciem el sistema**.

Executarem la comanda següent per crear els fitxers a /home anomenats **aquota.group  aquota.user**.

```
sudo quotacheck -gu /home
```

## Establir quota d'usuari

Amb la comanda següent assignarem quota de disc a un usuari concret.

```
sudo edquota -u nomUsuari
```

La instrucció per a les quotes de grup és:

```
sudo edquota -g nomGrup
```

Al executar la configuració de quotes per a un usuari anomenat lolo s'obre un editor de text com el següent:

![image](https://github.com/XaSaFa/MP04/assets/110727546/ba901745-bbb3-4a58-bf0c-9e1e1265845f)

Mostra la següent informació:

- Col 1: La partició del sistema d'arxius on està activada la quota.
- Col 2: Número de blocs que està utilitzant l'usuari en aquest moment.
- Col 3: Valor flexible de blocs a utilitzar per l'usuari.
- Col 4: Límit d'espai que pot utilitzar l'usuari.
- Col 5: i-nodes que està utilitzant l'usuari.
- Col 6 Límit flexible d'i-nodes que pot utilitzar l'usuari.
- Col 7: Límit d'i-nodes que no pot sobrepassar l'usuari.

Els límits flexibles es poden sobrepassar sobre el denominat **període de gràcia**, que és un temps que es pot modificar amb la instrucció següent:

```
sudo edquota -t
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/b13f8f91-ac0c-49a4-9848-5819a32c4f9a)

Quan canviem el periode de gràcia ho hem de fer en **anglès**: days, hours, minutes o seconds.

## Consultar les quotes

La comanda següent ens mostrarà l'estat de les quotes a /home:

```
sudo repquota /home
```

## Desactivar quotes

Amb la comanda següent podem desactivar les quotes a home:

sudo quotaoff /home

Aquesta comanda no serveix per anular quotes de forma definitiva ja que al reiniciar el sistema es tornen a activar les quotes.

## Reactivar quotes

Amb la comanda següent podem desactivar les quotes a home:

sudo quotaon /home

