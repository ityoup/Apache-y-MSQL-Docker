## Docker-compose para Apache y MSQL 
### Conectar dos servicios básicos para el desarrollo web
Antes de empezar, y de levantar cualquier servicio, recomiendo crear los directorios o como son conocidos comunmente en
docker como "VOLUMES", este tipo de volumenes hacer la tarea de replicar lo que hay en el host principal, hacia un directorio
que estará dentro de una ruta designada en el contenedor.
Por ejemplo, en este caso, tenemos la siguiente ruta:


`/home/nartikn/docker/Juan/requis/Web/Respaldo-Generador-Codigos:/var/www/html`


Antes de los dos puntos, tenemos la ruta del host. Mientras que despues de ellos, la ruta del contedor, en este caso
puse una ruta donde tenia guardados mis archivos web, y en el contenedor la tipica ruta que usa el servidor de apache.

