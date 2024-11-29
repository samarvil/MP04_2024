# Monitoritzar Linux

![image](https://github.com/XaSaFa/MP04/assets/110727546/032697e9-bca3-4b8c-9182-17417d4911f6)

El monitoratge del sistema ens serveix per evitar caigudes de rendiment i tenir una alta disponibilitat del sistema.

Normalment es busca trobar si hi ha algun problema de rendiment a:

- Memòria.
- Processos.
- Emmagatzematge.
- Connexions de xarxa.

Hi ha una serie de comandes que ens serveixen per a fer-ho:

## free

La comanda free mostra la memòria RAM i d'intercanvi utilitzada.

![image](https://github.com/XaSaFa/MP04/assets/110727546/1bc81e36-c64a-4db7-98a5-8e587a10ef16)

## mpstat

Mostra informació de la càrrega de treball de la CPU.

![image](https://github.com/XaSaFa/MP04/assets/110727546/3e4dd455-d93a-4a3e-b589-a09b86d49dbd)

## top

La comanda top és una comanda que normalment va integrada a les distribucions Linux, ens mostra el grau d'ocupació de la CPU, la memòria RAM, la memòria d'intercanvi (SWAP) i els processos que s'estan executant.

![image](https://github.com/XaSaFa/MP04/assets/110727546/c1db49cf-f9a7-428c-9dcf-43dbe388d6f7)

### Estat del sistema

#### Informació

![image](https://github.com/XaSaFa/MP04/assets/110727546/383af85a-7967-4d72-b7b6-a9e7d7d3749c)

El primer número ens mostra el temps (la hora), up ens indica quan temps fa que està funcionant el SO i user és la quantitat d'usuaris connectats.

#### Memòria

![image](https://github.com/XaSaFa/MP04/assets/110727546/44b0e959-f737-43cd-a10b-fb13cf032eaf)

Aquest quadre ens indica la memòria del sistema: total, lliure, utilitzada i en búfer).

#### Processos

Els processos es mostren en aquesta secció:

![image](https://github.com/XaSaFa/MP04/assets/110727546/2a17fa22-f9a4-4585-bece-eb7f8acfe9a8)

Els processos running són els que estan en execució, sleeping són els que estan esperant una informació d'un procés d'entrada/sortida o un event per seguir executant-se.

Els processos stopped són processos que s'han aturat (per exemple amb un control+c), els processos zombie són processos fills que estan pendents de que el procés que els ha creat els recuperi en algun moment.

#### Estat dels processadors

L'estat dels processadors també es mostra amb top:

![image](https://github.com/XaSaFa/MP04/assets/110727546/e242d410-d601-4e24-bf18-bb5b348f722d)

us mostra el temps emprat amb processos dels usuaris, sy mostra temps emprat amb processos del sistema, ni és el valor "nice" que indica la prioritat de processos.

id (iddle) indica el temps que el processador està parat, wa (waiting) indica el temps que la CPU està parada esperant I/O entrada/sortida per completar un procés.

#### Load average

![image](https://github.com/XaSaFa/MP04/assets/110727546/e6b42bcc-70f4-411b-b93a-7d59d280e6f9)

Aquesta secció mostra l'estat de càrrega del sistema sobre un, 5 i 15 minuts.

Indica el temps que has d'esperar per a que un programa s'executi, quant més alt és el número més has d'esperar.

El número, per exemple 0.5, indica que el processador està al 50% de funcionament. Si estigués al 1.0 indica que va al 100% de càrrega, al 1.2 va al 120% i està deixant de fer processos...



### Ordenar processos

Si presionem h durant l'execució de top ens surten les opcions que té el programa, per exemple ens deixa ordenar els processos per la càrrega de CPU o la memòria que ocupen.

Hi i si indiquen el temps que el processador està gestionant operacions d'interrupció de hardware (hi) o de software (si).

St (steal) indica el temps que la CPU està esperant a executar un procés però no pot per què una màquina virtual està utilitzant-lo.



![image](https://github.com/XaSaFa/MP04/assets/110727546/3177575e-9a20-478f-ab26-67d2f16e17a0)

### Veure els processos d'un únic usuari

Dins de top puc utilitzar la lletra u per filtrar procesos d'un usuari concret.

Per exemple amb u xavi només mostrarà els processos de l'usuari xavi:

![image](https://github.com/XaSaFa/MP04/assets/110727546/45bc76d8-18f1-4e88-aa68-9d52dcb44b76)

Per tornar a veure tots els processos prenem la lletra u i enter.

Podem fer el mateix si per terminal introduïm la instrucció ``` top -u usuari ```

### Matar un procés

Si tinc un procés que vull parar, com el de l'exemple següent (Firefox), simplement he d'introduïr la lletra k (kill) i el número PID del procés, en aquest cas 3191.

![image](https://github.com/XaSaFa/MP04/assets/110727546/b534adaa-a7c7-41e6-88c9-b6c79d3bf429)

![image](https://github.com/XaSaFa/MP04/assets/110727546/439645bc-8885-42e8-9b4f-8b896c67b778)

Això envia una senyal al procés per a tancar-ho.

### Conèixer la ruta d'un procés

Si volem saber on està un fitxer que s'està executant podem utilitzar la lletra c.

![image](https://github.com/XaSaFa/MP04/assets/110727546/6fb840b2-bd07-40e5-8e25-dd202efa19ef)

## htop

Htop és molt semblant a top però amb un menú d'opcions.

![image](https://github.com/XaSaFa/MP04/assets/110727546/41b1bcf8-7b14-4c8a-a53b-7ee664bc3bfd)
