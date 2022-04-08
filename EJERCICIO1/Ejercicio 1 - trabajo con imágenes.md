# Ejercicio 1 - trabajo con imágenes



[TOC]

## Instrucciones

- Crear un contenedor llamado *web* con una imagen *php:7.4-apache* y cargar en el navegador un archivo *index.html* con tu nombre desde *localhost:8000*
- En ese mismo contenedor cargar en el navegador un archivo *mes.php* que muestre en pantalla el nombre del mes actual.
- Borrar el contenedor.
- Crear un contenedor llamado *bbdd* con una imagen *mariadb.*
- Establecer las variables de entorno con un usuario llamado *invitado*, con contraseña *invitado*, una contraseña *root* que sea *root* y crear una base de datos llamada *prueba*.

## Solución

1 - Pantallazo donde se vea la ejecución del contenedor con el archivo *index.html*.

```dockerfile
docker run -d --name web -p 8000:80 php:7.4-apache
```



![](C:\Users\rebel\Desktop\DESPLIEGUE\EJERCICIO1\pantalla1.jpg)



2 - Pantallazo donde sea la ejecución del contenedor con el archivo *mes.php*

![](C:\Users\rebel\Desktop\DESPLIEGUE\EJERCICIO1\pantalla2.jpg)

3 - Pantallazo donde se vea el tamaño del contenedor *web* con los dos ficheros creados.

![](c:\Users\rebel\desktop\DESPLIEGUE\EJERCICIO1\pantalla3.jpg)

> La captura se hizo después de crear el contenedor de *mariadb*, por eso aparecen los dos contenedores.



4 - Pantallazo de la consola de la Base de Datos donde se ve que hemos podido conectarnos con el usuario y base de datos creados.

 ![](c:\Users\rebel\desktop\DESPLIEGUE\EJERCICIO1\pantalla4.jpg)



5 - Pantallazo donde se comprueba que no se puede borrar la imagen de *mariadb* mientras el contenedor se está ejecutando.

![](c:\Users\rebel\desktop\DESPLIEGUE\EJERCICIO1\pantalla5.jpg)



6 - Pantallazo donde se ven las imágenes que tengo descargadas en mi ordenador.

![](c:\Users\rebel\desktop\DESPLIEGUE\EJERCICIO1\pantalla6.jpg)



7 - Pantallazo donde se ve el proceso de borrado de los contenedores usados.

![](c:\Users\rebel\desktop\DESPLIEGUE\EJERCICIO1\pantalla7.jpg)

> Primero paramos el contenedor de la base de datos que estaba en ejecución.