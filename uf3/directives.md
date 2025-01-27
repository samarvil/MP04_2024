# Directives de grup (GPO - Group Policy Object)

Les directives de grup són objectes de Windows que emmagatzemen informació de configuració per a usuaris i grups d'un domini Active Directory.

Serveixen per fer que els usuaris i grups d'usuaris que poden fer una acció la puguin fer però prohibir que la facin als que no ho hauríen de poder fer.

## Exemple

Podem fer una directiva de grup per als usuaris d'una unitat organitzativa anomenada usuaris_bàsics.

Els membres d'aquesta unitat organitzativa no han de poder tenir accés al panell de control de Windows.

## Pas 1.- Creem una unitat organitzativa

Anem a crear l'unitat organitzativa usuaris_bàsics.

![image](https://github.com/XaSaFa/MP04/assets/110727546/2eee7313-71b4-497b-a3ee-8d2f10e9e191)

![image](https://github.com/XaSaFa/MP04/assets/110727546/7a557e81-ae4b-4256-a9d2-37b726931c9e)

![image](https://github.com/XaSaFa/MP04/assets/110727546/1cf7ee84-5fe3-4561-8c5d-ac088589e015)

## Pas 2.- Afegim usuaris a la uo

Arrosseguem els usuaris des de usuaris fins la uo.

![image](https://github.com/XaSaFa/MP04/assets/110727546/99f07852-1da2-4746-b246-0044233cd036)

## Pas 3.- Anem a configurar la directiva de grup

![image](https://github.com/XaSaFa/MP04/assets/110727546/d2070d30-c713-431d-b562-fbddbba0a49b)

![image](https://github.com/XaSaFa/MP04/assets/110727546/c397f9b2-bf94-43e7-bd7f-c5a1902eb458)

![image](https://github.com/XaSaFa/MP04/assets/110727546/261f5dd5-4e43-4709-85b3-ca4d0eee0b92)

![image](https://github.com/XaSaFa/MP04/assets/110727546/c8d1ae36-b551-4545-87f6-b4898a8990fb)

![image](https://github.com/XaSaFa/MP04/assets/110727546/7671ddc8-9449-45d2-b9ca-a8a9d1ffc800)

![image](https://github.com/XaSaFa/MP04/assets/110727546/b0796a19-fe31-4491-a20a-020677c63ac4)

![image](https://github.com/XaSaFa/MP04/assets/110727546/c3147a55-e618-409b-a944-f52e0d21141e)

![image](https://github.com/XaSaFa/MP04/assets/110727546/a8387dd5-70a3-4d8f-a60d-ceca8bf4736b)

## Pas 4.- Actualitzar directiva de grup

![image](https://github.com/XaSaFa/MP04/assets/110727546/6c296415-e7c1-4370-b253-58b2026e4d3e)

![image](https://github.com/XaSaFa/MP04/assets/110727546/59e17c82-408b-40e3-9e7a-2c2e018762c1)

Per fer que una directiva de grup s'actualitzi immediatament podem utilitzar la comanda:

```
gpupdate /force
```

## Pas 5.- Intentar accedir al Panell de Control des d'un ordinador client

Ara comprovarem que la directiva funciona, per això anem a un ordinador client, accedim amb un usuari dels que hem afegit a la UO.

Busquem Panel de Control:

![image](https://github.com/XaSaFa/MP04/assets/110727546/63465b1b-0bb3-4dee-9645-e12b495026a2)

Veiem que no ens deixa executar-lo:

![image](https://github.com/XaSaFa/MP04/assets/110727546/b07215c1-1e8e-4c31-83b2-87b3544d64ce)

