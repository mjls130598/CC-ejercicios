# Ejercicios del tema 2

## Ejercicio 1. Instalar alguno de los entornos virtuales de node.js (o de cualquier otro lenguaje con el que se esté familiarizado) y, con ellos, instalar la última versión existente, la versión minor más actual de la 4.x y lo mismo para la 0.11 o alguna impar (de desarrollo).

Las distintas versiones que se han instalado para este ejercicio son del lenguaje node.js con el entorno virtual nvm.

Para instalar las versiones, primero he instalado el entorno virtual nvm escribiendo en la terminal el siguiente comando:

`curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.36.0/install.sh | bash`

Una vez instalado, se comenzó a instalar las distintas versiones escribiendo en la terminal 

`nvm install v8.11.1`

siendo `8.11.1` la versión que se quiere descargar.

Para ver las versiones disponibles que se pueden instalar se ejecuta en la terminal el comando

`nvm ls-remote`

Las versiones instaladas fueron la 15.0.0, la 4.9.1 y la 11.15.0.

Una demostración de que se ha realizado la instalación de las versiones anteriores se encuentra en la siguiente imagen:

![Lista de versiones instaladas de node.js](./imagenes/lista_node.png "Lista de versiones instaladas de node.js")

## Ejercicio 2. Crear una descripción del módulo usando package.json. En caso de que se trate de otro lenguaje, usar el método correspondiente.

Para crear la descripción del módulo de la aplicación de ejemplo, se debe escribir en la terminal dentro de la carpeta del proyecto `npm init`. Una vez ejecutado el comando anterior, se deberán seguir los pasos que se indica por pantalla como los de la siguiente imagen:

![Pasos del npm init](./imagenes/npm-init.png "Pasos del npm init")

Cuando se hayan realizado todos los pasos, el package.json resultado es el que se muestra a continuación:

![Archivo package.json](./imagenes/package.png "Archivo package.json")

## Ejercicio 3. Descargar el repositorio de ejemplo anterior, instalar las herramientas necesarias (principalmente Scala y sbt) y ejecutar el ejemplo desde sbt. Alternativamente, buscar otros marcos para REST en Scala tales como Finatra o Scalatra y probar los ejemplos que se incluyan en el repositorio.

Primero, se instaló Java 8, Scala y SBT. Los pasos que se siguió para instalar SBT se encuentra en [su página oficial](https://www.scala-sbt.org/download.html?_ga=2.121828747.1077410046.1603361923-1348640796.1603358470).

Una vez instaladas las herramientas necesarias, se clonó el repositorio del profesor con `git clone https://github.com/JJ/spray-test my-project`.

Cuando se terminó de clonar el repositorio "spray-test", se ejecutó en el terminal dentro del directorio el comando `sbt`, que cargará el proyecto y nos mostrará un shell donde se escribe las órdenes que se quieran ejecutar sobre ese proyecto.

A continuación, se ejecutaron los test sobre este proyecto con la orden `test`. El resultado de que el test se pasó correctametne se muestra en la siguiente imagen:

![Test](./imagenes/test.png "Test")

Después, se escribió en el shell `re-start` para que comenzara la aplicación. Cuando se esté ejecutando el comando anterior, se dirigió a http://localhost:8080 como se muestra a continuación:

![Localhost](./imagenes/localhost.png "Localhost")

En una terminal distinta, se ejecuta una serie de pruebas para ver el correcto funcionamiento del proyecto. Las pruebas que se realizaron se pueden observar en la siguiente imagen:

![Pruebas](./imagenes/pruebas.png "Pruebas")

Para terminar la ejecución del proyecto, se escribe en el shell de SBT `re-stop`.

## Ejercicio 4. Para la aplicación que se está haciendo, escribir una serie de aserciones y probar que efectivamente no fallan. Añadir tests para una nueva funcionalidad, probar que falla y escribir el código para que no lo haga. A continuación, ejecutarlos desde mocha (u otro módulo de test de alto nivel), usando descripciones del test y del grupo de test de forma correcta. Si hasta ahora no has subido el código que has venido realizando a GitHub, es el momento de hacerlo, porque lo vamos a necesitar un poco más adelante.

Antes de crear los test, se ha creado el archivo Apuesta.js con cinco funciones:
	1. Para que recoja los datos
	2. Para que escriba dichos datos en un string.
	3. Para que devuelva el valor de local.
	4. Para que devuelva el valor de visitante.
	5. Para que devuelva el valor del resultado.

Dicho archivo se observa en la siguiente imagen:

![Archivo Apuesta.js](./imagenes/apuesta.png)

A continuación, se creó el fichero que se encarga de ejecutar los test sobre Apuesta.js. En él se realiza varias comprobaciones:
	1. La apuesta creada y la apuesta escrita en una cadena sean iguales.
	2. El equipo local y el equipo visitante sean distintos.
	3. El resultado de la apuesta sea igual que el escrito en una cadena.

El archivo comentado anteriormente se muestra a continuación:

![Archivo test.js](./imagenes/test_apuesta.png)
