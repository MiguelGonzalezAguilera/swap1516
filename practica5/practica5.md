#Practica5#

**REPLICACIÓN DE BASES DE DATOS MYSQL**

#**Crear una BD e insertar datos**#

**Creamos BD**  
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/create.PNG)

**Creamos tablas** 
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/table.PNG)

**Insertamos datos en tablas**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/insert.PNG)

**Comprobamos datos insertados**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/describe.PNG)
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/.PNG)

#**Replicar una BD MySQL con mysqldump**#

**Flush de tablas en maquina1**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/flush.PNG)

**mysqldump en maquina1**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/mysqldump.PNG)

**Hacemos el unlock de las tablas**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/unlock.PNG)

**En la maquina 2 copiamos el archivo .sql con los datos salvados de la maquina1**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/scp.PNG)

**En la maquina 2 importamos la BD, primero la creamos y luego la exportamos**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/bd2.PNG)


#**Replicación de BD mediante una configuración maestro-esclavo**#

**Lo primero que debemos hacer es editar el archivo de configuración de mysql del maestro en /etc/mysql/my.cnf **

**Comentamos bind**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/comentarbind.PNG)

**Establecemos el ID del servidor a 1**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/serverid1.PNG)

**Despues de estos cambios guardamos el archivo y reiniciamos el servicio**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/restartmysql.PNG)

**El siguiente paso es editar la configuración del esclavo, es practicamente igual a la del maestro**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/id2.PNG)

**Guardamos y reiniciamos el servicio**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/restartmysql2.PNG)

**Volvemos al maestro para crear un usuario y darle una serie de permisos para la replicación**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/ordenenes2.PNG)

**Pasamos a la maquina esclava para indicarle a mysql los datos el maestro**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/ordenmaestro.PNG)

**Por ultimo al arrancar el esclavo los demonios de mysql empezaran su trabajo**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/master_slave.PNG)

**Despues de activar las tablas en el maestro, comprobamos en el esclavo el estado que la variable "Seconds_Behind_Master" es distinta de null**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/status.PNG)

**Para comprobar el funcionamiento en el maestro insertamos una serie de datos**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/query1.PNG)

**Finalmente en el esclavo podemos ver reflejados los cambios en la BD**
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica5/query2.PNG)