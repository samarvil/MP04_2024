# Activitat Zentyal - Part 2

Tenim l'encàrreg d'implantar un sistema Zentyal per un hospital anomenat "Hospital Universitario Sanchinarro" que compta amb el següent organigrama:

![image](https://github.com/user-attachments/assets/9c16c267-d988-46ef-9d0a-f123cc83fa58)

Ens han proporcionat una llista de personal:

## Metges

- Dr. Javier Esteban Morales – Cardiologia
- Dra. Clara Jiménez Sanz – Neurologia
- Dr. Álvaro Torres Requena – Oncologia Mèdica
- Dra. Marta Lozano Benítez – Ginecologia i Obstetrícia
- Dr. Ignacio Ruiz Ortega – Traumatologia i Cirurgia Ortopèdica
- Dra. Teresa Valverde Muñoz – Dermatologia
- Dr. Miguel Ángel Cabrera Ríos – Urologia
- Dra. Elena Robles Martín – Psiquiatria
- Dr. Tomás Gil Navarro – Medicina Interna
- Dra. Ana María Delgado Ferrer – Pediatria
- Dr. Sergio Peña Cordero – Cirurgia General i Digestiva
- Dra. Lourdes Herrera Salgado – Endocrinologia i Nutrició
- Dr. Óscar Molina Vargas – Nefrologia
- Dra. Patricia Ramos Alarcón – Oftalmologia
- Dr. David Gómez Llamas – Reumatologia
- Dra. Silvia Casas Nogales – Medicina de Família
- Dr. Ricardo Doménech Vera – Otorrinolaringologia (ORL)
- Dra. Irene Pujol Casals – Hematologia
- Dr. Daniel Barrios Tejada – Anestesiologia i Reanimació
- Dra. Nuria Gallego Escribano – Cirurgia Plàstica, Estètica i Reparadora

## Infermeria

- Laura Sánchez Vidal | Infermeria de quiròfan
- Marc Pérez Gallardo | Infermeria d’UCI
- Júlia Gómez Alarcón | Infermeria de pediatria
- Nil Rodríguez Segura | Infermeria d’urgències
- Clàudia Navarro Rius | Infermeria d’hemodiàlisi
- Adrià Torres Mas | Infermeria de salut mental
- Helena Moreno Cañadas | Infermeria de geriatria
- Arnau Vidal Crespo | Infermeria d’atenció primària
- Paula Ruiz Domènech | Infermeria de neonatologia
- Daniel Soler Parra | Infermeria de medicina interna
- Marta Roca Benet | Infermeria d’oncologia
- Roger Cano Aranda | Infermeria de reanimació postquirúrgica
- Sara Molina Esteban | Infermeria comunitària
- Eric Ferrer López | Infermeria de control d’infeccions
- Aina Martí Rosell | Infermeria obstètrica
- Jan Gascón Oliva | Infermeria d’endoscòpies
- Clara Puig Font | Infermeria de cures pal·liatives
- Isaac León Bravo | Infermeria de salut laboral
- Eva Cortés Ibáñez | Infermeria anestèsica
- Oriol Ramos Fuster | Infermeria de trasplantaments

## IT

- Núria Ferrer Solà
- Joan Serra Pujol
- Laia Gómez Vidal
- Pau Riera Domènech

## Recursos humans

- Clara Batlle Miró
- Marc Lluch Casas
- Júlia Espinosa Grau
- Oriol Vidal Requena
- Gemma Prats Muntaner
- Albert Solsona Gil
- Irene Bosch Vallès
- Roger Martí Cuadras

## Administració

 - Lucía Álvarez Fernández
 - Iker Etxebarria Zubizarreta
 - Sofía Morales Medina
 - Raúl Sánchez Del Río
 - Aitana García Benítez
 - Manuel Romero Pacheco
 - Elena Costa Fontán
 - Carlos Jiménez Ortiz
 - Amira El Haddad Youssef
 - Luka Petrović Novak

# Creació de grups i usuaris

Per començar crearem els següents grups:

![image](https://github.com/user-attachments/assets/3f8cdf13-b36c-4b89-8d73-3dd73249dc99)

Després afegirem un parell d'usuaris a cada grup:

![image](https://github.com/user-attachments/assets/225d6a86-c3dd-4d5f-833b-c6d03075b941)

![image](https://github.com/user-attachments/assets/5588fe88-e4fe-44a6-b90f-bbb26f63d759)

# Creació de recurs compartit amb els membres del grup

Cada grup tindrà un recurs compartit diferent.

- Administració tindrà una carpeta accessible només per als seus membres que es dirà admin_files.
- Infermeria tindrà una carpeta anomenada docs_enfermeria.
- IT tindrà una carpeta anomenada IT_crow.
- Medicina tindrà una carpeta anomenada historiales_medicos.
- Recursos humanos tindrà una carpeta anomenada curriculums.

![image](https://github.com/user-attachments/assets/71154252-965d-4b55-a816-364d3ca425f0)

![image](https://github.com/user-attachments/assets/d3e34ec0-d3bc-41d9-87af-6e74e8a5cf3f)

![image](https://github.com/user-attachments/assets/0fdaa69c-f5a0-4879-bc70-3331d0879934)

I guardarem els canvis:

![image](https://github.com/user-attachments/assets/745cfd87-8d0b-4c7a-b353-874bfa2a0a13)
