# Elecció del hardware

Anem a instal·lar Ubuntu Desktop per tant hem de buscar els requisits de maquinari.

![image](https://github.com/XaSaFa/MP04/assets/110727546/c0916040-9d53-4510-8e1f-e9b7ea97222e)

Així al crear la MV les seves característiques seran:

- RAM: 4GB
- Disc Dur: 50GB
- CPUs: 2

- ![image](https://github.com/XaSaFa/MP04/assets/110727546/1a37568c-e270-4b83-a9a9-2b11ae5c34b9)

# Instal·lació Ubuntu Desktop

1. Triem Try or Install Ubuntu.

![image](https://github.com/XaSaFa/MP04/assets/110727546/0bf9f2fa-8eda-452a-b3e4-411b778f34bb)

2. Seleccionem l'idioma que volem i cliquem a Instal·lar Ubuntu.

![image](https://github.com/XaSaFa/MP04/assets/110727546/e7382f99-5b43-4fab-be26-e967c0cc172b)

3. Escollim la disposició del nostre teclat.

![image](https://github.com/XaSaFa/MP04/assets/110727546/823d8ca6-cc34-4381-a4d6-1ba6e3edf08d)

4. Escollim instal·lació mínima.

![image](https://github.com/XaSaFa/MP04/assets/110727546/7f1da4a9-372e-4c86-abff-20aa2581e465)

5. Escollim Més opcions per tal de poder crear particions.

![image](https://github.com/XaSaFa/MP04/assets/110727546/b50311ca-8f22-4832-b829-0b05425a5931)

6. Crearem una nova taula de particions.

![image](https://github.com/XaSaFa/MP04/assets/110727546/ae9d9b28-9e9a-459b-92e6-666fbc19d276)

Això ens deixa amb tot l'espai lliure.

![image](https://github.com/XaSaFa/MP04/assets/110727546/99db0c5f-d958-4802-8c70-a3199098b830)

7. Crearem les particions.

 - Partició boot:
   - Aquesta partició serveix per arrencar el SO i tindrà només 1MB.
 - Partició EFI per al sistema:
   - Aquesta partició serà de tipus EFI i servirà per els fitxers d'arrancada del SO.
   - Tindrà un tamany de 512MB.  
 - Intercanvi (Swap):
   - Aquesta partició servirà per que el sistema l'utilitzi si es queda sense RAM o volem hivernar el SO.
   - Si la memòria RAM és inferior a 4GB es recomana que la partició SWAP sigui del doble de la RAM, en cas contrari que sigui igual a la RAM.
   - Com hem assignat 4GB al SO, la SWAP partició serà de 8GB.
 - Home:
   - Aquesta partició contindrà els fitxers dels usuaris, això separa les dades d'usuari de les aplicacions i el kernel del sistema, facilitzant les còpies de seguretat i l'actualització del SO sense perdre la informació dels usuaris.
   - Deixarem 10GB per a dades d'usuaris.
 - Root:
   - L'arrel del SO on estarà el kernel del sistema i les aplicacions.
   - Aquesta partició tindrà el tamany que sobra.

![image](https://github.com/XaSaFa/MP04/assets/110727546/7735f11c-3001-4389-b058-a53797371d35)

![image](https://github.com/XaSaFa/MP04/assets/110727546/07bd7636-49a5-4806-a906-1794ce73f2df)

8. Escollim zona horària

![image](https://github.com/XaSaFa/MP04/assets/110727546/94bf4726-a66f-4b3e-a0c7-e5f3f1b2b6ed)

9. Creem un usuari administrador i donem nom a l'equip.

![image](https://github.com/XaSaFa/MP04/assets/110727546/87c27c61-5748-4053-a385-cd4d8615a5c4)

10. Reiniciem el SO.

![image](https://github.com/XaSaFa/MP04/assets/110727546/f7b1d732-a159-4e66-9420-77caa38e557c)

11. Ara podem actualitzar el SO o deixar-ho per a més endavant.
