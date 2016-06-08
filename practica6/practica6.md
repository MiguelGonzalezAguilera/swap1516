#Practica6#

**DISCOS EN RAID**

#*Configuración del RAID por software**#

**El primer paso para la realización de está practica es añadir dos discos más en /dev/sdb y dev/sdc **  

**Instalamos en la maquina el software necesario para configurar el RAID**  
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica6/1.PNG)

**Creamos el disco RAID1 usando el dispositivo /dev/md0, indicando el numero de dispositivos a utilizar**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica6/3.PNG)

**Comprobamos ahora la información de los de ambos discos** 
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica6/4.PNG)

**Una vez creado el dispositivo RAID usaremos /dev/md0 para darle formato con mkfs**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica6/5.PNG)

**A partir de ahora ya podemos crear el directorio en el que se montará la unidad del RAID como los parametros de su montaje**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica6/6.PNG)

**Comprobamos el estado del raid**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica6/7.PNG)

**Para finalizar el proceso y para que el sitema al arrancar monte el dispositivo RAID debemos editar el archivo /etc/fstab**
*Anotaremos el UUID correspondiente al dispositivo RAID creado*
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica6/8.PNG)

**En el archivo /etc/fstab añadimos la siguiente linea con el UUID tomado anteriormente**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica6/9.PNG)

**Finalmente simulamos un fallo en un de los discos, lo retiramos en caliente, y añadimos en caliente el disco reemplazante a este**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica6/10.PNG)
