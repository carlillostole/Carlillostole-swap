**CARLOS TOLEDANO DELGADO**

#**Ejercicios Tema 6**

**Ejercicio T6.1: Aplicar con iptables una política de denegar todo el tráfico en una de las máquinas de prácticas. Comprobar el funcionamiento.
Aplicar con iptables una política de permitir todo el tráfico en una de las máquinas de prácticas. Comprobar el funcionamiento.**

Para denegar todo el trafico, utilizamos el comando: iptables -A INPUT -j DROP
El fichero prueba.html ubicado en /var/www  no se descarga.

Para aceptar todo el trafico, utilizamos el comando: iptables -A INPUT -j ACCEPT
El fichero prueba.html ubicado en /var/www  se descarga.


**Ejercicio T6.2: Comprobar qué puertos tienen abiertos nuestras máquinas, su estado, y qué programa o demonio lo ocupa.**

Con cat /etc/services podemos ver el listado con los servicios de red del sistema. 

Para comprobaar qué servicios están activos y a la escucha en nuestro sistema Linux, utilizaremos netstat -a o con la opción -ap para mostrar qué programas están asociados a las conexiones activas.

**Ejercicio T6.3: Buscar información acerca de los tipos de ataques más comunes en servidores web, en qué consisten, y cómo se pueden evitar.**

Los ataques a servidores web más comunes son los ataques de inyección, ataques DDoS, de fuerza bruta y Cross Site Scripting.

	-Los ataques de inyección de código consisten en introducir mediante formularios consultas sql a ejecutar en nuestra base de datos, pudiendo conseguir acceso a datos que creíamos seguros. Es uno de los ataues más fáciles de realizar, aunque podemos evitarlos poniendo atención en los lugares donde el usuario nos pasa información, comprobando que no puede realizar de ningún modo una consulta. 
	-La denegación de servicio (DoS) o denegación de servicio distribuida(DDoS) son las formas más comunes para saturar nuestros servidores y paralizar el funcionamiento. Se realizan haciendo que un ordenador intente inundar un servidor con paquetes. En DDoS, los servidores son amenazados por muchos dispositivos distribuidos Se dividen en ataques de volumen, donde el ataque intenta desbordar el ancho de banda, los ataques de protocolo, donde se intentan consumir servicios o recursos de la red y los ataques a aplicaciones, donde las peticiones se hacen para explotar el niver web. La solución a esto consiste en disponer de cortafuegos o un buen sistema de seguridad que identifique rápidamente si se trata de un ataque de denegación de servicio y repeler a la máquina o máquinas que lo estén realizando.
	-Los ataques de Fuerza bruta consisten en probar todas las combinaciones de nombre de usuario y contraseña en una página web. Buscan contraseñas débiles para tener acceso rápidamente. Para evitar esto, lo más sencillo es usar contraseñas que sean seguras.
	-Los ataques de Cross Site Scripting consisten en inyectar en páginas web un código en JavaScript o un lenguaje similar para obtener información de usuarios que confían en esa web sin que ellos se percaten.