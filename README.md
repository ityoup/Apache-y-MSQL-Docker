## Docker-compose para Apache y MSQL 
### Conectar dos servicios básicos para el desarrollo web
Antes de empezar, y de levantar cualquier servicio, recomiendo crear los directorios o como son conocidos comunmente en
docker como "VOLUMES", este tipo de volumenes hacer la tarea de replicar lo que hay en el host principal, hacia un directorio
que estará dentro de una ruta designada en el contenedor.
Por ejemplo, en este caso, tenemos la siguiente ruta:


`/home/nartikn/docker/Juan/requis/Web/Respaldo-Generador-Codigos:/var/www/html`


Antes de los dos puntos, tenemos la ruta del host. Mientras que despues de ellos, la ruta del contedor, en este caso
puse una ruta donde tenia guardados mis archivos web, y en el contenedor la tipica ruta que usa el servidor de apache.

De igual manera, pasa lo mismo con la ruta de MYSQL, recomiendo seguir la misma ruta del contenedor.

Una vez que se hayan creado los volumenes, faltaría levantar el docker-compose con el siguiente comando:

`Docker-compose up -d`

Este comando buscará las imagenes, las descargará y las levantará.

Con el comando:

`docker ps`

Podemos ver las imagenes que estan en funcionamiento.


### Hacer las conexiones de red entre contenedores

Primero que nada, crearemos una network, para asi poder conectar contenedores:

`docker network create`

Es así, como crearemos la red. (Debe especificar el nombre de la misma despues de `create`


Una vez que haya sido creada, faltaría conectarlos contenedores, haciendo un `docker ps` podremos encontrar la id del contenedor
y la necesitaremos para conectarlos

con un `docker network connect` y la id del contenedor, los conectaremos. (Hacerlo con los dos)


para ver si los contenedores han sido conectados, usamos:


`docker network inspect` y el nombre de la red que le pusimos más atrás.

![](https://media.giphy.com/media/vFKqnCdLPNOKc/giphy.gif)
