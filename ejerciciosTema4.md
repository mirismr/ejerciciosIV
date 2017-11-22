# Ejercicios tema 4

## Ejercicio 1: Instala LXC en tu versión de Linux favorita. Normalmente la versión en desarrollo, disponible tanto en GitHub como en el sitio web está bastante más avanzada; para evitar problemas sobre todo con las herramientas que vamos a ver más adelante, conviene que te instales la última versión y si es posible una igual o mayor a la 1.0.

Descargamos la versión del [repositorio](https://github.com/lxc/lxc) e instalamos las dependencias necesarias. Para ver que todo ha ido correctamente y que nuestro núcleo es compatible, ejecutamos `lxc-checkconfig`:

![Instalando lxc](img/16.png)

## Ejercicio 2: Crear y ejecutar un contenedor basado en tu distribución y otro basado en otra distribución, tal como Fedora.

Antes de nada debemos instalar `debootstrap` para las distribuciones *Debian* y `yum` para las distribuciones *Fedora*.

Ejecutamos el comando `lxc-create -t ubuntu -n cont-ubuntu` para crear el contenedor basado en *Debian*:

![Instalando contenedor](img/17.png)

Para crear el contenedor basado en *Fedora*, ejecutamos `lxc-create -t centos -n una-caja-centos`:

![Instalando contenedor](img/18.png)

Le cambiamos la contraseña del root tal y como nos pide cuando acabamos la instlación:

![Instalando contenedor](img/19.png)

Para poner en marcha cualquiera de los dos, introducimos el comando `lxc-start -n cont-ubuntu` o `lxc-start -n una-caja-centos`:

![Instalando contenedor](img/20.png)