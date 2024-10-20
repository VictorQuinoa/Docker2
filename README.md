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

Creo un archivo usando este comando:

```
echo "<html><body><h1>Hola Mundo</h1></body></html>" >/home/accesodatos/SXE/WebApache/index.html
```

Y para comprobar si funciona, desde el navegador de la maquina virtual y el de fuera pongo:

**http://localhost:8080**

Y se comprueba que la página funciona.

## Crea otro contenedor 'dam_web2' con el mismo bind mount y a otro puerto, por ejemplo 9080.

Para esto usamos el mismo comando anterior cambiando el puerto:

**docker run -d --name dam_web2 -p 9080:80 -v /home/accesodatos/SXE/WebApache:/usr/local/apache2/htdocs httpd:2.4**

## Comprueba que los dos servidores 'sirven' la misma página, es decir, cuando consultamos en el navegador:

### http://localhost:9080 
### http://localhost:8000

Al tener el mismo bind mount, al acceder se muestra la misma página con el mensaje de "Hola Mundo"

## Realiza modificaciones de la página y comprueba que los dos servidores 'sirven' la misma página

Cuando se modifica el archivo de la página, al estar los dos servidores montados en base al mismo archivo, ambos se actualizan de igual manera.
