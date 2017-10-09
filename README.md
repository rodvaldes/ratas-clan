# Ratas Clan Server
 
## Overview ##

La idea es poder contar con un servidor centralizado de juegos Arcade
para jugar on-line.

## Scope ##

Realizar una prueba de concepto de servidor Arcade en la nube. La prueba debe considerar.

* Instalación Y Configuración de máquina en la nube modalidad IaaS.
* Instalación de Servidor Kaillera.
* Prueba conexión remota Kaillera con cliente MAME.
* Prueba piloto modo 2P.



## Instalación del servidor Kaillera.
 ````bash
 sudo yum install --nogpgcheck glibc.i686
 ````

 ## Arranque del server
 
 ```bash
 [rvaldes@cybersyn kaillerasrv]$ ./kaillerasrv
     _ _  ____ __ ______ ___ ______  ______  ______________ _sns_ ______ _ _
   ______|   /  __\    /  __ \/   /  \/   /  \/  _  \____  \_   __\    /
   \|    |  /___\__/  /__(_/_/   /___/   /___/  _____/  / __/___\__/  /_
    |    _    \   ____  \    \   \   \   \   \   \   \   _    \   ____  \
    |_____\    \___  \   \_   \___    \___    \___    \___\    \___  \   \_
 =kAILLERA=\____/==\______/____/==\____/==\____/==\____/== \____/==\______/===
 
 Kaillera Server v0.86 (Feb 15 2002/18:05:54) (c) 2001 Christophe Thibault
 ------------------------------------------------------------------------
 
 08/19/17-14:25:09> Initializing Kaillera communication layer...
 08/19/17-14:25:09> Listening on port 27888 for incoming connections...
 08/19/17-14:25:09> Touching Kaillera master server...
 08/19/17-14:25:14> Touching done!
 08/19/17-14:26:09> Touching Kaillera master server...
 08/19/17-14:26:13> Touching done!
 08/19/17-14:27:09> Touching Kaillera master server...
 08/19/17-14:27:13> Touching done!
 08/19/17-14:27:24> Httpd: got incoming connection from 127.0.0.1
 08/19/17-14:27:25> Httpd: got incoming connection from 127.0.0.1
 08/19/17-14:27:26> Httpd: got incoming connection from 127.0.0.1
 08/19/17-14:28:09> Touching Kaillera master server...
 08/19/17-14:28:13> Touching done!
 08/19/17-14:29:09> Touching Kaillera master server...
 08/19/17-14:29:13> Touching done!
 08/19/17-14:30:09> Touching Kaillera master server...
 08/19/17-14:30:13> Touching done!
 08/19/17-14:31:09> Touching Kaillera master server...
 08/19/17-14:31:13> Touching done!
 ````
 
 ## Abrir el puerto 27888
 
 
 ```bash
[rvaldes@cybersyn ~]$ firewall-cmd --get-active-zones
public
  interfaces: enp0s3
[rvaldes@cybersyn ~]$ firewall-cmd --zone=public --add-port=27888/tcp --permanent
Authorization failed.
    Make sure polkit agent is running or run the application as superuser.
[rvaldes@cybersyn ~]$ sudo firewall-cmd --zone=public --add-port=27888/tcp --permanent
[sudo] password for rvaldes:
success
[rvaldes@cybersyn ~]$ sudo firewall-cmd --reload
success
[rvaldes@cybersyn ~]$
```
