#Practica4#

**APACHE BENCHMARK**

#**Maquina Servidor**#

**Creamos un html en la maquina servidora en /www/var/ llamado prueba.thml*

![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/crear_html.PNG)

**Realizamos los test a la maquina servidor mediante el comando ab**  
**ab -n 1000 -c 5 http://192.168.25.129/prueba.html**
 
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/resultados_ab_serv.PNG)

**Muestra de una tabla y grafica de datos con los resultados obtenidos**

 ![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/datos_ab_serv.PNG)


#**Maquina Balanceador Nginx**#

**Ponemos en funcionamiento el servicio de nginx** 
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/onNginx.PNG)

**Realizamos los test a la maquina servidor mediante el comando ab**  
**ab -n 1000 -c 5 http://192.168.25.131/prueba.html**
 
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/resultados_ab_nginx.PNG)

**Muestra de una tabla y grafica de datos con los resultados obtenidos**

 ![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/datos_ab_nginx.PNG)

#**Maquina Balanceador Ha-proxy**#

**Ponemos en funcionamiento el servicio de ha-proxy** 

![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/onHaproxy.PNG)

**Realizamos los test a la maquina servidor mediante el comando ab**  
**ab -n 1000 -c 5 http://192.168.25.132/prueba.html**
 
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/resultados_ab_haproxy.PNG)

**Muestra de una tabla y grafica de datos con los resultados obtenidos**

 ![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/datos_ab_haproxy.PNG)



**SIEGE**

#**Maquina Servidor**#

**Realizamos los test a la maquina servidor mediante el comando de siege**  
**siege -b t60S -v http://192.168.25.129**
 
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/siege.PNG)
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/res_siege_serv.PNG)

**Muestra de una tabla y grafica de datos con los resultados obtenidos**

 ![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/datos_siege_serv.PNG)

#**Maquina Balanceador Nginx**#

**Ponemos en funcionamiento el servicio de nginx** 

![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/onNginx.PNG)

**Realizamos los test a la maquina servidor mediante el comando de siege**  
**siege -b t60S -v http://192.168.25.131**
 
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/res_siege_nginx.PNG)

**Muestra de una tabla y grafica de datos con los resultados obtenidos**

 ![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/datos_siege_nginx.PNG)

#**Maquina Balanceador Ha-proxy**#

**Ponemos en funcionamiento el servicio de ha-proxy** 

![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/onHaproxy.PNG)

**Realizamos los test a la maquina servidor mediante el comando de siege**  
**siege -b t60S -v http://192.168.25.132**
 
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/siege.PNG)
![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/res_siege_haproxy.PNG)

**Muestra de una tabla y grafica de dataos con los resultados obtenidos**

 ![img](https://github.com/MiguelGonzalezAguilera/swap1516/blob/master/imagenes/practica4/datos_siege_haproxy.PNG)

