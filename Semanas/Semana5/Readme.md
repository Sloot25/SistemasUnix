# Compilar un Kernel

## Notas importantes 
* Es necesario que nuesta maquina virtua tenga 30GB de almacenamiento, de otra forma la compulación fallará por falta de almacenamiento. 

* La práctica no se realizo correctamente debido a que en los 3 intentos me marcó que la memoria no era suficiente, incluso con la partición con 140GB.

Instalamos los paquetes necesarios de tal forma que 
 apt install build-essential libncurses-dev bison flex libssl-dev libelf-
dev bc dwarves -y
![Kernel](Imgs/Img_1.png)
![Kernel](Imgs/Img_2.png)

Descargamos el código fuente del kernel linux para debian12. Usaremos el link:

[kernel](https://mirrors.edge.kernel.org/pub/linux/kernel/v6.x/linux-6.11.3.tar.gz)
Extramos los archivos descargados
Copiamos la configuración de nuestro kernel actual e iniciamos la configuración del nuevo kernel

![Kernel](Imgs/Img_3.png)
![Kernel](Imgs/Img_4.png)
![Kernel](Imgs/Img_5.png)
![Kernel](Imgs/Img_6.png)
![Kernel](Imgs/Img_7.png)
![Kernel](Imgs/Img_8.png)
![Kernel](Imgs/Img_9.png)

Compilamos nuestro kernel con todos los nucleos disponibles usando make -j $(nproc)

![Kernel](Imgs/Img_10.png)
![Kernel](Imgs/Img_11.png)
![Kernel](Imgs/Img_12.png)
![Kernel](Imgs/Img_13.png)
![Kernel](Imgs/Img_14.png)

Instalamos los modulos usando make modules_install

![Kernel](Imgs/Img_15.png)
![Kernel](Imgs/Img_16.png)
![Kernel](Imgs/Img_17.png)
![Kernel](Imgs/Img_18.png)
![Kernel](Imgs/Img_19.png)

