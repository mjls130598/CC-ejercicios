# Ejercicios del tema 1

## Ejercicio 1. Buscar una aplicación de ejemplo, preferiblemente propia, y deducir qué patrón es el que usa. ¿Qué habría que hacer para evolucionar a un patrón tipo microservicios?.

El patrón que utiliza mi Trabajo de Fin de Grado es una arquitectura en capas ya que implementa un buscador para cualquier dispositivo móvil en el que se divide de la siguiente manera: en la capa de la interfaz es donde el usuario puede interactuar con el sistema, en la capa de aplicación se encarga de la comunicación entre el servidor y el cliente, en la de lógica del negocio se realiza las búsquedas de los documentos del sistema y, por último, en la de acceso a los datos se encarga de obtener los datos almacenados en la base de datos.

Lo que habría que hacer para que fuera un patrón de tipo microservicios sería agrupar las capas anteriores en dos servicios distintos, uno de ellos se encargaría de la interfaz del usuario y el otro de realizar aquellas acciones que se necesitan ejecutar en la parte del servidor.

## Ejercicio 2. En la aplicación que se ha usado como ejemplo en el ejercicio anterior, ¿podría usar diferentes lenguajes? ¿Qué almacenes de datos serían los más convenientes?

Sí podría utilizar distintos lenguajes ya que para la interfaz se podría utilizar HTML, CSS y JavaScript, para la comunicación cliente-servidor sería con PHP, para realizar la búsqueda dentro del sistema se haría en Java y para obtener los datos de la base de datos se realizaría en SQL.

Para guardar los documentos del sistema y las consultas realizadas sobre el buscador los convenientes serían utilizar MySQL o MongoDB.
