# Docker2

## Descarga la imagen 'httpd' y comprueba que está en tu equipo.

**sudo docker run httpd**

**sudo docker ps -a**

Aparece instalada.

## Crea un contenedor con el nombre 'dam_web1'.


## Si quieres poder acceder desde el navegador de tu equipo, ¿que debes hacer?


## Utiliza bind mount para que el directorio del apache2 'htdocs' esté montado un directorio que tu elijas.

## Realiza un 'hola mundo' en html y comprueba que accedes desde el navegador. 

## Crea otro contenedor 'dam_web2' con el mismo bind mount y a otro puerto, por ejemplo 9080.

## Comprueba que los dos servidores 'sirven' la misma página, es decir, cuando consultamos en el navegador:

### http://localhost:9080 
### http://localhost:8000

## Realiza modificaciones de la página y comprueba que los dos servidores 'sirven' la misma página
