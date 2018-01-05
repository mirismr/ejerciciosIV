# Ejercicios tema 6

## Ejercicio 1: Instalar chef-solo en la máquina virtual que vayamos a usar
Usaré la máquina virtual *Lubuntu* instalada para los ejercicios del tema 5.

Instalamos con el comando: `sudo curl -L https://www.opscode.com/chef/install.sh | bash`:

![Instalacion](img/45.png)
![Instalacion](img/46.png)

## Ejercicio 2: Crear una receta para instalar la aplicación que se viene creando en la asignatura en alguna máquina virtual o servidor en la nube.

Se ha hecho en el proyecto de la asignatura y está explicado en la [documentación] (https://mirismr.github.io/proyectoIV17-18/)

## Ejercicio 3: Desplegar la aplicación de DAI con todos los módulos necesarios usando un playbook de Ansible.

Se ha hecho en el proyecto de la asignatura y está explicado en la [documentación] (https://mirismr.github.io/proyectoIV17-18/)


## Ejercicio 4: Instalar una máquina virtual Debian usando Vagrant y conectar con ella.

Así se ha instalado la máquina virtua usada en la asignatura DAI. Para ello creamos el Vagrantfile con `vagrant init bento/ubuntu-16.04`.
En el directorio donde esté el Vagrantfile hacemos `vagrant up`:
![Instalacion](img/47.png)

Para conectarnos a la máquina ejecutamos `vagrant ssh`:
![Instalacion](img/48.png)
