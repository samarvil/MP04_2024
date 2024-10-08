# Monitor de rendiment

El monitor de rendiment és una eina per controlar la velocitat a la que el sistema executa les tasques que té assignades.

Ens dona una serie de facilitats per comprovar-ho.

## Executar el monitor de rendiment

Per executar el monitor de rendiment podem escriure **perfmon.msc** al prompt de Windows o anar a **Administrador del servidor->Herramientas->Monitor de rendimiento**.

![image](https://github.com/XaSaFa/MP04/assets/110727546/f89c58da-fc68-4d0c-8403-e19a0968d0b0)

El monitor ens dona informació de l'activitat del nostre sistema, principalment ús de disc, xarxa, memòria i CPU.

## Monitoritzar el sistema

Per defecte només veiem el % d'ús del processador

![image](https://github.com/XaSaFa/MP04/assets/110727546/54b5a6ce-ee8b-4bc0-9529-b3f55e58e3d8)

Però podem afegir més informació, això es fa amb la opció Agregar contadores, per exemple anem a afegir la informació de % d'ús de memòria.

![image](https://github.com/XaSaFa/MP04/assets/110727546/85bb4410-b242-4d30-933e-73f1b8a48118)

![image](https://github.com/XaSaFa/MP04/assets/110727546/b011e122-4987-473d-b034-bf569e7b989f)

Ara veurem les dues informacions:

![image](https://github.com/XaSaFa/MP04/assets/110727546/68b59f8d-ae8a-4cf0-a6b3-93729d7ef022)

## Personalitzar la vista

Podem canviar la vista a gràfic de línies, de barres i informació en text.

![image](https://github.com/XaSaFa/MP04/assets/110727546/a8fe1127-ff51-4712-810e-7ac128b201e8)

![image](https://github.com/XaSaFa/MP04/assets/110727546/a7585cf1-45e0-493e-8b4b-8084e18a0bfc)

![image](https://github.com/XaSaFa/MP04/assets/110727546/c01b06fd-38ee-4a6c-8512-d2ad2dc44535)

## Personalitzar colors

Podem canviar els colors dels valors a pantalla, per això farem click dret sobre el nom del valor a la part inferior de pantalla i cliquem sobre propietats.

![image](https://github.com/XaSaFa/MP04/assets/110727546/1576c337-f7f6-45d8-96da-b401639e2ce6)

O tenim un botó de propietats també:

![image](https://github.com/XaSaFa/MP04/assets/110727546/46c25076-9567-4a12-8fff-6b8c339abb07)

Aquí podem personalitzar com es veu cada valor

![image](https://github.com/XaSaFa/MP04/assets/110727546/2844bf9a-a53e-421e-b5c2-02c7f71f05d9)

![image](https://github.com/XaSaFa/MP04/assets/110727546/f4e476cb-57c8-4b97-8ac2-774dd93ea43b)

## Pausar el gràfic

Si necessitem observar els valors detingudament podem parar el gràfic amb el botó de pausa.

![image](https://github.com/XaSaFa/MP04/assets/110727546/1fb99be6-2a13-45d5-955c-faad332e2830)

# **Activitat de classe:**

Afegiu els següents contadors amb vista de **barres**:

- % ús de memòria (color vermell)
- % ús de processador per part de l'usuari (color blau).
- % temps de lectura de disc (color taronja).
- % temps d'escriptura de disc (color verd).
- Interfície de xarxa bytes enviats (color marró).
- Interfície de xarxa bytes rebuts (color groc).

Feu operacions que facin servir el disc, la xarxa, la memòria i el processador per veure els canvis al monitor.

Per a la xarxa podeu instal·lar EDGE anant des de Windows Server a [https://www.microsoft.com/es-es/edge/business](https://www.microsoft.com/es-es/edge/business)
