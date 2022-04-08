# Ejercicio 3 - Redes



[TOC]

## Instrucciones

- Crear una red bridge *redbd*.
- Crear un contenedor con *mariadb* que se conecte a la red anterior, con el puerto 3306, y un volumen persistente
- Crea un contenedor con *Adminer* que se conecte al contenedor de *mariadb*.
- Crear un contenedor llamado *bbdd* con una imagen *mariadb*.
- Comprueba en el navegador que *Adminer* funciona correctamente, que se conecta al contenedor anterior y que puede crear una base de datos nueva.

## Solución

1 - Pantallazo donde se vean los contenedores creados.



Primero creamos la red bridge con:

```dockerfile
docker network create redbd
```

Luego creamos el contenedor de *mariadb* que llamaremos *mibasededatos*:

```dockerfile
docker run -d --name mibasededatos --network redbd -p 3306:80 -env MYSQL_USER=invitado -env MYSQL_PASSWORD=invitado -env MYSQL_ROOT_PASSWORD=root mariadb
```

![](C:\Users\rebel\Desktop\DESPLIEGUE\EJERCICIO3\pantalla1.jpg)

> En la imagen podemos observar cómo se muestra el contenedor de *mariadb* en ejecución y cómo creamos el contenedor con *Adminer* conectado a *mariadb*.



2 - Pantallazo donde se vea el acceso a la BD desde la interfaz web de *Adminer.*

![](C:\Users\rebel\Desktop\DESPLIEGUE\EJERCICIO3\pantalla2.jpg)

> En la imagen se ve cómo en localhost se ejecuta *Adminer* con conexión a la BD (en la siguiente imagen se ve cómo estamos conectados).



3 - Pantallazo donde se ve la creación de una base de datos desde *Adminer*.

![](C:\Users\rebel\Desktop\DESPLIEGUE\EJERCICIO3\pantalla3.jpg)



4 - Pantallazo donde se comprueba en la consola del servidor cómo se ha creado correctamente la base de datos.

![](C:\Users\rebel\Desktop\DESPLIEGUE\EJERCICIO3\pantalla4.jpg)



5 - Pantallazo donde se comprueba que se borran las imágenes, los contenedores y los volúmenes usados.

![](C:\Users\rebel\Desktop\DESPLIEGUE\EJERCICIO3\pantalla5.jpg)