**Carlos Toledano Delgado - Joaquín Ballesteros Ortega**


#**Práctica 4. Comprobar el rendimiento de servidores web**

En esta práctica se deben usar las dos herramientas para medir, primero el
rendimiento de una sola máquina servidora (haciendo peticiones a la IP de la máquina
1, p.ej.), y a continuación el rendimiento de la granja web cuando usamos balanceo de
carga tanto con nginx como con haproxy (haciendo las peticiones a la dirección IP del
balanceador). 

#**Apache Benchmark**
Los resultados en VMWare han sido los siguientes:

Comando ejecutado: ab -n 1000 -c 10 http://IPmaquina/prueba.html
El archivo prueba.html es un archivo creado en /var/www.

![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/tests%20benchmark/servidor1bench.png)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/tests%20benchmark/nginxbench.png)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/tests%20benchmark/haproxybench.png)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/graficas%20benchmark/grafica1.jpg)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/graficas%20benchmark/grafica2.jpg)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/graficas%20benchmark/grafica3.jpg)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/graficas%20benchmark/grafica4.png)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/graficas%20benchmark/grafica5.png)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/graficas%20benchmark/grafica6.png)


#**Siege**

Los resultados en VMWare han sido los siguientes:

Comando ejecutado: siege  -b -t60S -v http://ipmaquina
El archivo prueba.html es un archivo creado en /var/www.

![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/tests%20siege/grafica1.png)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/tests%20siege/grafica2.png)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/tests%20siege/grafica3.png)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/graficas%20siege/grafica1.png)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/graficas%20siege/grafica2.png)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/graficas%20siege/grafica3.png)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/graficas%20siege/grafica4.png)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/graficas%20siege/grafica5.png)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/graficas%20siege/grafica6.png)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/graficas%20siege/grafica7.png)


![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA4/img/graficas%20siege/grafica8.png)

Los resultados son más o menos los esperados, tardando menos con el balanceador que en el servidor solo. Vemos también que HaProxy es mejor balanceador que Nginx, ya que los tiempos son siempre mejores.
