# TALLER 1: APLICACIONES DISTRIBUIDAS (HTTP, SOCKETS, HTML, JS,MAVEN, GIT)

**Estudiante:** Edwar Fabian Lozano Florez  
**Clase:** AREP  
**Profesor:** Luis Daniel Benavides

## Arquitectura
La aplicación cuenta con una arquitectura monolítica lo que hace que tanto el front como el back se ejecuten en el mismo servidor
(Localhost). Por otro lado, también se emplea arquitectura por capas, separando la lógica en la capa de servicios, permitiendo así,
que en el controlador se puedan agregar más endpoints simplemente utilizando sus servicios.

Si se desea cambiar el proveedor del servicio (API), se puede realizar fácilmente debido a que la conexión se realiza desde
la interfaz **connectionService**, entonces para una nueva conexión únicamente se deberían crear una nueva clase que la implemente, 
con los nuevos parámetros. Además, connectionService devuelve una conexión del tipo HTTPUrlConnection. También cuenta con una
sobrecarga de constructores lo que le permite crear la conexión a la nueva API o si esta llega a requerir parámetros, por
ejemplo, una búsqueda, también le permita realizar la conexión. También se puede fácilmente agregar una nueva funcionalidad
a partir de la información brindada por el nuevo proveedor.

## Testeo 
Se realizan 2 pruebas TDD, una comprobando que se pueda encontrar una película por el nombre dado Y la otra que comprueba que
se pueda cambiar el poveedor de la información y la conexión siga siendo factible.

## USO
Para iniciar la aplicación se debe:
1. Ejecutar el meteodo **main** que se encuentra en la clase **Gateway**
2. Dirigirse al navegador y buscar: **localhost:8080/app.html**

Dentro de la aplicación se encontrará una interfaz muy sencilla con una barra de búsqueda en la parte superior y la ventana de
bienvenida.
![img.png](src/main/resources/static/img/img.png)

Para acceder a la información de la película deseada únicamnete se debe buscar su nombre en la barra de búsqueda.
![img_1.png](src/main/resources/static/img/img_1.png)