



El objetivo de esta práctica es configurar una red entre varias máquinas de forma que
tengamos un balanceador que reparta la carga entre varios servidores finales.

El problema a solucionar es la sobrecarga de los servidores. Se puede balancear
cualquier protocolo, pero dado que esta asignatura se centra en las tecnologías web,
balancearemos los servidores HTTP que tenemos configurados.

De esta forma conseguiremos una infraestructura redundante y de alta disponibilidad.


**Configurar una máquina e instalarle el nginx como balanceador de carga**

**1.**
El proceso de instalación en Ubuntu se basa en el uso de apt-get. Lo primero quedebemos hacer es importar la clave del repositorio de software: 
cd /tmp/
wget http://nginx.org/keys/nginx_signing.key
apt-key add /tmp/nginx_signing.key
rm -f /tmp/nginx_signing.key 

A continuación, debemos añadir el repositorio al fichero /etc/apt/sources.list Para ello, podemos ejecutar las siguientes órdenes en el terminal: 
echo "deb http://nginx.org/packages/ubuntu/ lucid nginx" >> /etc/apt/sources.list
echo "deb-src http://nginx.org/packages/ubuntu/ lucid nginx" >> /etc/apt/sources.list 

Ahora ya podemos instalar el paquete del nginx: 
apt-get update
apt-get install nginx 

**2.**
Una vez instalado, podemos proceder a su configuración como balanceador de carga.

La configuración de NginX se realiza en el archivo “/etc/nginx/conf.d/default.conf”, la configuración realizada nos permitirá redirigir el tráfico a un grupo de servidores que hemos llamado apaches con la directiva upstream, en dicho grupo de servidores hemos configurado que el primer servidor (server 192.168.111.128 weight=2) reciba el doble de carga que el servidor segundo (server 192.168.111.129 weight=1), el algoritmo para repartir la carga no es necesario que lo indiquemos porque se toma “round robin” por defecto al usar la directiva upstream. Dentro de la directiva location, deberemos indicar con la directiva proxy_pass hacia donde vamos a redirigir el tráfico entrante, en nuestro caso la dirección de acceso a nuestro grupo de servidores (http://apaches). Por último, debemos indicar que en los backends la versión de HTTP es 1.1 (proxy_http_version 1.1), y que se elimine la cabecera Connection (proxy_set_header Connextion “”).











