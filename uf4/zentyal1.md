# Configurar Zentyal com Controlador de domini

En aquesta pràctica tenim una MV amb Zentyal ja instal·lat i configurarem el servei de directori.

L'eina d'administració de Zentyal és via web a l'adreça _localhost:8443_

## 1.- Afegir components

Afegirem els components de Controlador de Domini i DNS.

![image](https://github.com/user-attachments/assets/11019a7a-3bde-49cb-a07e-002472633fd7)

![image](https://github.com/user-attachments/assets/79ccefe8-170b-411c-8ecb-04688add0318)

![image](https://github.com/user-attachments/assets/d9cda03f-973f-409b-b555-1a638ee2a7cf)

## 2.- Habilitar el mòdul de xarxa

Activem el mòdul de xarxa i configurem l'adreça de la tercera interfície de xarxa que és una xarxa privada de centre.

![image](https://github.com/user-attachments/assets/cd2b87c0-3ee4-4b50-ac46-12aca7551284)

![image](https://github.com/user-attachments/assets/6e283ab6-87b7-4c63-a952-3e33ca8ad7ec)

## 3.- Canviar el nom de domini

Canviarem el nom de domini, el vostre domini serà X.local on X és el vostre cognom, el nom del server serà el vostre nom.

![image](https://github.com/user-attachments/assets/932375c0-6314-4f64-841d-0f36ef40ddb5)

![image](https://github.com/user-attachments/assets/0b8848d8-4ea6-4ddb-ae18-0a3c6f102ec8)

## 4.- Habilitar el mòdul de controlador de domini

Habilitem el mòdul i a nom netbios ficarem el nostre cognom.

![image](https://github.com/user-attachments/assets/480d37ed-3e6c-42b4-a798-c08c0737abbb)

![image](https://github.com/user-attachments/assets/dbc8d8c7-0736-41e5-b9e5-fca941ea6198)

![image](https://github.com/user-attachments/assets/d9909296-a713-4df8-bd9d-c54ddbc74870)

## 5.- Canviar el password de l'usuari Administrator

L'usuari Administrator és l'administrador del domini, li ficarem una contrasenya vàlida a més d'un nom i cognom.

![image](https://github.com/user-attachments/assets/06845445-b404-44b0-8fd7-37bcf2a4ee43)

![image](https://github.com/user-attachments/assets/52fac4ad-a666-417b-bf78-ca4b8bc82f0d)

![image](https://github.com/user-attachments/assets/429dc026-b275-4060-a4aa-84a4671d6c9f)

![image](https://github.com/user-attachments/assets/99524869-81d4-432e-a2da-1ddcb5359a56)

# 6.- Afegir un usuari del domini

Afegim un usuari al domini per a provar-lo.

![image](https://github.com/user-attachments/assets/96ceb014-b259-42c1-a0d2-3bf16d49f0be)

![image](https://github.com/user-attachments/assets/30660a93-b309-4209-837e-4a38fe1cf7b4)


## 6.- Canviar la configuració del client Windows

A l'adaptador de xarxa de Windows fiquem una IP vàlida a la mateixa xarxa que el server i com a DNS la IP del server Zentyal.

A més unirem Windows al domini.

![image](https://github.com/user-attachments/assets/45372640-e69f-492c-a1ad-559b77c3e5e0)

![image](https://github.com/user-attachments/assets/520646d8-9323-48a9-948d-a58e56b4fadd)

![image](https://github.com/user-attachments/assets/659f1792-4e4f-4cce-9cc4-e6d4c8cf3634)

![image](https://github.com/user-attachments/assets/bf4b60d1-ff24-4729-8fa2-85a997ade7c4)

![image](https://github.com/user-attachments/assets/903325c7-6536-49de-a75d-44f26362c762)

![image](https://github.com/user-attachments/assets/3898002c-0d1a-415f-92d0-258f6fe79f40)

![image](https://github.com/user-attachments/assets/a9c09742-10c0-4a81-95c3-2c3bb41c7554)

![image](https://github.com/user-attachments/assets/19ca8c9d-515b-4c94-a5e8-86c537bbcbaa)


