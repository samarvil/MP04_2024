# Compartir una carpeta amb un grup d'usuaris

# Pas 1 - Creació del grup

Crearem un grup d'usuaris anomenat "enfermeria" que puguin tenir accés a la carpeta compartida.

![image](https://github.com/user-attachments/assets/c5e692fa-5c04-4f5c-95ca-ce8049a5f4c4)

![image](https://github.com/user-attachments/assets/6bb2c607-620e-4803-8407-23e266569736)

![image](https://github.com/user-attachments/assets/fe9067e2-f232-484f-9e79-4bd15244a415)

![image](https://github.com/user-attachments/assets/a4c32c28-06b0-4098-b0f5-3e773b9c554b)

![image](https://github.com/user-attachments/assets/fd1bdd86-d076-40bb-936d-60fda2064314)

# Pas 2 - Creació de la carpeta compartida

Creem la carpeta compartida anomenada "enfermeria" i li donem accés al grup anterior. 

![image](https://github.com/user-attachments/assets/60a5c444-4d7a-443b-97e9-4b99a9b78545)

![image](https://github.com/user-attachments/assets/8a5e1ae7-0eaf-4e6e-a603-f73bd98ef7eb)

![image](https://github.com/user-attachments/assets/43179fd2-c595-4b74-9cdf-b0e771bb2d2b)

![image](https://github.com/user-attachments/assets/6479f20a-ae91-43d1-be98-59875c269f3d)

# Pas 3 - Creació de Script connexió usuaris

Crearem un script (un fitxer amb extensió .bat) dins la carpeta NETLOGON del servidor.

![image](https://github.com/user-attachments/assets/6e342681-9da2-4184-b7d5-74db4d5f22a8)

![image](https://github.com/user-attachments/assets/74f1ff81-6877-44ab-9f1e-b528eb67e745)

![image](https://github.com/user-attachments/assets/1f96842e-a4cd-457b-97ae-593da359ca9a)

![image](https://github.com/user-attachments/assets/f156cb06-820a-4c9f-b066-065f08b6dbbb)

![image](https://github.com/user-attachments/assets/6bbd3dd5-6d05-44e0-a266-673cefae7db9)

![image](https://github.com/user-attachments/assets/8117a0ad-3f0a-4b5b-9db8-f29f56c48a2d)

![image](https://github.com/user-attachments/assets/0bc40282-1a41-4518-8ee0-beba46bca7d2)

# Pas 4 Afegir l'script a l'inici dels usuaris

Al perfil dels usuaris del grup direm que executin l'script anterior, d'aquesta manera quan iniciïn sessió a un ordinador de l'Active Directory automàticament s'executarà l'script que connecta la unitat de xarxa.

![image](https://github.com/user-attachments/assets/b7276ae6-c914-429c-a72c-2b1b69c93907)

![image](https://github.com/user-attachments/assets/15764f11-27d0-44e5-9fa4-b27a4c850bba)

![image](https://github.com/user-attachments/assets/2ddde777-d110-4ec4-99fe-0a004fdb21c6)

# Pas 5 Inicia sessió al client

Iniciem sessió a un ordinador client amb un usuari del grup amb l'script inicial anterior i comprovem que té accés a la unitat de xarxa. 

![image](https://github.com/user-attachments/assets/6103dd16-ba75-47bd-9c0f-c8c9d6b9f77b)
