**Carlos Toledano Delgado - Joaquín Ballesteros Ortega**

#**Práctica 6. Discos en RAID**

#**Los objetivos concretos de esta práctica son:**
  • Configurar dos discos en RAID 1. Los discos se añadirán a un sistema ya
instalado y funcionando, de forma que en total tendremos tres discos (el
sistema operativo estará ya instalado en /dev/sda y añadiremos dos discos
más, que serán el /dev/sdb y el /dev/sdc, para configurar el dispositivo de
almacenamiento RAID en estos dos discos nuevos de igual tamaño).

  • Hacer pruebas de retirar y añadir un disco “en caliente”, y comprobar que el
RAID sigue funcionando correctamente.

#**1.Configuración del RAID por sofware**

Como se ha indicado, partimos de una máquina virtual ya instalada y configurada a la
que, estando apagada, añadiremos dos discos del mismo tipo y capacidad.

1.Ahora arrancamos la máquina y entramos para instalar el software necesario para
configurar el RAID:

  sudo apt-get install mdadm

2.Debemos buscar la información (identificación asignada por Linux) de ambos discos:

  sudo fdisk -l

3.Ahora ya podemos crear el RAID 1, usando el dispositivo /dev/md0, indicando el
número de dispositivos a utilizar, así como su ubicación:

  sudo mdadm -C /dev/md0 --level=raid1 --raid-devices=2 /dev/sdb /dev/sdc

4.En este punto, el dispositivo se habrá creado con el nombre /dev/md0, sin embargo,
en cuanto reiniciemos la máquina, Linux lo renombrará y pasará a llamarlo
/dev/md127.

5.Una vez creado el dispositivo RAID, y como aún no habremos reiniciado la máquina,
usaremos /dev/md0 para darle formato:

  sudo mkfs /dev/md0

Por defecto, mkfs inicializa un dispositivo de almacenamiento con formato ext2.

6.Ahora ya podemos crear el directorio en el que se montará la unidad del RAID:

  sudo mkdir /dat

  sudo mount /dev/md0 /dat

Podemos comprobar que el proceso se ha realizado adecuadamente, y también los
parámetros con los que Linux ha conseguido montarlo usando la orden:

  sudo mount

7.Para comprobar el estado del RAID, ejecutaremos:
  sudo mdadm --detail /dev/md0

8.Para finalizar el proceso, conviene configurar el sistema para que monte el dispositivo
RAID creado al arrancar el sistema. Para ello debemos editar el archivo /etc/fstab y
añadir la línea correspondiente para montar automáticamente dicho dispositivo
Para obtener los UUID de todos los dispositivos de almacenamiento que tenemos, debemos
ejecutar la orden:
s
  ls -l /dev/disk/by-uuid/

9.Anotaremos el correspondiente al dispositivo RAID que hemos creado. Ahora ya
podemos añadir al final del archivo /etc/fstab la línea para que monte automáticamente
el dispositivo RAID, que será similar a:

UUID=ccbbbbcc-dddd-eeee-ffff-aaabbbcccddd /dat ext2 defaults 0 0

![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA6/img/raid.png)

10.Finalmente, una vez que esté funcionando el dispositivo RAID, podemos simular un
fallo en uno de los discos:

  sudo mdadm --manage --set-faulty /dev/md127 /dev/sdb

También podemos retirar “en caliente” el disco que está marcado como que ha fallado:

  sudo mdadm --manage --remove /dev/md127/dev/sdb

Y por último, podemos añadir, también “en caliente”, un nuevo disco que vendría a
reemplazar al disco que hemos retirado:

  sudo mdadm --manage --add /dev/md127 /dev/sdb

Resultado de agregar disco en caliente, producir fallo y eliminar disco:

![curl](https://github.com/carlillostole/Carlillostole-swap/blob/master/PRACTICA6/img/2.png)


En todo momento podemos obtener información detallada del estado del RAID y de
los discos que lo componen.
