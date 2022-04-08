# Ejercicio 4 - Imagen con DockerFile



[TOC]

## Instrucciones

- Crear una imagen personalizada basada en *apache.*

- Desplegar una plantilla o proyecto dentro del contenedor.

  

## Solución

1 - Pantallazo donde se ve el código del archivo *DockerFile.*

![](C:\Users\rebel\Desktop\DESPLIEGUE\EJERCICIO4\pantalla1.jpg)



2 - Pantallazo donde se ve el comando que crea la nueva imagen

![](C:\Users\rebel\Desktop\DESPLIEGUE\EJERCICIO4\pantalla2.jpg)



3 - Pantallazo donde se ve funcionando el proyecto/plantilla a través de un contenedor basado en esta imagen.



Creamos el contenedor con:

```dockerfile
docker run -d--name ejercicio 80:80 ejercicio4:v1
```

Y cargamos *localhost* en el navegador.

![](C:\Users\rebel\Desktop\DESPLIEGUE\EJERCICIO4\pantalla3.jpg)



4 - Pantallazo donde se muestra la nueva imagen subida en *Docker Hub.*



Primero nos conectamos a nuestra cuenta con:

```
docker login
```

y usamos nuestro nombre y contraseña.



Una vez logueados procedemos a subir la imagen con:

```
docker push ejercicio4:v1
```

> No he podido subir correctamente la imagen por un error de sintaxis. Es posible que el error sea que cree la imagen sin poner delante mi nombre de usuario (ya he creado un repositorio llamado bradok/ejercicio4). El nombre de la imagen debería de ser bradok/ejercicio4:v1 para que pudiera subirse correctamente.