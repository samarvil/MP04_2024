# Importació d'usuaris a Windows Server

De vegades voldrem crear usuaris a l'Active Directory de forma más ràpida que la introducció manual, per tal de fer-ho de forma menys feixuga tenim opcions com la importació per terminal.

Per a fer aquesta importació necessitem un fitxer de text que tindrà:
- Una línia amb els camps a importar.
- Una línia amb la informació per cada usuari.

## Exemple:

Tenim un domini anomenat MORDOR.COM, i dins del domini una UO anomenada CFGM que conté una altra UO anomenada SMX, com a la imatge:

![image](https://github.com/user-attachments/assets/9837b63d-f2c8-4b1c-aed6-1cdcaafe5029)

Per tal d'importar usuaris crearem un fitxer de text anomenat usuarios.csv i dins d'ell afegirem els camps necessaris i un usuari anomenat user1, el fitxer quedaria així:

![image](https://github.com/user-attachments/assets/175f210b-1d53-436b-8d21-baf10d8f601d)

Per tal de fer la importació anem a un terminal de Windows i escrivim la següent comanda:

```
csvde -i -f usuarios.csv
```

Aquesta comanda fa una importació del fitxer de forma que afegeix els usuaris del fitxer a AD.

![image](https://github.com/user-attachments/assets/da116757-3a7e-4f28-9f66-835bfc79ea83)

![image](https://github.com/user-attachments/assets/3b5139c5-97cf-4111-97e9-1ef9590a1bc9)

L'usuari importat estarà deshabilitat per defecte.

![image](https://github.com/user-attachments/assets/28da0e98-a5bb-469f-ac5f-671802a5d03d)
