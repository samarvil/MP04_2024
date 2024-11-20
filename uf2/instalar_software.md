# Instal·lar software a Ubuntu per terminal

![image](https://github.com/XaSaFa/MP04/assets/110727546/ad80faea-e8c9-433c-bb09-bdaad8b778b5)

## Repositoris

Ubuntu utilitza un sistema de repositoris de software per tal de poder amplicar les seves funcionalitats, és a dir, instal·lar software.

Un repositori de Linux és un lloc confiable que conté paquets de software que es poden instal·lar al nostre sistema operatiu.

## Instal·lar paquets

Ubuntu ens permet gestionar les instal·lacions de paquets amb apt i apt-get, apt és més moderm que apt-get.

Aquestes comandes són interfícies per gestionar paquets, APT significa (Advanced Package Tool).

A nivell d'usuari potser és més amigable apt que apt-get.

Per tal d'instal·lar un paquet del repositori oficial utilitzem la comanda apt install, per exemple per instal·lar 

![image](https://github.com/XaSaFa/MP04/assets/110727546/e22c9a97-e5e5-4552-a669-fca393146dd0)

## Buscar paquets

Si no estem segurs del nom d'un paquet a instal·lar podem fer servir la comanda apt search.

![image](https://github.com/XaSaFa/MP04/assets/110727546/087986df-abf9-4bc6-9c7e-221c937fed3e)

## Actualitzar repositoris

Per tenir els repositoris actualitzats a les últimes versions utilitzem la comanda apt update.

![image](https://github.com/XaSaFa/MP04/assets/110727546/3dba0fa2-33a5-4fef-ac7e-49cb1e6b60f3)

## Mostrar paquets que es poden actualitzar

Si volem tenir un llistat dels paquets instal·lats dels quals hi ha versions més modernes als repositoris escrivim la comanda  sudo apt list --upgradable.

![image](https://github.com/XaSaFa/MP04/assets/110727546/5a7c0e10-3953-473a-92cf-30d036534301)

## Desinstal·lar paquests

Quan volem desinstal·lar un paquet utilitzem la comanda apt remove.

![image](https://github.com/XaSaFa/MP04/assets/110727546/3a8cf4d9-3f89-4727-a184-d99f02e4b73d)

Normalment després volem esborrar els fitxers que no s'utilitzaran més amb apt purge i apt autoremove.

![image](https://github.com/XaSaFa/MP04/assets/110727546/c3294161-686c-4d24-ba4b-9839a83a808a)

## Instal·lar les últimes versions del software del sistema

Hi ha una comanda que busca els paquets instal·lats i els actualitza a la última versió que hi ha al repositori, aquesta comanda no es recomana per què de vegades volem tenir versions específiques dels programes.

La comanda és apt upgrade.

![image](https://github.com/XaSaFa/MP04/assets/110727546/1e7bc044-fe52-4239-a040-6dedac30fe6c)

## Actualitzar versió de Linux

Si enlloc dels paquets volem actualitzar el sistema operatiu tenim la comanda sudo do-release-upgrade.

Aquesta comanda actualitza el sistema operatiu a la nova versió existent, però fa falta configurar el fitxer /etc/update-manager/release-upgrades.

![image](https://github.com/XaSaFa/MP04/assets/110727546/03762673-2303-4afc-9fba-a0c8aa4df4e6)

![image](https://github.com/XaSaFa/MP04/assets/110727546/6b1ca11b-5d15-4bac-aada-b6cf4c572e65)
