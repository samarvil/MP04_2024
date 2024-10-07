# Visor d'esdeveniments (Visor de Eventos)

A Windows server cada vegada que hi ha una **incidència** de funcionament es crea un esdeveniment.

![image](https://github.com/XaSaFa/MP04/assets/110727546/6c264b48-0ff0-4a15-a9a6-c9c686f46f79)

La manera que té l'administrador de reconèixer aquestes incidències és utilitzant aquest visor d'esdeveniments "Visor de eventos" a Windows Server.

## Com accedir al Visor?

![image](https://github.com/XaSaFa/MP04/assets/110727546/a083968f-5570-47dc-93bd-4a6841446fb9)

El Visor d'esdeveniments el podem accedir mitjançant l'**administrador del servidor->Herramientas->Visor de eventos**.

Des de cmd es pot accedir amb la comanda **eventvwr.msc**.

## Què és el Visor d'events?

![image](https://github.com/XaSaFa/MP04/assets/110727546/e495645a-c963-4958-8794-2cbcc2215eb1)

El visor d'events és un visor dels fitxers de registre o log del sistema.

## Registres de Windows

![image](https://github.com/XaSaFa/MP04/assets/110727546/ca7c7321-06ee-4f9b-bc1d-32a693580896)

Aquí podem veure una sèrie d'events del SO.

**1. Aplicación.** Aquí queden els events de les aplicacions i serveis que no són del SO.
**2. Seguridad.** Events relatius a la seguretat del sistema.
**3. Instalación.** Eventos relatius a la configuració de rols i característiques.
**4. Sistema.** Events del sistema i dels components relacionats.
**5. Eventos reenviados.** Informació reenviada d'altres sistemes de la xarxa.

Per veure quins esdeveniments hi ha clickem a sobre d'una de les opcions, per exemple **Instalación**.

![image](https://github.com/XaSaFa/MP04/assets/110727546/bae04955-24ab-40ed-b9fd-30f76b96023f)

Aquí podem veure els registres que hi ha i de cadascun d'ells podem veure la data quan es va registrar, l'origen, un identificador de l'event...

A més si cliquem amb el botó dret sobre el nom dels camps mostrats es poden modificar les columnes que es veuen:

![image](https://github.com/XaSaFa/MP04/assets/110727546/f90d05fa-17d8-41e8-af76-30a3eaf9e3df)

### Detalls de l'event

Si cliquem sobre un event s'obrirà una finestra amb informació detallada.

![image](https://github.com/XaSaFa/MP04/assets/110727546/3dfd2bea-5bad-47ba-b2f1-013d0ff753d1)

## Crear vistes personalitzades d'events

Podem crear vistes personalitzades quan busquem un determinat tipus d'esdeveniments a l'hora de resoldre un problema.

![image](https://github.com/XaSaFa/MP04/assets/110727546/2386a9da-2b5d-4d36-9985-33c633a88043)

![image](https://github.com/XaSaFa/MP04/assets/110727546/db28c4e6-6c92-47a9-b543-4e5e687f1d61)

Aquí podem filtrar per:

1. Temps: Quan es va crear el registre de l'esdeveniment.
2. Nivell d'event (només si coneixem exactament què busquem).
3. Registre/Origen: Buscar per tipus d'events o per l'origen que ha provocat l'event.
4. Identificadors: Si coneixem el id. dels events podem escriure'ls aquí de la següent forma:
  - un id: 1.
  - més d'un id (separem per comes): 1, 3, 5.
  - interval: 1-5.
  - interval menys un id: 1-5, -3 ( seria igual que escriure 1,2,4,5).
5. Categoría de la tasca: Només si indiquem **orígenes del evento**.
6. Paraules clau: Relacionades amb l'esdeveniment.
7. Usuari: Podem escriure els usuaris que han provocat els esdeveniments.
8. Equips: Podem escriure a quins equips han passat els esdeveniments.

### Exemple

Anem a crear una vista personalitzada sobre l'event 4625 (Login fallit).

![image](https://github.com/XaSaFa/MP04/assets/110727546/02666ef1-afc7-4938-b58d-661559e4ee43)

En aquest cas veiem que només hi ha un intent fallit de login.

![image](https://github.com/XaSaFa/MP04/assets/110727546/45851ed5-0df1-4c05-8236-728082f1e54a)

## Exportar i importar Vistes personalitzades.

Les vistes personalitzades són filtres que es poden exportar en format XML amb l'opció **exportar vista personalizada**.

![image](https://github.com/XaSaFa/MP04/assets/110727546/3ad62097-ddb0-4067-b490-2a924d3f71a5)

Es poden importar amb l'opció **Importar vista personalizada**.

![image](https://github.com/XaSaFa/MP04/assets/110727546/a05c5366-6ae7-4f93-99f3-cb80e1f8818e)

## Programar una tasca quan es crea un esdeveniment

De vegades és interessant programar una tasca quan un esdeveniment succeeix, pot servir per avisar a l'administrador, per exemple.

Per programar una tasca primer hem de tenir una categoria d'esdeveniment o una vista personalitzada, després anem a l'opció **Adjuntar tarea a...**.

![image](https://github.com/XaSaFa/MP04/assets/110727546/63eb94b2-92c7-4694-8229-d3b75e9d3644)

![image](https://github.com/XaSaFa/MP04/assets/110727546/83ef2a46-9e2d-4014-b6bf-4ca382390c42)

![image](https://github.com/XaSaFa/MP04/assets/110727546/72f4aafe-c758-4905-942c-90be4995c928)

I li diem quin programa volem que s'executi.

![image](https://github.com/XaSaFa/MP04/assets/110727546/d9fe39fe-a255-4d68-986e-5cb4a823ce70)

![image](https://github.com/XaSaFa/MP04/assets/110727546/3126e0ba-6086-4c08-b7ca-fc5b17fbebfe)
