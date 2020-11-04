# Ejercicios del tema 3

## Ejercicio 1. Buscar alguna demo interesante de Docker y ejecutarla localmente, o en su defecto, ejecutar la imagen anterior y ver cómo funciona y los procesos que se llevan a cabo la primera vez que se ejecuta y las siguientes ocasiones.

Antes de buscar alguna demo y descargar la imagen se debe haber descargado *Docker* en el dispositivo.

Para descargar *Docker* abrimos una terminal y escribios los siguientes pasos:

1. Se actualiza el paquete apt con `sudo apt-get update`.
2. Se instalan los paquetes necesarios para utilizar *Docker* con el comando `sudo apt-get install docker-ce docker-ce-cli containerd.io`
3. Se verifica que se ha instalado correctamente ejecutando la orden `sudo docker run hello-world`

La siguiente imagen se muestra la primera descarga de la imagen *hello-world*.

![Imagen *Hello World*](./imagenes/dockerHello.png "Imagen Hello World")

Los pasos seguidos se han obtenido de la [página oficial de *Docker*](https://docs.docker.com/engine/install/ubuntu/).

A continuación, se va a descargar el contenedor *jjmerelo/daleksay*, para eso se ejecuta el comando `sudo docker run --rm jjmerelo/docker-daleksay -f smiling-octopus Uso argumentos, ea` que realiza lo que se muestra en la siguiente imagen y que borra el contenedor que se haya creado para instalar la imagen una vez creada.

![Imagen Pulpo](./imagenes/dockerPulpo.png "Imagen Pulpo")

La primera vez que se ejecuta la imagen se descarga aquello necesario para instalar la imagen. En las siguientes veces que se ejecuta la imagen, ya no se vuelve a descargar los procesos necesarios para su ejecución como se muestra a continuación:

![Imagen Pulpo 2](./imagenes/dockerPulpo2.png "Imagen Pulpo 2")

## Ejercicio 2. Tomar algún programa simple, “Hola mundo” impreso desde el intérprete de línea de órdenes, y comparar el tamaño de las imágenes de diferentes sistemas operativos base, Fedora, CentOS y Alpine, por ejemplo.


