# Activitats de Síntesi - Windows Server

Aquestes activitats tenen com a objectiu consolidar els coneixements adquirits sobre configuració de discos, còpies de seguretat, tasques programades i monitorització d’esdeveniments a Windows Server.
Crea un **github** on responguis cada activitat en un arxiu diferent. Comparteix l'enllaç del repositori a la tasca corresponent de Moodle.

## Activitat 1: Gestió Integral d'un Servidor per a Realitzar una Còpia de Seguretat amb Monitorització Automàtica

Configura un sistema complet de còpies de seguretat i monitorització automàtica en un Windows Server.

### Tasques
1. **Gestió de Disc**: 
   - Crea una partició dedicada per a les còpies de seguretat amb Diskpart.
   - Formata la partició i assigna-li una lletra d'unitat.

2. **Configuració de la Còpia de Seguretat**: 
   - Programa una tasca setmanal de còpia de seguretat que utilitzi la partició creada.

3. **Monitoratge d’Esdeveniments**: 
   - Configura el Visor d’Esdeveniments per enviar una alerta si la còpia de seguretat falla.

4. **Simulació i Prova**: 
   - Executa la còpia de seguretat manualment i verifica el funcionament de l’alerta.

### Resultats esperats
- Partició per a còpies de seguretat creada.
- Tasca de còpia de seguretat programada i funcional.
- Sistema de monitorització d’esdeveniments actiu amb alertes.

---

## Activitat 2: Automatització de Manteniment i Control del Sistema

Configura tasques programades per mantenir el rendiment del servidor i assegurar-ne el funcionament correcte.

### Tasques
1. **Tasques Programades per Manteniment**: 
   - Crea una tasca per netejar fitxers temporals i optimitzar el sistema.
   - Programa una tasca per reiniciar el servidor setmanalment.

2. **Monitoratge del Rendiment**: 
   - Configura el Monitor d’Esdeveniments per registrar l’ús de CPU, memòria i disc.

3. **Control de Serveis Crítics**: 
   - Assegura que serveis essencials es reinicien automàticament si s'aturen.

4. **Documentació del Procés**: 
   - Documenta les configuracions de manteniment i control del sistema implementades.

### Resultats esperats
- Tasques de manteniment programades.
- Alertes configurades per controlar l’ús de recursos.
- Documentació de la configuració d’automatització.

---

## Activitat 3: Simulació de Recuperació de Desastres amb Còpies de Seguretat i Restauració

Recupera dades perdudes utilitzant còpies de seguretat i configurar alertes per evitar futurs problemes.

### Tasques
1. **Simulació d’Error**: 
   - Simula una pèrdua de dades desconnectant un volum o provocant un error d’accés.

2. **Restauració des de la Còpia de Seguretat**: 
   - Restaura els fitxers perduts o el volum complet des de la còpia de seguretat.

3. **Documentació del Procés de Recuperació**: 
   - Redacta un informe detallant els passos de restauració i les opcions utilitzades.

4. **Configuració d’Alerta Preventiva**: 
   - Crea una alerta per evitar la repetició de l'error en el futur.

### Resultats esperats
- Recuperació completa de dades.
- Informe detallat del procés de restauració.
- Alerta configurada per prevenir problemes similars en el futur.
