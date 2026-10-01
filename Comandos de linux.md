## COMANDOS DE LINUX
Un comando Linux es un programa o utilidad que se ejecuta en la línea de comandos. Una línea de comandos es una interfaz que acepta líneas de texto y las procesa en forma de instrucciones para tu ordenador 

Un flag es una forma de pasar opciones al comando que se ejecuta, la mayoría de los comandos de LINUX tienen una pagina de ayuda que podemos llamar con la flag (-h). La mayoría de las veces las flags son opcionales.

Un argumento o parámetro es la input que debemos a un comando para que puedan ejecutarse correctamente, en su matoria de los casos, el argumento es una ruta de archivos.

Se puede invocar flags utilizando (-) y (--) mientras que la ejecución de los argumentos dependen del orden en que los pase a la función

**COMANDOS**

1.- **ls**
Comando principal- Permite listar el contenido del directorio que quieras. Tiene muchas opciones, por lo que es bueno obtener ayuda usando la flag (--help)

2.- **Alias**
Comando alias, permite definir alias temporales en tu sesión de Shell. al crear un alias, se indica al Shell que sustituya una palabra por una serie de comandos 

3.- **unalias**
Comando que tiene como objetivo eliminar un alias de los ya definidos

4.- **pwd**
Imprimir el directorio de trabajo, muestra la ruta absoluta del directorio en el que se encuentra 

ejemplo: US=Andres == /home/Andres/Documents

5.- **cd**
Comando popular, junto con (ls) es el cambio de directorio, como su nombre lo indica, cambia el directorio al que se intenta acceder.

cd videos ó cd /home/kinsta/Documents/Videos

cd - carpeta de inicio
cd -- sube nivel
cd - vuelve al directorio anterior

6.- **cp**
Copia archivos y carpetas directamente en el terminal de Linux que a veces puede sustituir a los gestores de archivos convencionales, se debe de utilizar el comando cp se debe escrirbi junto con los archivos de origen y destino.

- cp file_to_copy.txt new_file.txt
- cp -r dir_to_copy/ new_copy_dir/

7.- **rm**
Comando para eliminar archivos y directorios
- rm file_to_copy.txt
- rm -r dir_to_remove/

para eliminar un directorio con contenido en su interior, es necesario utilizar flag forcé (-f) y recursive
- rm -rf dir_with_content_to_remove/

8.- **mv**
Comando para mover o renombrar archivos y directorios en el sistema de archivos 

para que se utilice el comando se debe de escribir el nombre con los archivos de origen y destino

-mv source_file destination_folder/

-mv command_list.txt commands/

para las rutas absolutas utilizarías 
mv /home/kinsta/BestMoviesOfAllTime ./

donde ./ es el directorio en que te encuentras

También se puede usar mv para renombrar archivos mientras los mantienes en el mismo directorio-

- mv old_file.txt new_named_file.txt

9.- **mkdir**

Para crear carpetas en el Shell se utilizara el comando mkdir, solo tienes que especificar el nombre de la nueva carpeta (asegurando que NO existe)
- mkdir images/
Para la creación de subdirectorios, usando flag padre (-p)

10.- **man**
Muestra la pagina del manual de cualquier otro comando
- man mkdir

11.- **touch**
Permite actualizar los tiempos de acceso y modificación de los archivos especificados 

- touch -m old_file

Aun que la mayoría de las veces no se utilizara touch para modificar las fechas de los archivos, si no para crear nuevos archivos vacíos

- touch new_file_name

12.- **chmod**
Permite cambiar el modo de un archivo (permisos) rápidamente, tiene varias opciones disponibles con el.
Los permisos básicos que puede tener un archivo son
	-r (leer)
	-w (escribir)
	-x (ejecutar)
El caso mas común de chmod es hacer que un archivo sea ejecutable por el usuario, para esto se escribe chmod y el flag (+x) seguido del archivo en el que desea modificar los permisos

- chmod +x script

