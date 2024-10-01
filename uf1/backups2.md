# Fer còpies de seguretat a Windows Server

Per tal de fer còpies de seguretat a Windows Server anirem a l'administrador del servidor i després a Herramientas-> Copias de seguridad.

![image](https://github.com/XaSaFa/MP04/assets/110727546/03c616ee-40ef-45fb-ac7c-2f3e6e77dab2)

Si no surt la opció és que encarar no hem instal·lat la característica al sistema operatiu.

També ho podem fer directament amb la instrucció **wbadmin.msc**.

## Escollim còpia de seguretat local i **Hacer copia una vez**.

![image](https://github.com/XaSaFa/MP04/assets/110727546/ce218f57-3ab0-4c0d-bcc5-42f14a71ef8c)

![image](https://github.com/XaSaFa/MP04/assets/110727546/0ea58672-d927-4012-8ee4-e8e6bcfcfb56)

## Opcions de còpia de seguretat

### Tipus de còpia

Com encara no hi ha cap còpia de seguretat creada només podem escollir la segona opció **Opciones diferentes**.

![image](https://github.com/XaSaFa/MP04/assets/110727546/eae4ddfd-07aa-4da9-8c4d-92db5992e34d)

### De què fem la còpia

Aquí podem escollir si fer còpia sencera del servidor o només d'una part.

![image](https://github.com/XaSaFa/MP04/assets/110727546/dff5b7d9-ba44-47c4-a6df-0e476a33f191)

### Opció 1 - Còpia de servidor sencer

Necessitarem l'espai que ens indica Windows.

![image](https://github.com/XaSaFa/MP04/assets/110727546/ede629e2-a7d3-414a-b25d-5a52a3f7bd75)

#### Afegim un disc per a fer la còpia

Així que afegirem un disc per poder fer la còpia, a l'exemple he creat un disc de 16GB.

![image](https://github.com/XaSaFa/MP04/assets/110727546/65248efa-a168-46ca-9164-ffa083665ec0)

I crearem un volum que ocupi tot el disc en format NTFS.

![image](https://github.com/XaSaFa/MP04/assets/110727546/677e7a08-08d8-4b4b-9fd3-18a24cc21a6a)

![image](https://github.com/XaSaFa/MP04/assets/110727546/fe46f537-c0b3-4fc5-a215-893299a90a08)

Escollim una unitat local com a destinació de la còpia de seguretat:

![image](https://github.com/XaSaFa/MP04/assets/110727546/c3885401-6406-4765-8b19-c6ae87bf0821)

![image](https://github.com/XaSaFa/MP04/assets/110727546/c28f63aa-d248-4b71-9e90-f6c6a23020ce)

![image](https://github.com/XaSaFa/MP04/assets/110727546/6d14a672-21fb-40fd-824d-a8450a600a86)

![image](https://github.com/XaSaFa/MP04/assets/110727546/0e050ea8-c1f6-44ee-b69a-7aeb0ae72c23)

La còpia de seguretat està en progrés:

![image](https://github.com/XaSaFa/MP04/assets/110727546/83a1d085-e4d3-4c8b-aec1-63eb772bc69c)

Còpia finalitzada:

![image](https://github.com/XaSaFa/MP04/assets/110727546/00d520f1-ed02-4a48-96aa-87a9a3442123)

Informació de la còpia de seguretat:

![image](https://github.com/XaSaFa/MP04/assets/110727546/9ad64f6c-9d2e-4e47-8c07-75b04e44d81e)

Si anem a Este equipo veiem els fitxers de la còpia de seguretat:

![image](https://github.com/XaSaFa/MP04/assets/110727546/ef37efbe-26fb-4444-8887-986d09aee0fc)

### Opció 2 - Còpia personalitzada

![image](https://github.com/XaSaFa/MP04/assets/110727546/4e274332-444c-40ed-b81f-b3b95686d135)

![image](https://github.com/XaSaFa/MP04/assets/110727546/15d28573-7830-442f-b90e-8a58905b0680)

Seleccionem els elements a guardar:

![image](https://github.com/XaSaFa/MP04/assets/110727546/62be895b-2466-48ed-9bb2-67bfa27b42d4)

![image](https://github.com/XaSaFa/MP04/assets/110727546/2cedd494-69a1-4dbb-90ab-94bd9cc14c0d)

![image](https://github.com/XaSaFa/MP04/assets/110727546/281ffeab-9439-4cb1-93c6-f92761a067aa)

![image](https://github.com/XaSaFa/MP04/assets/110727546/a756bf79-db26-4073-a7e9-90850186a4c1)

![image](https://github.com/XaSaFa/MP04/assets/110727546/075700f5-4fe1-43d5-a622-fa03a8c8fd31)

Quan finalitza una còpia de seguretat ens indica com ha anat, per a poder recuperar-se la còpia de seguretat ha d'indicar que és **Correcta**.

![image](https://github.com/XaSaFa/MP04/assets/110727546/ba98ae74-8f2e-4df5-b17f-e89204bfbb36)

A detalls trobem els logs del sistema amb els errors que han pogut passar.

![image](https://github.com/XaSaFa/MP04/assets/110727546/1dc0e665-791f-4813-a912-f651f348c683)

![image](https://github.com/XaSaFa/MP04/assets/110727546/388d2bf8-c9ea-47ca-9bf4-60fb2b5021a6)
