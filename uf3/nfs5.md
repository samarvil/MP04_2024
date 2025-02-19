# Muntar automàticament les carpetes compartides

És probable que vulguem que les carpetes compartides estiguin disponibles automàticament quan un client entri al sistema, per a fer-ho modificarem **/etc/fstab** al client.

```
sudo nano /etc/fstab
```

Cada línia del fitxer representa un volum diferent en el següent format:

- Dispositiu: Referencia el volum que anem a muntar. En el nostre exemple serà 192.168.1.10:/shared
- Punt de muntatge: La carpeta on es muntaran les dades del volum. /mnt/nfs/shared
- Sistema de fitxers: Indica el sistema de fitxers del volum. nfs.
- Opcions: Paràmetres que farà servir mount per muntar el dispositiu. Separats per comes i sense espais. Utilitzarem: auto,noatime,nolock,bg,nfsvers=3,intr,tcp,actimeo=1800.
- Freqüència de backup: Cada quan es farà un dump per copiar el sistema de fitxers, si utilitzem 0 no es fa la copia.
- Ordre de revisió: Ordre en el que l'eina fsck revisa el volum cercant posibles errors durant el procés d'inici. Si val 0 no es revisa.

La línia que escreiurem será:

192.168.1.10:/shared /mnt/nfs/shared nfs auto,noatime,nolock,bg,nfsvers=3,intr,tcp,actimeo=1800 0 0

Podeu consultar les opcions de forma més exhaustiva [aquí](https://manpages.ubuntu.com/manpages/noble/en/man5/nfs.5.html).

![image](https://github.com/XaSaFa/MP04/assets/110727546/55d43a9a-e803-4111-9cd5-4e5ca6a08dc9)

Caldrà reiniciar per comprovar que el volum queda muntat correctament.

![image](https://github.com/XaSaFa/MP04/assets/110727546/a754ea5e-2932-4ab8-9c1f-1694d137ff03)
