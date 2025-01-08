# Com funciona LDAP

LDAP es basa en entrades, on cada entrada és un conjunt d'atributs identificats per un nom global únic (dn - Distinguished Name) que serveix per identificar-la.

Les entrades s'organitzen de forma jeràrquica i lògica mitjançant un esquema de directori que conté la definició dels objectes que formen part del directori.

## Entrades

Cada entrada del directori representa un objecte.

Els objectes poden ser reals com persona o moble. També poden ser abstractes com una funció dins l'estructura de l'empresa.

Els objectes tindran atributs en forma atribut/valor. Els atributs poden ser:

- Atributs normals: Identifiquen l'objecte (nom, cognoms, etc.).
- Atributs operatius: Son atributs que utilitza el servidor per administrar el directori (data de creació, tamany, etc.).

Les entrades s'indexen mitjançant el nom complert (dn), que facilita la identificació singular a cada element de l'arbre. 
El nom complert es formarà amb una serie de pars atribut/valor, separats per comes, que reflexen la ruta des de la posició de l'objecte fins l'arrel de l'arbre.

Entre els atributs que poden emplear-se habitualment tenim els següents, tot i que poden haver molts més:

- uid (user id): Identificació única de l'entrada a l'arbre.
- objectClass: Indica el tipus d'objecte al que pertany l'entrada.
- cn (common name): Nom de la persona representada per l'objecte.
- givenname: Nom de pila.
- sn (surname): Cognom de la persona.
- o (organization): Entitat a la que pertany la persona.
- u (organizational unit): El departament on treballa la persona.
- mail: direcció de correu electrònic de la persona.

Aquests atributs són propis d'una persona, per a altres objectes poden canviar.

Exemple d'entrada de persona:

|   |
|---|
| dn: uid=jraynor, ou=terrans, dc=starcraft, dc=com 
objectClass: person
cn: Jim
givenname: Jim
sn: Raynor
o: starcraft
u: terrans
mail: jraynor@starcraft.com|

## Jerarquia

Les entrades estan organitzades jeràrquicament, amb una estructura en forma d'arbre.

![LDAPExemple](https://github.com/user-attachments/assets/4a9a5172-a73b-4202-adef-ffc0c153fce1)


Les implementacions actuals de LDAP utilitzen DNS per a les capes superiors de la jerarquia.

L'atribut objectClass especifica quins atributs són vàlids i imprescindibles per cada tipus d'objectes.

[Tipus d'objectes](https://www.zytrax.com/books/ldap/ape/)

LDAP té comandes per crear, modificar i eliminar entrades del directori.


