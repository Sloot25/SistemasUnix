# Fail2ban 

Actualizamos los paquetes de nuestro sistema e instalamos fail2ban
![Imagenes](Imgs/Img_1.png)
Cambiamos el directorio de trabajo y creamos una copia de las configuraciones 
![Imagenes](Imgs/Img_2.png)
Abrimos el archivo jail.local en el editor de texto nano con permisos de superusuario para hacer ajustes.
![Imagenes](Imgs/Img_3.png)
Hacemos backend = systemd
![Imagenes](Imgs/Img_4.png)
Regresamos a la raiz y reiniciamos fail2ban 
![Imagenes](Imgs/Img_5.png)
Revisamos el estatus del fail2ban 
![Imagenes](Imgs/Img_6.png)
Desbloquea manualmente una drección ip especifica que habia sido bloqueada por el setvicio ssh
![Imagenes](Imgs/Img_7.png)
Consulta el estado del filtro fail2ban para el servicio sshd, mostrando estadiscticas como IPs bloqueadas y tiempo de los bloqueos
![Imagenes](Imgs/Img_8.png)
Reinciamos 
![Imagenes](Imgs/Img_9.png)

# ClamaV

Instalamos clamav y clamav-daemon 

![Imagenes](Imgs/Img_10.png)

Ejecutamos dpkg reconfigure clamav-daemon 
![Imagenes](Imgs/Img_11.png)
![Imagenes](Imgs/Img_12.png)
![Imagenes](Imgs/Img_13.png)
![Imagenes](Imgs/Img_14.png)
![Imagenes](Imgs/Img_15.png)
![Imagenes](Imgs/Img_16.png)
![Imagenes](Imgs/Img_17.png)
![Imagenes](Imgs/Img_18.png)
![Imagenes](Imgs/Img_19.png)
![Imagenes](Imgs/Img_20.png)
![Imagenes](Imgs/Img_21.png)
![Imagenes](Imgs/Img_22.png)
![Imagenes](Imgs/Img_23.png)
![Imagenes](Imgs/Img_24.png)
![Imagenes](Imgs/Img_25.png)
![Imagenes](Imgs/Img_26.png)
![Imagenes](Imgs/Img_27.png)
![Imagenes](Imgs/Img_28.png)
![Imagenes](Imgs/Img_29.png)
![Imagenes](Imgs/Img_30.png)
![Imagenes](Imgs/Img_31.png)
![Imagenes](Imgs/Img_32.png)

Revisamos el estado del servicio clamav.freshclam

![Imagenes](Imgs/Img_33.png)

Activamos el servicio clamav-freshclam para que se inicie automaticamente 

![Imagenes](Imgs/Img_34.png)
![Imagenes](Imgs/Img_35.png)

Ejecutamos manualmente la actualización de la base de datos de virus de ClamAV usando freshclam 

![Imagenes](Imgs/Img_36.png)

Creamos el archivo script de clamavscan.sh y colocamos lo siguiente:

![Imagenes](Imgs/Img_37.png)

Asignamos permisos de ejecución al script clamavscan.sh para que el sistema pueda ejercutarlo automaticamente cada día y ejecutamos el script para verificar que funcione

![Imagenes](Imgs/Img_38.png)
![Imagenes](Imgs/Img_39.png)
![Imagenes](Imgs/Img_40.png)
![Imagenes](Imgs/Img_41.png)

# Postfix y Logwatch 

Instalamos 3 paquetes clave:

* mailutils: Herramientas de correo para enviar y leer correos desde lineas de comando 
* postfix: Un servidor de correo que gestiona el envío y recepción de correos electrónicos 
* Logwatch: Una herrmienta que analiza los registros del sistema y genera informes resumidos o detallados sobre la actividad.

![Imagenes](Imgs/Img_42.png)

Reconfigurmaos el postfix 

![Imagenes](Imgs/Img_43.png)
![Imagenes](Imgs/Img_44.png)

Abrimos el archivo aliases con nano para configurar alias de correo, que redirigen correos enviados a cuentas del sistema. 

![Imagenes](Imgs/Img_45.png)

Actualizamos la base de datos de alias después de editar /etc/aliases. Esto permite que postfix aplique los cambios y envíe correos a las nuevas direcciones de alias configuradas.

![Imagenes](Imgs/Img_46.png)

Crea un directorio de caché para Logwatch. Esto almacena datos temporales y ayuda a Logwatch a manejar archivos grandes de registro. Copiamos el archivo de configuracion y personalizamos los ajustes de tal forma que camiamos Output = mail. 

Finalmente ejecutamos el comando 

![Imagenes](Imgs/Img_47.png)
![Imagenes](Imgs/Img_48.png)

Hacemos cat de /var/mail/root 
![Imagenes](Imgs/Img_49.png)

Abrimos el archivo de tareas diarias y lo configuramos 

![Imagenes](Imgs/Img_50.png)
