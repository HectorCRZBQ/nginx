# Docker y Nginx como balanceador de carga

1.	Intalamos docker (https://docs.docker.com/desktop/install/windows-install/)

3.	Vamos a crear una carpeta vacia y la llamamos como queramos, en mi caso, **Balanceador_Carga**

4.	Abrimos la Windows PowerShell para comenzar con los comandos, y uan vez estemos donde nuestra carpeta vamos a crear tres htmls:
 -  PS C:\Users\hecto\Balanceo_Carga> echo "Hola Server 1"> como h1 index.1.html
 -  PS C:\Users\hecto\Balanceo_Carga> echo "Hola Server 2"> como h1 index.2.html
 -  PS C:\Users\hecto\Balanceo_Carga> echo "Hola Server 3"> como h1 index.3.html

4.	Con esto podemos levantar contenedores de docker para cada html que hemos creado anteriormente, **pero en terminales separadas**:
     * docker run --rm -v C:\Users\hecto\Balanceo_Carga\index.1.html:/usr/share/nginx/html/index.html   -p 8080: 80 nginx
     * docker run --rm -v C:\Users\hecto\Balanceo_Carga\index.2.html:/usr/share/nginx/html/index.html  -p 8081: 80 nginx
     * docker run --rm -v C:\Users\hecto\Balanceo_Carga\index.3.html:/usr/share/nginx/html/index.html  -p 8082: 80 nginx

5. En la carpeta de hosts de Windows incorporamos las direcciones para los servidores 1, 2 y 3

6.	Para extraer las direcciones IP o IPAdress, existen dos formas de acceder a estos valores:
o	Una primera por medio de la terminal con el comando **docker inspect (nombre del contenedor)**. Ej: docker inspect clever_williams.

![nginx](nginx_images/Imagen1.png)
![nginx](nginx_images/Imagen2.png)
 - Accediendo dentro de Docker Desktop a nuestro contenedor, dentro de el seleccionamos la pestaña de Inspect y la opción de Networks donde encontraremos el campo de IPAdress

![nginx](nginx_images/Imagen3.png)
 
7.	Incoporamos los valores de IP a hosts
  
![nginx](nginx_images/Imagen4.png)

10.	Tras ello debemos crear un archivo **default.conf** :

![nginx](nginx_images/Imagen5.png)

11.	Ejecutamos en una nueva terminal el comando: **docker run --rm -v C:\Users\hecto\Balanceo_Carga\default.conf:/etc/nginx/conf.d/default.conf -p 8085:80 nginx** para levantar el config anterior en el puerto 8085.

12.	Y por ultimo para ver si funciona accedemos por medio de un buscador a http://localhost:8085
Para que solo nos devuelva un servidor en concreto se usa **ip hash**.

![nginx](nginx_images/Imagen6.png)

Para poner uno como backup se monta como server server1.com:80 **backup**;
Para deshabilitar un servidor se hace con server server2.com:80 **down**;

![nginx](nginx_images/Imagen7.png)

Para que cada servidor tenga a su vez los tres servidores creados

![nginx](nginx_images/Imagen8.png)

Hector de la Cruz Baquero - [Linkdedin](https://www.linkedin.com/in/h%C3%A9ctor-de-la-cruz-baquero-ba193429b/) - [Webpage](https://hectorcrzbq.github.io/)

