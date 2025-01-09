# Preparar la xarxa per utilitzar LDAP

Per a poder fer les pràctiques simularem una xarxa on puguin connectar-se els dos ordinadors, client i servidor.

Per a fer-ho farem servir VirtualBox amb **Xarxa NAT**.

# 1. Crear la xarxa

Al mateix VirtualBox anem a Archivo->Herramientas->Network Manager:

![image](https://github.com/XaSaFa/MP04/assets/110727546/f115473c-4f47-4a85-906e-25f182b79eca)

Seleccionem NAT Networks i fem clic a Crear:

![image](https://github.com/XaSaFa/MP04/assets/110727546/1c536b43-793f-465b-8d7a-672350b9e61a)

Configurem la xarxa i el seu nom, deixem actiu DHCP:

![image](https://github.com/XaSaFa/MP04/assets/110727546/49757c0f-1610-45f9-bcde-dcbe2d8e476d)

Quedarà així:

![image](https://github.com/XaSaFa/MP04/assets/110727546/687f40ce-dd34-47ca-ac02-96ce19de3da3)

# 2. Canviem les opcions de xarxa de les MV servidor i client:

Tenint les MV apagades canviem les opcions a configuració:

![image](https://github.com/XaSaFa/MP04/assets/110727546/5fcd92a6-f218-4760-a644-4bc954d88e62)

![image](https://github.com/XaSaFa/MP04/assets/110727546/3e6d5412-edcc-47ac-a224-494e0493b920)

# 3. Fixem la IP del servidor:

La MV del servidor ha de tenir IP fixa, per això utilitzem Netplan.

Establim IP fixa amb netplan a la màquina servidor.

![image](https://github.com/XaSaFa/MP04/assets/110727546/4ac4efb9-2f0e-4736-91cb-d79c4cea9651)

Apliquem els canvis amb: 

```
sudo netplan apply
```

I comprovem que tenim la IP escollida:

![image](https://github.com/XaSaFa/MP04/assets/110727546/0fb4e3d3-7ba0-4cd2-918b-e8d2f11d397f)

# 4. Comprovem que el client i el servidor poden fer ping.

IP Servidor (Fixa):

![image](https://github.com/XaSaFa/MP04/assets/110727546/b02e9a1c-176a-4fa8-a612-8804fe1a4f3f)

IP client (DHCP):

![image](https://github.com/XaSaFa/MP04/assets/110727546/eca8d54b-d8e1-4731-a6d2-f85a5570dbdd)

Ping Client a Servidor:

![image](https://github.com/XaSaFa/MP04/assets/110727546/a916ec49-6971-4769-a30a-9646950ed59e)

Ping Servidor a Client:

![image](https://github.com/XaSaFa/MP04/assets/110727546/53e19ff1-b733-4dbd-9d3d-0579ad947347)
