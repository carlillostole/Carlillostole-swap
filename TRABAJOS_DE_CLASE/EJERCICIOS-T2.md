**Ejercicio T2.1: Calcular la disponibilidad del sistema descrito en edgeblog.net si en cada subsistema tenemos en total 3 elementos.**

La disponibilidad al hacer dos réplicas de cada elemento es de 99.203%. Se puede calcular la disponibilidad de cualquier sistema replicando elementos con igual o distinta disponibilidad usando el código incluido.


**Ejercicio T2.2: Buscar frameworks y librerías para diferentes lenguajes que permitan hacer aplicaciones altamente disponibles con relativa facilidad. Como ejemplo, examina PM2: https://github.com/Unitech/pm2 que sirve para administrar clústeres de NodeJS.**

-Microsoft Operations Framework (MOF) para conseguir alta disponibilidad en productos y tecnologías de Microsoft.
-IBM High Availability Cluster Multiprocessing está orientado a correr en clusters con SO AIX Unix e IBM System p (Sistemas Operativos creados por IBM) y conseguir un cluster de multiprocesamiento de alta disponibilidad.
-Linux-HA es un framework para clusters de alta disponibilidad que usen Linux.


**Ejercicio T2.3: ¿Cómo analizar el nivel de carga de cada uno de los subsistemas en el servidor? Buscar herramientas y aprender a usarlas.**

-Top permite conocer en tiempo real la actividad del procesador, así como la lista de procesos que hacen un mayor uso de la CPU.
-Gnome-System-Monitor
-Performance Monitor en Windows.
-Munin
-Nagios
-Ganglia
-Zabbix


**Ejercicio T2.4: Buscar diferentes tipos de productos: (1) Buscar ejemplos de balanceadores software y hardware (productos comerciales). (2) Buscar productos comerciales para servidores de aplicaciones. (3) Buscar productos comerciales para servidores de almacenamiento.**

**(1)**
Entre los balanceadores de carga software más conocidos están HAProxy y Nginx. También están Linux Virtual Servers, Pound o Pen. Ejemplos de balanceadores de carga hardware:

-Serie BIG-IP de f5.
-Cisco tiene una gran gama de balanceadores. Sus routers también incluyen esta función.
-AppDirector OnDemand de la compañía Radware.
-Load Balancer ADC de Barracuda.

**(2)**
Servidores de aplicaciones Java EE:

-WebLogic de Oracle.
-WebSphere de IBM.
-JBoss AS de JBoss (RedHat).
-Geronimo y TomEE de Apache.

Otros servidores de aplicación:

-Internet Information Server, de Microsoft, para .NET.
-Base4 Server.
-Zope.

**(3)** 
Buscar productos comerciales para servidores de almacenamiento:
Hay infinidad de servidores de almacenamiento, en especial con la proliferación de servicios y almacenamiento en la nube. Por ejemplo:

-Dell Compellent FS8600
-HP ConvergedSystem 200-HC StoreVirtual System
-IBM EXP2500 Storage Enclosure
