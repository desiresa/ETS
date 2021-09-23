# ETS

## Maven

## Instalación de Maven en Xubuntu

## Índice

1. [Instalar apache Maven con apt](#instalar1)

2. [Instalar una versión concreta de Apache Maven](#instalar2)

3. [Verificación de la Instalación](#instalar3)

## 1. Instalar Apache Maven con apt <a name="instalar1"></a>

Actualizamos el SO con:

````
sudo apt update`
````
![]()

````
sudo apt install maven
````
![]()

Comprobamos la versión que nos instaló:

````
mvn -version
````
![]()

Con esto ya tenemos instalado Maven, pero también podemos instalar una versión en concreto descargandolo desde la página de Apache.

## 2. Instalar una versión en concreto de Apache maven <a name="instalar2"></a>

Descargamos la última versión disponible que encontremos en la página.
````
wget https://www.apache.org/dist/maven/maven-3/3.8.2/binaries/apache-maven-3.8.2-bin.tar.gz -P /tmp
````

![]()

Cuando se complete la instalación, movemos la carpeta al directorio /opt.

````
sudo tar xf /tmp/apache-maven-*.tar.gz -C /opt
````
![]()


Para mayor comodidad a la hora de comprobar las actualizaciones y las versiones de Maven, crearemos un enlace símbolico de Maven en /opt.

````
sudo ln -s /opt/apache-maven-3.8.2 /opt/maven
````
![]()

Para que Maven funcione correctamente, necesitamos crear un enlace símbolico, donde añadiremos la ruta del OpenJDK que tengamos instalado.

Creamos un nuevo archivo, dentro de /etc/profile.d/

````
sudo nano /etc/profile.d/maven.sh
````
![]()

Y lo completamos con la siguiente información:

````
export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-amd64
 export M2_HOME=/opt/maven
 export MAVEN_HOME=/opt/maven
 export PATH=${M2_HOME}/bin:${PATH}

````
![]()

````
/etc/profile.d/maven.sh
````

Cambiamos los permisos del archivo:

````
sudo chmod +x /etc/profile.d/maven.sh
````

Ejecutamos el contenido del archivo, para que cargue las variables

````
source /etc/profile.d/maven.sh
````

## 3. Verificación de la Instalación <a name="instalar3"></a>
