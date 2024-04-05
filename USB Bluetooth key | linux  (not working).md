# USB bluetooth linux not working

Pour ajouter un périphérique bluetooth avec un terminal (donc sans blueman)

Utilise ` hcitool scan ` pour trouver le périphérique bluetooth.

Dans un terminal, `bluetoothctl` ce qui donne

```
~$ bluetoothctl 
[NEW] Controller xx:xx:xx:xx:xx:xx user-HP-desktop [default]
[NEW] Device yy:yy:yy:yy:yy:yy Galaxy S3 Mini
[bluetooth]#
```

Puis entrer `agent on`, `power on`, `scan on`

On obtient quelque chose du style

```
[bluetooth]# agent on
Agent registered
[bluetooth]# power on
Changing power on succeeded
[bluetooth]# scan on
Discovery started
[CHG] Controller xx:xx:xx:xx:xx:xx Discovering: yes
```

Nomalement, une ligne mentionnant le périphérique yy:yy:yy:yy:yy:yy devrait apparaître. Donc on peut faire

```
pair yy:yy:yy:yy:yy:yy
connect yy:yy:yy:yy:yy:yy
```
Pour quitter bluetoothctl `quit`

---
author: Nuliel
date: Le 13/03/2018, à 23:48
URL :https://forum.ubuntu-fr.org/viewtopic.php?pid=21887628#p21887628
---