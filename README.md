Balanceador con MySQL y Nginx

En este proyecto realizaremos una configuración con una máquina que funcionará como balanceador, 2 que funcionarán con Nginx y PHP y una ultima que tendra MySQL Server.

Configuración VagrantFile y scripts de aprovisionamiento.
Empezaremos creando las maquinas con sus IP respectivas en el archivo VagrantFile que se genera al hacer un vagrant init en la línea de comandos de nuestra terminal. La máquina que actuará de balanceador tendra una sola dirección privada con una red interna. Las máquina de MySQL tendrá también una sola dirección privada en otra red interna diferente a la del balanceador. Por último, las máquinas con Nginx tendrán dos direcciones privadas que esten en la misma red interna que las anteriores, una dirreción en cada red interna.



También hay que configurar los scripts que aprovisionarán las máquinas para que de esta forma, la primera vez que las iniciemos se instalen los paquetes necesarios de cada una.

Script máquina MySQL


Script máquinas Nginx


Script máquina Balanceador
