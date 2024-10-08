# Comandes Linux Terminal

Conèixer la IP de l'ordinador:
```
ip a
```

Comprovar connexió amb un equip del qual coneixem la seva IP:
```
ping IP
```

Instal·lar paquet XXXX de apt:
```
sudo apt install XXXX
```
desinstal·lar paquet XXXX de apt:
```
sudo apt remove XXXX
sudo apt purge XXXX
```
Comprovar si un servei funciona:
```
sudo service SERVEI status
```
(status podem canviar-ho per restart, reload, start i stop per reiniciar, recarregar, iniciar i parar un servei).

Apagar equip:
```
shutdown -h now
poweroff
```

Reiniciar equip:
```
reboot now
```

Connectar d'un equip a un altre per SSH
```
ssh nomUsuari@ipequip
```

Exemple: ssh francesc@192.168.1.10
