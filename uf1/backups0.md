# Còpies de seguretat

![image](https://github.com/XaSaFa/MP04/assets/110727546/0d20cfad-e478-4370-b749-b129cf954f54)

Una de les coses més importants d'un sistema operatiu és tenir fiabilitat en la informació del sistema, per això és molt important que la informació estigui resguardada, una de les maneres de aconseguir-ho és fent còpies de seguretat o backups.

## Tipus de còpies de seguretat

![image](https://github.com/user-attachments/assets/7ed21236-d945-430e-a5fa-cb56c32e228c)

Hi ha tres maneres principals de plantejar les còpies de seguretat.

### Còpia completa

Com indica el seu nom aquest tipus de backup implica guardar TOTA la informació del servidor.

Aquesta còpia implica la despesa de molt temps de procés i molt espai d'emmagatzematge i pot ser una opció no viable per a moltes empreses.

### Còpia incremental

Aquest tipus de còpies de seguretat guarda la informació que ha canviat des de la última còpia de seguretat (del tipus que sigui).

Per exemple si fem una còpia de seguretat completa un diumenge i una incremental cada dia, per a recuperar les dades del dimarts haurem de recuperar la còpia de diumenge, aplicar els canvis de dilluns i els de dimarts.

El procés és bastant lent, si falla alguna de les còpies tindrem dades inexactes.

### Còpia diferencial

Aquest tipus de còpia de seguretat guarda la informació des de la última còpia completa creada, tota la informació.

És un tipus de còpia de seguretat que ocupa més que la incremental, però que és més ràpida de recuperar.

Per exemple, si fem una còpia total un diumenge i una diferencial cada dia, per recuperar les dades de dimarts haurem de recuperar les dades de la còpia completa i després les de la còpia de dimarts. 
