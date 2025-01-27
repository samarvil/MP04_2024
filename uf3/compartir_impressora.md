# Compartir impressora a un domini de Windows

# Configuració a la MV Windows Server:

## Pas 1. Instal·lar impressora

Anem a la web [https://download.pdfforge.org/download/pdfcreator/PDFCreator-stable](https://download.pdfforge.org/download/pdfcreator/PDFCreator-stable) des de windows server com usuari administrador.

Windows mostra un missatge d'advertència i afegim la web als llocs web de confiança:

![image](https://github.com/XaSaFa/MP04/assets/110727546/8cac6821-8d22-4a18-86ea-200673f23e90)

![image](https://github.com/XaSaFa/MP04/assets/110727546/bbaf3772-186c-4125-a4f4-6f1745f6605e)

**Repetim el pas amb els següents avisos**.

Descarreguem el fitxer i executem:

![image](https://github.com/XaSaFa/MP04/assets/110727546/d9336c7f-fd33-42b6-ab22-3b7863beaabc)

![image](https://github.com/XaSaFa/MP04/assets/110727546/9a96f4d5-3847-4724-b305-2ca1c7c6f48d)

![image](https://github.com/XaSaFa/MP04/assets/110727546/717c4f87-46c0-4083-998c-f0bcdcb15122)

![image](https://github.com/XaSaFa/MP04/assets/110727546/abbd8cc4-5b26-4a02-a32a-65c70847225f)

El programa ens convida a reiniciar l'equip.

![image](https://github.com/XaSaFa/MP04/assets/110727546/d2023206-dc51-42b4-b4cd-96f1c3777339)

Un cop reiniciat tornem a executar pdfcreator:

![image](https://github.com/XaSaFa/MP04/assets/110727546/350883ee-9dfe-4991-84ec-3cb38c79fbf9)

Aquí ja el veiem en funcionament:

![image](https://github.com/XaSaFa/MP04/assets/110727546/68eb700b-25d3-4fd7-a0d7-e3fa69fba1c6)

## Pas 2. Creau un grup d'impressió

Anem a usuaris:

![image](https://github.com/XaSaFa/MP04/assets/110727546/abd9d8f2-d64d-470c-8095-7f3efe9bd171)

Creem un grup anomenat "usuaris impressora".

![image](https://github.com/XaSaFa/MP04/assets/110727546/0d7f26ea-45b0-4c02-a1d8-cc9d59240c3e)

![image](https://github.com/XaSaFa/MP04/assets/110727546/cd5c0dff-54fc-43c1-9b99-ec4f90066d63)

Afegim algun usuari.

![image](https://github.com/XaSaFa/MP04/assets/110727546/7db9ae4c-25c5-48b0-b2de-31de02fa390b)

![image](https://github.com/XaSaFa/MP04/assets/110727546/b82ebe47-b349-448e-803a-c542a1f388e1)

![image](https://github.com/XaSaFa/MP04/assets/110727546/48fb26d6-a452-44a1-9765-8a4bd2edc2ef)

## Pas 3. Instal·lar rol administració d'impressió

![image](https://github.com/XaSaFa/MP04/assets/110727546/a9481c38-16e2-4d0b-9815-7437b892da49)

![image](https://github.com/XaSaFa/MP04/assets/110727546/be600e7e-919d-45f6-9d29-dcb3dd3c4a74)

![image](https://github.com/XaSaFa/MP04/assets/110727546/883109f1-48c0-4da3-8336-b6687822db39)

![image](https://github.com/XaSaFa/MP04/assets/110727546/d9921a2a-a9fe-4017-8b00-914b125576dc)

![image](https://github.com/XaSaFa/MP04/assets/110727546/4f9ed327-aade-4e3f-8a8d-5cd62c7725cb)

![image](https://github.com/XaSaFa/MP04/assets/110727546/e74bbaa2-2032-4c5f-a112-1f32a984b33f)

![image](https://github.com/XaSaFa/MP04/assets/110727546/385f74f7-16d5-499d-8ea1-c18d1a6ecf6b)

![image](https://github.com/XaSaFa/MP04/assets/110727546/29e94456-83e2-4e60-916c-fcfe7108822f)

![image](https://github.com/XaSaFa/MP04/assets/110727546/95a9643b-490c-46f8-83be-8a92c61bbd29)

![image](https://github.com/XaSaFa/MP04/assets/110727546/43225996-9b7e-4b1d-94c0-58bac4c1c0ac)

## Pas 4. Compartir impressora

![image](https://github.com/XaSaFa/MP04/assets/110727546/75dc47b8-ad0e-4576-a73c-55c53934ac78)

Escollim el nom del nostre servidor:

![image](https://github.com/XaSaFa/MP04/assets/110727546/6f215200-db51-4ac7-990f-586386ee210e)

**IMPORTANT**

Si tenim que instal·lar una impressora de veritat i no volem haver de portar els drivers a cada equip on hagio de funcionar la impressora seguim els següents passos:

A "controladores" fem click dret i escollim "Agregar controlador":

![image](https://github.com/XaSaFa/MP04/assets/110727546/360a3814-7ae3-4a5b-858e-c740b7f06a31)

![image](https://github.com/XaSaFa/MP04/assets/110727546/ca16c80c-2f50-401f-8b76-a846b453757d)

![image](https://github.com/XaSaFa/MP04/assets/110727546/cfd8cfd8-2c21-4c93-ab3a-4bf7185ac8a4)

I escollim la impressora que volem compartir.

![image](https://github.com/XaSaFa/MP04/assets/110727546/174b8440-7cf6-43df-8e30-015576ad9bba)

![image](https://github.com/XaSaFa/MP04/assets/110727546/caeb5bad-4d8c-444d-a410-aeecb01e7ce6)

![image](https://github.com/XaSaFa/MP04/assets/110727546/220bb8f6-9ed4-4926-8668-f6986cff8531)

![image](https://github.com/XaSaFa/MP04/assets/110727546/096544ba-8cec-45d0-a0b5-6bb7da1740b3)

![image](https://github.com/XaSaFa/MP04/assets/110727546/0463b93c-5051-44a4-bcfb-4b63dd769219)

Treiem Todos i afegim el grup usuaris d'impressora que havíem creat anteriorment:

![image](https://github.com/XaSaFa/MP04/assets/110727546/4829775e-d658-41c8-9a80-9eaaa18efe06)

![image](https://github.com/XaSaFa/MP04/assets/110727546/ce1869ce-3f1d-44cc-9165-ed7532be0d0d)

![image](https://github.com/XaSaFa/MP04/assets/110727546/558b28ff-bd47-4032-86f7-2198117ff2d6)

# Configuració a la MV Client Windows

## Pas 1. Iniciar sessió amb un usuari correcte

Hem d'iniciar sessió amb un usuari del grup usuaris d'impressió que hem creat abans.

## Pas 2. Panell de control

Obrim panell de control->Anem a "dispositivos e impresoras":

![image](https://github.com/XaSaFa/MP04/assets/110727546/a738a8f2-4cca-46c5-847c-54e7229dd269)

![image](https://github.com/XaSaFa/MP04/assets/110727546/af8deaa0-26d6-4b6e-8795-e2c4851f754a)

Ens sortiran les impressores disponibles:

![image](https://github.com/XaSaFa/MP04/assets/110727546/037c543f-b417-46c9-ba32-19c83706d494)

![image](https://github.com/XaSaFa/MP04/assets/110727546/64bba22f-4807-4a76-954b-fef1f6705d18)

Ens demana autorització d'un usuari administrador:

![image](https://github.com/XaSaFa/MP04/assets/110727546/bfc510d7-4fba-45fc-9ca4-c4872c3168b5)

![image](https://github.com/XaSaFa/MP04/assets/110727546/770bc735-7aa9-4018-a0ac-e4ae7c817f85)

![image](https://github.com/XaSaFa/MP04/assets/110727546/5c16ac6b-bbf8-4e2e-a244-0677ffadd9a7)

![image](https://github.com/XaSaFa/MP04/assets/110727546/a42295fd-f2d0-4036-ad77-2223cb3c8b7c)

![image](https://github.com/XaSaFa/MP04/assets/110727546/70e63285-ac4f-4d0c-ade4-0a4e0afae470)

![image](https://github.com/XaSaFa/MP04/assets/110727546/44566d62-c6a5-4eda-8c51-f6dcd6c8e175)
