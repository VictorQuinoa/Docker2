# Docker2

## Descarga la imagen 'httpd' y comprueba que está en tu equipo.

**sudo docker run httpd**

**sudo docker ps -a**

Aparece instalada.

## Crea un contenedor con el nombre 'dam_web1'.

**sudo docker run --dam_web1 -it httpd**

## Si quieres poder acceder desde el navegador de tu equipo, ¿que debes hacer? Utiliza bind mount para que el directorio del apache2 'htdocs' esté montado un directorio que tu elijas.

Para entrar hay que eliminar el contenedor creado usando:
**docker stop dam_web1**
**docker rm dam_web1**

Y despues usar el comando:
**docker run -d --name dam_web1 -p 8080:80 -v /home/accesodatos/SXE/WebApache:/usr/local/apache2/htdocs httpd:2.4**

## Realiza un 'hola mundo' en html y comprueba que accedes desde el navegador. 

## Crea otro contenedor 'dam_web2' con el mismo bind mount y a otro puerto, por ejemplo 9080.

## Comprueba que los dos servidores 'sirven' la misma página, es decir, cuando consultamos en el navegador:

### http://localhost:9080 
### http://localhost:8000

## Realiza modificaciones de la página y comprueba que los dos servidores 'sirven' la misma página
