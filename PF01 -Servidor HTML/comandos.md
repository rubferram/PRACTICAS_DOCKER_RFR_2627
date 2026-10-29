## docker image pull nginx:alpine 
Descarga la imagen
## docker images 
Comprueba que se ha instalado
## docker create --name servidor -p 8080:80 nginx:alpine 
Crea el contenedor
## docker start servidor 
Inicia el contenedor
## curl localhost:8080 
Prueba que todo está correcto
## docker cp ./html/holamundo.html servidor:/usr/share/nginx/html/index.html 
Copia el contenido del repositorio al contenedor
## docker logs -f servidor 
Muestra el registro del contenedor y lo pone en modo seguimiento
## docker commit -a "rubferram" servidor rubferram/miservidorweb:1.0 
Crea una nueva imagen a partir del contenedor
## docker save -o miservidorweb.tar rubferram/miservidorweb:1.0 
Exporta la imagen a una imagen .tar para uso posterior
## docker system prune 
Elimina todas las imagenes y contenedores
## docker import miservidorweb.tar 
Importa la imagen
