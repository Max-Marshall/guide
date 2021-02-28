## Problemas comunes en un servidor de aplicaciones

En esta guía aprenderemos algunos problemas que se suelen presentar en nuestros servidores de aplicaciones y como detectarlos de la mejor forma.

![Image](https://promwebsoft.com/files/images/varias/desarrollo-aplicaciones-web.png)

### ¿Cómo sabemos si tenemos conexión a internet? 

Esto es algo muy común que se suele presentar cuando instalamos un servidor, para detectarlo la mejor forma es usar algunos de estos comandos (Linux/Windows).

`ping 8.8.8.8` _un simple ping a Google nos permite saber si estamos conectados_

`ifconfig` _para ver la configuración de red en linux_

`ipconfig` _para ver la configuración de red en windows_

### ¿Cómo sabemos si nuestro servidor es accesible desde Internet?

Al igual que debemos comprobar que podemos acceder a internet, también tenemos que asegurarnos que internet pueda acceder a nosotros.

`sudo ufw status` _comprobamos el estado del firewall en linux_

`sudo ufw disable` _para desactivarlo en caso que no permita acceder a otros dispositivos a nuestro servidor_

`sudo ufw status` _comprobamos el estado del firewall en linux_

`sudo ufw disable` _para desactivarlo en caso que no permita acceder a otros dispositivos a nuestro servidor_

`netsh advfirewall set currentprofile state off` _en el caso de windows, el firewall se desactiva con este comando_

`netstat /a` _también podemos utilizar netstat para ver todas las conexiones activas hacia y en nuestro servidor_


### Cómo sabemos a quién pertenece una dirección web (URL)?

`dig google.es` _en linux podemos usar dig para ver a quien pertenece_

`nslookup google.es` _en windows podemos hacerlo con nslookup_

### ¿Cómo probamos que podemos acceder a un servidor?

En la mayoría de casos haciendo un `ping` podemos comprobarlo, pero si queremos acceder a un recurso específico podemos utilizar lo siguiente:

`curl dominio.com/recurso` _tanto en linux como windows podemos usar curl, el cuál tiene muchas opciones disponibles_

`wget dominio.com/recurso` _este también es similar al curl, pero en windows deberemos instalarlo por separado_

### ¿Qué otros comandos te han hecho falta?

En la sección de comprobación de firewalls tuve que utilizar algunos especificos como `netsh`.
