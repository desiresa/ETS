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

## 1. Instalación de git con paquetes predeterminados <a name="id1"></a>

<div style="text-align: justify">

Primero probaremos a instalar git con paquetes predeterminados y con la versión más estable y reciente disponible. Esto nos servirá para empezar a utilizar Git en el equipo de una manera más rápida.

Antes de instalarlo comprobaremos si ya tenemos una versión disponible con el siguiente comando.

</div>

````
git --version
````

<div align="center">

![](./Imagen/1.png)

</div>

<div style="text-align: justify">

Si no nos aparece una versión instalada, procederemos a ejecutar el comando que nos recomiendo para la instalación. O si simplemente queremos tener una versión instalada más actual.

Primero actualizaremos los paquetes, por si algún paquete se encuentra desactualizado.

````
sudo apt update
````

<div align="center">

![](./Imagen/4.png)

</div>

Luego de la actualización, podremos instalar Git.

````
sudo apt install git
````

<div align="center">

![](./Imagen/2.png)

</div>

Nos deberá devolver el siguiente resultado.

<div align="center">

![](./Imagen/3.png)

</div>

## 2. Instalación de Git desde la fuente <a name="id2"></a>

Esta opción de instalación nos permitirá utilizar cualquier versión de git que queramos usar o simplemente probar. Las podremos encontrar en la siguiente dirección: **https://mirrors.edge.kernel.org/pub/software/scm/git/** .

Primero verificamos si tenemos Git instalado, y la versión que tengamos instalada:

````
git --version
````

<div align="center">

![](../Imagen/6.png)

</div>

Para poder comenzar a instalar la versión, deberemos actualizar los repositorios del sistema.

````
sudo apt update
````

![](../Imagen/.png)

Y también instalaremos la lista de paquetes necesarios para el correcto funcionamiento de Git.

````
sudo apt install libz-dev libssl-dev libcurl4-gnutls-dev libexpat1-dev gettext cmake gcc
````

![](../Imagen/8.png)

Después de haber instalado la lista de paquetes, y que no nos haya saltado ningun error. Crearemos una carpeta temporal, donde descargaremos la versión de Git que queramos instalar.

````
mkdir tmp
cd /tmp
````

![](../Imagen/9.png)

Desde la página web anterior -> **https://mirrors.edge.kernel.org/pub/software/scm/git/**, escogeremos una versión, en este caso la última hasta el momento. Usando el comando curl *(una herramienta para obtener o enviar datos usando la sintaxis de URL)*, que deberemos instalar si no se encuentra disponible.


![](./Imagen/7.png)


````
sudo apt install curl
````
![](./Imagen/8.png)

Utilizamos la herramienta curl, junto con la dirección del paquete que queramos descargar, y enviaremos el archivo a git.tar.gz.

````
curl -o git.tar.gz https://mirrors.edge.kernel.org/pub/software/scm/git/git-2.29.3.tar.gz
````

![](./Imagen/9.png)

Descomprimimos el archivo:

````
tar -zxf git.tar.gz
````

![](./Imagen/10.png)

Vamos al directorio donde se encuentra el archivo descomprimido.

````
cd git-*
````

![](./Imagen/11.png)

Creamos el paquete con make, y lo instalamos.

````
make prefix=/usr/local all
sudo make prefix=/usr/local install
````

![](./Imagen/)

![](./Imagen/12.png)
