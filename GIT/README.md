# Instalación de Git en Linux

<div align="center">

![img git](http://mgaitan.github.io/intro-git/img/Git.png)

</div>

### Requisitos previos

<div style="text-align: justify">

Antes de proceder a la realización de la instalación de git, deberemos tener un equipo o una máquina virtual, con un sistema operativo Linux y deberemos contar con una cuenta con permisos de administrador (**Root**).

</div>

## Índice

 1.[Instalación de git con paquetes predeterminados](#id1)

 2.[Instalación de git desde la fuente](#id2)

 3.[Configuración de Git](#id3)

## Instalación de git con paquetes predeterminados <a name="id1"></a>

<div style="text-align: justify">

Primero probaremos a instalar git con paquetes predeterminados y con la versión más estable y reciente disponible. Esto nos servirá para empezar a utilizar Git en el equipo de una manera más rápida.

Antes de instalarlo comprobaremos si ya tenemos una versión disponible con el siguiente comando.

</div>

````
git --version
````

<div align="center">

![](1.png)

</div>

<div style="text-align: justify">

Si no nos aparece una versión instalada, procederemos a ejecutar el comando que nos recomiendo para la instalación. O si simplemente queremos tener una versión instalada más actual.

Primero actualizaremos los paquetes, por si algún paquete se encuentra desactualizado.

````
sudo apt update
````

<div align="center">

![](2.png)

</div>

Luego de la actualización, podremos instalar Git.

````
sudo apt install git
````

<div align="center">

![](3.png)

</div>

Nos deberá devolver el siguiente resultado.

![](4.png)

## Instalación de Git desde la fuente <a name="id2"></a>

Esta opción de instalación nos permitirá utilizar cualquier versión de git que queramos usar o simplemente probar. Las podremos encontrar en la siguiente dirección: **https://mirrors.edge.kernel.org/pub/software/scm/git/** .
