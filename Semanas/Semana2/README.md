# Semana 2
## GParted y configuración de discos con LVM

Realizamos la búsqueda de GParted 
![im0]( https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-17%2015-30-40.png)

y en la página lo descargamos![alt text](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-15%2000-49-18.png)
![a](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-15%2000-51-23.png)

Comenzando la descarga
![im5](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-17%2015-31-10.png)

Usaremos GParted en el sistema que instalamos sin LVM
![im6](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-17%2015-34-48.png)

Entramos a nuestto sistema y ejecutamos "df-h" y "lsblk"
![im10](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-17%2023-02-33.png )

Verificamos que entramos sin problema
![im7](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-17%2015-37-38.png )

Vamos a la configuración de la máquina virtual y seleccionamos la ISO de GParted
![im8](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-17%2015-37-38.png)

![im9]( https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-17%2015-56-18.png)

Iniciamos la máquina virtual 
![im11](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2000-20-54.png)

Seleccionamos la opción "Don't touch keymap"
![im13](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2000-22-02.png)

GParted iniciado
![im14](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2000-22-58.png)

Vemos la información de disco
![im15](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2000-23-07.png)

Para comenzar las modificaciones,modificamos /dev/sda8
![im16](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2000-25-20.png)

![im17](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2000-25-31.png)

![im18](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2000-27-50.png)

![im19](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2000-27-56.png)

![im20](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2000-37-13.png)

![im21](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2000-42-41.png)

![im22](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2000-54-47.png)

![im23](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2000-56-56.png)

![im24](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2000-57-32.png)

![im25](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2001-08-47.png)

![im26](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2001-13-47.png)

![im27](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2001-17-24.png)

Después de haber aplicado los cambios, guardamos todo
![im28](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2001-17-31.png)

![im29](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2001-17-53.png)

Para comprobar los cambios realizados en GParted, ejecutamos los comandos "df-h" y "lsblk"
![im31](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2001-38-00.png)

##Configuración de discos con LVM

Iremos a la parte de Hard Disk y expanderemos el disco
![im32](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2001-40-02.png)

![im33](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2001-40-04.png)

Comprobamos la información del disco
![im34](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2001-41-11.png)

Instalaremos las herramientas que necesitamos: "parted", "e2fsprogs" y "echo"
![im36](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2001-52-27.png)

![im41](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2001-53-35.png)

Verificamos los dispositivos SCSI disponibles
![im35](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2001-54-28.png)

![im37](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2001-58-23.png)

El comando indica que se realice un "rescan" del dispositivo SCSI
![im38](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2001-59-19.png)

Obtenemos la tabla de particiones actuales del disco
![im39](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2002-00-54.png)

Redimensionamos la partición
![im40](https://github.com/Sloot25/SistemasUnix/blob/main/Semanas/Semana2/Screenshot%20from%202024-11-18%2002-10-51.png)