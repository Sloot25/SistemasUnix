# phpMyAdmin

Hacemos un update a los paquetes de apt 
![Imagenes](Imgs/Img_1.png)

instalamos apache2 
![Imagenes](Imgs/Img_2.png)
instalamos mariadb-server 
![Imagenes](Imgs/Img_3.png)
Configuramos la seguridad del servidor mariadb
![Imagenes](Imgs/Img_4.png)
![Imagenes](Imgs/Img_5.png)
Iniciamos el cliende de linea de comandos de MariaDB para ejecutar comandos SQL en la base de datos 
![Imagenes](Imgs/Img_6.png)
Instalamos php, libapache2-mod-php y php-mysql

![Imagenes](Imgs/Img_7.png)
Abrimos el archivo de configuración 
![Imagenes](Imgs/Img_8.png)
Y movemos el archivo php a la primer posicion.
![Imagenes](Imgs/Img_9.png)
Recargamos la configuración de apache sin detener el servidor. Revisamos el estado del servidor para verificar si está activo y funcionando correctamente.
![Imagenes](Imgs/Img_10.png)
# Instalación de phpMyAdmin y paquetes recomendados.

Instalamos extensiones adicionales de PHP necesarias para el funcionamiento de phpMyAdmin. Estas extensiones permiten manejar cadenas de caracteres, archivos comprimidos y procesamiento de imagénes.
![Imagenes](Imgs/Img_11.png)
Posteriormente podemos instalar phpMyAdmin, es por ello que vamos a descargarlo desde wget. 
![Imagenes](Imgs/Img_12.png)
Descomprimimos el archivo descargado
![Imagenes](Imgs/Img_13.png)
Movemos la carpeta extraida a la ubicación estándar para aplicaciones web en el servidor.
![Imagenes](Imgs/Img_14.png)
![Imagenes](Imgs/Img_15.png)
Creamos un directorio temporal para phpMyAdmin. Cambiamos el propietario del directorio temporal a www-data, el usuario con el que corre apache.

Finalmente copiamos el archivo de configuración de ejemplo a un archivo de configuración real.
![Imagenes](Imgs/Img_16.png)
Instalamso pwgen 
![Imagenes](Imgs/Img_17.png)
Generamos una cadena de 32 caractenes con pwgen -s 32 1 
![Imagenes](Imgs/Img_18.png)
Abrimos el archivo /usr/share/phpMyAdmin/config.inc.php y establecemos una cadena de caracteres para la configuración de blowfish_secret. 
![Imagenes](Imgs/Img_19.png)
Descomentamos las directivas controluser y controlpass
![Imagenes](Imgs/Img_20.png)
Descomentamos cada una las lineas de esta seccion 
![Imagenes](Imgs/Img_21.png)
Añadimos la siguiente linea en la parte inferior del archivo 
![Imagenes](Imgs/Img_22.png)
Ejecutamos un script SQL para crear las tablas necesarias en MariaDB para el correcto funcionamiento de phpMyAdmin
![Imagenes](Imgs/Img_23.png)
Desde el prompt, ejecute el siguiente comando para crear el usuario pma y otorgarle los permisos apropiados.
![Imagenes](Imgs/Img_24.png)
![Imagenes](Imgs/Img_25.png)
Creamos o editamos el archivo de configuración de Apache para phpMyAdmin. Esto puede incluir la configuración de rutas y permisos.
![Imagenes](Imgs/Img_28.png)
Habilita la configuración de phpMyAdmin en Apache y recargamos la configuración de apache para aplicar los cambios.
![Imagenes](Imgs/Img_29.png)
Ya podemos acceder
![Imagenes](Imgs/Img_30.png)
![Imagenes](Imgs/Img_31.png)
