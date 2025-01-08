# Crear una unitat organitzativa:

Ho farem mitjançant un fitxer LDIF (LDAP Data Interchange Format).

## 1.- Editem un fitxer:

El fitxer es pot dir com vulguem, li direm uo per unitat organitzativa.

```
sudo nano uo.ldif
```

## 2.- Creem el contingut:

![image](https://github.com/XaSaFa/MP04/assets/110727546/708d4045-4862-47ac-b4c5-6be780c53e78)

L'objecte que em creat es diu "unidad", és a la part superior de la jerarquía i és una unitat organitzativa.

## 3.- Afegir la informació a la BBDD de LDAP:

Per afegir aquesta informació a la BBDD del directori ho fem mitjançant la instrucció:

```
sudo ldapadd -x -D cn=admin,dc=dungeonofbits,dc=com -W -f uo.ldif
```

Ens demana la contrasenya d'administració de LDAP.

![image](https://github.com/XaSaFa/MP04/assets/110727546/04ddc59e-d567-410f-a44b-3e27c7a21ee9)

## 4.- Comprovem que s'ha introduït:

Podem comprovar que hem introduït correctament les dades amb la comanda:

```
sudo slapcat
```

![image](https://github.com/XaSaFa/MP04/assets/110727546/04c48130-6adf-468d-9ddf-c74ef47e473a)

