# Xarxes a VirtualBox

Per modificar la xarxa d'una MV accedim a la configuració de xarxa **amb l'equip apagat**.

![image](https://github.com/user-attachments/assets/3991e331-e3d7-46f8-9588-23b7b6f0ec31)

Aquí podem afegir fins a 4 dispositius virtuals de xarxa com si tinguèssim 4 targetes de xarxa a l'ordinador virtual.

![image](https://github.com/user-attachments/assets/86f4553f-d197-4313-b690-4f87e16a8453)

Les opcions de cada targeta són aquestes:

![image](https://github.com/user-attachments/assets/ce74abd6-a7c3-4e93-9225-2056d43c43ad)

[Vídeo explicant les opcions de xarxa](https://www.youtube.com/watch?v=Fhdxk4bmJCs)

## Not connected

Vol dir que no hi ha dispositiu de xarxa, aquí no es pot configurar res.

## NAT

La MV pot accedir a Internet mitjançant Network Address Translation, però no té una IP accessible més enllà de VirtualBox i no es pot comunicar amb les altres MV (de fet totes tenen la mateixa IP).

**Funcionament:**

![image](https://github.com/user-attachments/assets/a6ed5128-5a4e-45de-8c84-5f6fc79da5a0)

## NAT NETWORK

Similar a NAT però les MV es poden comunicar ja que estan a la mateixa xarxa.

Per tal d'utilitzar Xarxa NAT hem de configurar la xarxa primer

![image](https://github.com/user-attachments/assets/1f063288-ef57-4f05-9f64-f9b82d59c9e8)

![image](https://github.com/user-attachments/assets/d2929ffc-2604-4452-b299-c39e461ee546)

**Funcionament:**

![image](https://github.com/user-attachments/assets/acb1f8b9-a666-4ed8-bf79-1f0125483b44)

## Internat NETWORK

Les MV només poden comunicar-se entre elles però no amb l'exterior.

![image](https://github.com/user-attachments/assets/a2382dae-0be3-4493-92e6-8fbab6482c3f)

## Bridged Adapter 

L'adaptador pont fa que la MV actui com si fos una màquina real connectada a la mateixa xarxa que l'ordinador real.

![image](https://github.com/user-attachments/assets/3d696609-8811-4c92-bc9b-d4877dac520c)