13.- **./**
Aun que no sea un comando en si mismo, permite a nuestro Shell ejecutar un archivo ejecutable con cualquier interprete instalado en nuestro sistema directamente desde el terminal. 

Ejemplo, puedes ejecutar un script phyton o un programa en formato .run, como XAMPP, solo asegurarse que cuando se ejecute un ejecutable tenga los permisos de ejecución (x) que se pueden modificar con el comando chmod


14.- **exit**
Comando con el cual se puede terminar una sesión de Shell, en la mayoría de los casos, cerrar automáticamente el terminal que se esta utilizando

15.- **SUDO**
superuser do - permite actuar como superusuario o usuario root, mientras se ejecuta un comando especifico, es la forma en que Linux se protege y evita que los usuarios modifiquen accidentalmente el sistema de archivos de la maquina o instalen paquetes inapropiados 

Utilizado comúnmente para instalar software o para edición de archivos fuera del escritorio personal del usuario.
	-sudo apt install gimp

	-sudo cd /root/ 

Pedirá la contraseña de admin antes de ejecutar el comando que se haya escrito después


16.- **shutdown**
Comando que permite apagar la maquina, aun que, también puede utilizarse para detenerla y reiniciarla 

Para apagar el ordenador inmediatamente (el valor predeterminado es 1 min)
	-shutdown now

También se puede programar el apagado del sistema de un formato de 24 horas:
	-shutdown 20:40
Para cancelar una llamada de shutdown anterior, puedes utilizar el flag -c
 	-shutdown -c

17.- **htop**
visor de procesos interactivo que permite la gestión de recursos de la maquina directamente desde la terminal, aun que, en la mayoría de los casos no se encuentra instalado de forma predeterminada.

18.- **unzip**
Permite la extracción de contenido de un archivo .zip desde el terminal, también puede que no venga instalado por defecto, se deberá instalar desde el gestor de paquetes
	- unzip images.zip

19.- **apt, yum, pacman**
Independientes de la distribución que se utilicen gestores de paquetes para instalar, actualizar y eliminar el software que se usa a diario
	-DEBIAN (Ubuntu, Mint)
		- sudo apt install gimp
	-RED HAT (Fedora, CentOS)
		- sudo yum install gimp
	-ARCH (Manjaro, Arco Linux)
		- sudo pacman -S gimp

20.- **echo**
Muestra el texto definido en la terminal 

echo "cool message"
 -cool message

Su uso principal es imprimir las variables de entorno dentro de esos mensajes

	-echo "Hey $USER"
	-Hey kinsta

21.- **cat**

Abreviatura de (concatenate), permite crear, visualizar y concatenar archivos directamente desde el terminal, se utiliza principalmene para previsualizar un archivo sim abrir un editor de texto grafico
-cat long_text_file.txt

22.- **ps**

Puedes echar un vistazo a los procesos que tu sesión de Shell actual este ejecutando, imprime información útil sobre los programas que esta ejecutando como el ID de proceso, el TTY, la hora y el nombre del comando

23.- **kill**
Señal de TERM o kill a un proceso que lo termina.
Puedes matar procesos introduciendo el PID (PROCESS ID) o nombre binaro de programa
	- kill 533494

	- kill Firefox


24.- **ping**
Prueba la conectividad de la red, comúnmente se utilizara para solicitar un dominio o una IP
	-ping Google.com
	-8.8.8.8

25.- **vim**
Editor de texto de terminal libre y de código abierto que se utiliza desde los 90, permite la edición de texto plano utilizando combinaciones de teclas diferentes
	-vim

26.- **history**
Muestra una lista enumerada con los comando utilizados en el pasado

27.- **passwd**
Permite el cambo de contraseñas de las cuentas de los usuarios, como primer punto pide introducir la contraseña actual y posterior una nueva contraseña con su confirmación
	-psswd

28.- **which**
Muestra la ruta completa de los comandos del Shell, si no puede reconocer e comando dado, dará error
	- which Python
		- /usr/bin/python
	- wich brave
		- /usr/bin/brave

29.- **shred** 
Este comando anula el contenido de un archivo permanentemente (el archivo se vuelve extremadamente difícil de recuperar)
	-cat file_to_shred.txt

30.- **less**
(opuesto a more) programa que permite inspeccionar archivos hacia a delate y atrás
	-less large_txt_file.txt

31.- **tail**
Similar a cat, tail imprime el contenido de un archivo con una advertencia importan, solo imprime las ultimas líneas (por defecto imprime las ultimas 10 lineas), pero se puede modificar con (-n)
	-tail -n 4 long.txt

32.- **head**
Contrario a tail, muestra las primeras 10 líneas del archivo de texto, al igual (-n) para mostrar cualquier numero de las líneas del texto.
	-head -n 6 long.txt

33.- **grep**
Utilidades mas potentes para trabajar con archivos de texto, busca líneas que coincidan con una expresión regular y las imprime. = (cntrl + f)
También puede contar el numero de veces que se repite el patron utilizando (-c)
	-grep "linux" long.txt
	-grep -c "linux" long.txt

34.- **whoami**
Comando que muestra el nombre de usuario actualmente en uso.
	-whoami
Se obtendría el mismo resultado usando echo.
	-echo $USER

35.- **whatis**
Imprime una descripción de una sola linea de cualquier otro comando.
	-whatis python

# python (1) - an interpreted, interactive, object-oriented programming language

	-whatis whatis

# whatis (1) - display one-line manual page descriptions

36.- **wc**
(Word count)-recuento de palabras, devuelve el numero de palabras de un archivo de texto.
	-wc long.txt

# 37 207 1000 long.txt

-37 líneas
-207 palabras
-1000 bytes de tamaño
-El nombre del archivo (long.txt)
Si solo necesitas el número de palabras, utiliza el indicador -w:
	- wc -w long.txt

207 long.txt

37.- **uname** 
unix name- imprime la información del sistema operativo, lo cual resulta útil cuando se conoce la versión actúa de Linux; Aun que la mayoría de veces, se utiliza la flag (-a = all).
	-uname

Linux
	- uname -a

-Linux kinstamanjaro 5.4.138-1-MANJARO #1 SMP PREEMPT Thu Aug 5 12:15:21 UTC 2021 x86_64 GNU/Linux
 
38.- **neofetch**
Herramienta CLI, que nos muestra información sobre el sistema.
-versión de kernel
-Shell
-hardware
-ASCII de la distro de Linux
-neofetch

39.- **find** 
El comando find nos busca archivos en una jerarquía de directorios, basándose en una expresión regex.
	- find [flags] [path] -name [expression]

40- **wget**
world wide web get, es una utilidad para recuperar contenidos de interne

	- wget https://raw.githubusercontent.com/DaniDiazTech/Object-Oriented-Programming-in-Python/main/object_oriented_programming/cookies.py

##COMANDOS PRINCIPALES PARA PRINCIPANTES
-find = "buscar dentro de mi PC/VM".
-wget = "descargar desde Internet".
-cat = "ver el contenido".
-mkdir = "crear carpetas".
-cp = "copiar archivos".
-mv = "mover o renombrar archivos".
-rm = "eliminar archivos".



https://kinsta.com/es/blog/linux-comandos/
