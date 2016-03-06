**CARLOS TOLEDANO DELGADO 3GII - SWAP (TECNOLOGIAS DE LA INFORMACION)**

**TRABAJO: buscar información sobre el tipo de contenido para el que los siguientes software de servidor web es más adecuado (o más eficiente, o se usa más actualmente...): apache, nginx, cherooke, lighttp, node.js, tomcat**


#**NGINX**

Nginx es un servidor web/proxy inverso ligero de alto rendimiento y un proxy para protocolos de correo electrónico (IMAP/POP3).
Es el segundo servidor web más usado en dominios activos (14,35%) superando a Microsoft Information Server. Además, pasó a ser la marca más usada en más de 100 millones de sitios. 
Nginx está diseñado para ser un buen servidor para sitios que necesitan velocidad, proxy inversos eficientes y eficiente servicio de contenido estático. Una característica importante es que tiene un uso bajo de memoria siendo recomendado para sitios que corren sobre VPS.

	•	Servidor de archivos estáticos, índices y autoindexado.
	•	Proxy inverso con opciones de caché.
	•	Balanceo de carga.
	•	Tolerancia a fallos.
	•	Soporte de HTTP y HTTP2 sobre SSL.
	•	Soporte para FastCGI con opciones de caché.
	•	Servidores virtuales basados en nombre y/o en dirección IP.
	•	Streaming de archivos FLV y MP4.9
	•	Soporte para autenticación.
	•	Compatible con IPv6
	•	Soporte para protocolo SPDY
	•	Compresión gzip.
	•	Habilitado para soportar más de 10.000 conexiones simultáneas. 


#**APACHE**

La arquitectura del servidor Apache es muy modular. El servidor consta de una sección core y diversos módulos que aportan mucha de la funcionalidad que podría considerarse básica para un servidor web. 
Es usado principalmente para enviar páginas web estáticas y dinámicas en la World Wide Web. Muchas aplicaciones web están diseñadas asumiendo como ambiente de implantación a Apache, o que utilizarán características propias de este servidor web.
Apache es el componente de servidor web en la popular plataforma de aplicaciones LAMP, junto a MySQL y los lenguajes de programación PHP/Perl/Python y también Ruby.

	•	Modular
	•	Código abierto
	•	Multi-plataforma
	•	Extensible
	•	Popular (ayuda/soporte)


#**THTTPD**

THTTPD (tiny/turbo/throttling HTTP server) es un servidor web de código libre disponible para la mayoría de las variantes de Unix. Se caracteriza por ser simple, pequeño, portátil, rápido, y seguro, ya que utiliza los requerimientos mínimos de un servidor HTTP. Esto lo hace ideal para servir grandes volúmenes de información estática.

	•	Simple
	•	Pequeño
	•	Portátil
	•	Rápido
	•	Seguro

El uso apropiado de esta herramienta es obtener velocidad en la transferencia de archivos y reducción de gastos innecesarios para funciones que no son requeridas en el servidor, debido a tener solo la posibilidad de utilizar servidores estándar (Apache).
Este rasgo importante permite al administrador de servidor limitar la tasa de bit máxima para ciertos tipos de archivos transferidos, generando, una aplicación mucho más ligera y rápida.


#**CHEROKEE**

Cherokee es un servidor web multiplataforma. Su objetivo es ser rápido y completamente funcional, sin dejar de ser liviano comparado con otros servidores web. Está escrito completamente en C. Puede usarse como un sistema embebido y soporta complementos para aumentar sus funcionalidades. Es software libre, disponible bajo la Licencia Pública General de GNU.

	•	Soporta tecnologías como: FastCGI, SCGI, PHP, CGI, SSI, SSL/TLS. 
	•	Soporta la configuración de servidores virtuales.
	•	Permite la realización de redirecciones.
	•	Permite su utilización como balanceador de carga.
	•	Dispone de un panel de autenticación:
	•	plain
	•	htpasswd
	•	htdigest
	•	PAM


#**NODE.JS**

Node.js es un entorno en tiempo de ejecución multiplataforma, de código abierto, para la capa del servidor, basado en el lenguaje de programación ECMAScript, asíncrono, con I/O de datos en una arquitectura orientada a eventos y basado en el motor V8 de Google. Fue creado con el enfoque de ser útil en la creación de programas de red altamente escalables, como por ejemplo, servidores web. 

Node.js es similar en su propósito a Twisted o Tornado de Python, Perl Object Environment de Perl, C,EventMachine de Ruby, Apache MINA ... Al contrario que la mayoría del código JavaScript, no se ejecuta en un navegador, sino en el servidor. Node.js implementa algunas especificaciones de CommonJS e incluye un entorno REPL para depuración interactiva.


#**TOMCAT**

Apache Tomcat (también llamado Jakarta Tomcat o simplemente Tomcat) funciona como un contenedor de servlets desarrollado bajo el proyecto Jakarta en la Apache Software Foundation. Tomcat implementa las especificaciones de los servlets y de JavaServer Pages (JSP) de Oracle Corporation.
Tomcat puede funcionar como servidor web por sí mismo. En sus inicios existió la percepción de que el uso de Tomcat de forma autónoma era sólo recomendable para entornos de desarrollo y entornos con requisitos mínimos de velocidad y gestión de transacciones. Hoy en día ya no existe esa percepción y Tomcat es usado como servidor web autónomo en entornos con alto nivel de tráfico y alta disponibilidad.

Dado que Tomcat fue escrito en Java, funciona en cualquier sistema operativo que disponga de la máquina virtual Java.