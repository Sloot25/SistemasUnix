# Semana 3
## Asegurar Bootloader

Accedemos al menú de edición de las entradas de GRUB
![im1](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana3/Screenshot%20from%202024-11-18%2011-29-41.png)

Le daremos opción del kernell que se utiliza para especificar el programa que debe ejecutarse como proceso de inicialización y le indicaremos al kernel que cargue una shell/bin/sh 
![im2](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana3/Screenshot%20from%202024-11-18%2011-30-46.png)

![im3](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana3/Screenshot%20from%202024-11-18%2011-33-20.png)

![im4](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana3/Screenshot%20from%202024-11-18%2011-34-38.png)

Presionamos ctrl x
![im5](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana3/Screenshot%20from%202024-11-18%2011-34-52.png)

![im6](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana3/Screenshot%20from%202024-11-18%2011-35-24.png)

Mount nos muestra una lista de todos los sistemas de archivos montados en ese momento

![im7](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana3/Screenshot%20from%202024-11-18%2011-36-12.png)

Passwd
![im8](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana3/Screenshot%20from%202024-11-18%2011-36-42.png)

Cuando se ejecuta sudo update-grub, el contenido del archivo se utiliza para construir el archivo de configuración de GRUB
![im9](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana3/Screenshot%20from%202024-11-18%2011-41-56.png)

Vamos a la linea respectiva
![im10](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana3/Screenshot%20from%202024-11-18%2011-43-31.png)

La opción --unrestricted se puede agregar a la configuración de una entrada de menú para hacerla accesible
![im11](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana3/Screenshot%20from%202024-11-18%2011-50-48.png)

Ponemos el comando sudo update-grub
![im12](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana3/Screenshot%20from%202024-11-18%2012-13-54.png)

##Protección con Contraseña de GRUB
Usamos el sudo grub-mkpasswd-pdkdf2 para generar una contraseña cifrada para usar en la configuración de GRUB
![im13](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana3/Screenshot%20from%202024-11-18%2012-18-30.png)

Colocamos el usuario root y la contraseña encriptada y guardamos el script y usamos sudo update-grub
![im15](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana3/Screenshot%20from%202024-11-18%2012-34-06.png)

Reiniciamos el sistema y se nos pedirá el usuario y contraseña
![im17](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana3/Screenshot%20from%202024-11-18%2013-10-29.png)