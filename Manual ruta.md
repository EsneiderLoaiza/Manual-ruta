<pre><code>		 MANUAL DE INSTALACIÓN DE RUTA EN XUBUNTU  20.04

				REALIZADO POR: 
			DAVID ESNEIDER LOAIZA VANEGAS


			INTELLIGENT ELECTRONIC SOLUTIONS


				  MEDELLÍN



				     2021
</code></pre>
<h2 id="tabla-de-contenido">Tabla de contenido</h2>
<p>Introducción	<br>
Objetivo	<br>
Comparativa de sistemas operativos a tener en cuenta	<br>
Selección de sistema operativo Xubuntu 20.04</p>
<ol>
<li>Descarga de Xubuntu_20.04.iso</li>
<li>Descarga de Balena Etcher</li>
<li>Instalar Xubuntu 20.04</li>
<li>Preparando entorno gráfico</li>
<li>Instalación de Docker</li>
<li>Crear archivo 10_ies.rules</li>
<li>Instalar Qt</li>
<li>Instalar mysql-client</li>
<li>Instalar psmsic</li>
<li>Descarga e instalación de AnyDesk</li>
<li>Eliminar carpetas y archivos innecesarios</li>
<li>Archivos libICT_bills.s…</li>
<li>Archivo kbitech_ICT</li>
<li>Instalar alsa-utils</li>
<li>Archivo autostart</li>
<li>Carpeta RUTA</li>
<li>Carpeta db</li>
<li>Archivos manager, configuration, genericModals, docker-clean, docker compose</li>
<li>Librerías necesarias</li>
<li>Archivo ttys_enable.sh</li>
<li>Archivo ttys-enable.service</li>
<li>Archivo billetero.ini</li>
<li>Archivo <a href="http://autoverificacion.sh">autoverificacion.sh</a></li>
<li>Archivo Crontab</li>
<li>Carpeta Documents</li>
<li>Montar contenedores de Docker</li>
<li>Pantalla de carga</li>
<li>Probando estado</li>
</ol>
<h2 id="introducción">Introducción</h2>
<p>Este es un manual en el que se explicará paso a paso  cada ejecución a realizar para una correcta compresión</p>
<h2 id="objetivo">Objetivo</h2>
<p>Realizar la instalación de ruta desde cero, así como comprender cada paso, comando y programa a instalar en el equipo para una correcta función a la hora de sacarlo a producción</p>
<h2 id="comparativa-de-sistemas-operativos-a-tener-en-cuenta">Comparativa de sistemas operativos a tener en cuenta</h2>
<p><strong>Xubuntu</strong><br>
•	800 Mhz de CPU<br>
•	256 MB de RAM<br>
•	6 GB de disco</p>
<p><strong>Linux Lite</strong><br>
•	160Mhz de CPU<br>
•	768 MB de RAM<br>
•	8 GB de disco</p>
<p><strong>Zorin OS Lite</strong><br>
•	700Mhz de CPU<br>
•	512 de RAM<br>
•	8 GB de disco</p>
<p><strong>Arch Linux</strong><br>
•	512 MB de RAM<br>
•	800 MB de disco</p>
<p><strong>Helium</strong><br>
•	Basada en Debian 9<br>
•	Gestor de ventanas OpenBox<br>
•	256 MB de RAM<br>
•	10 GB de disco</p>
<p><strong>Porteus</strong><br>
•	256 de RAM<br>
•	300 MB de disco<br>
•	Entorno grafico OpenBox</p>
<p><strong>Connochaet OS</strong><br>
•	Gestor de ventanas iceWM<br>
•	Disponible solo x86<br>
•	Procesador i686<br>
•	128 MB de RAM<br>
•	3 GB de disco</p>
<p><strong>Puppy Linux</strong><br>
•	128MB de RAM<br>
•	233Mhz de CPU</p>
<p><strong>AntiX</strong><br>
•	Disponible para x86<br>
•	266 Mhz de CPU<br>
•	256 MB de RAM<br>
•	2.7 GB de disco</p>
<h2 id="arquitecturafuncionamiento-de-ruta">Arquitectura/funcionamiento de ruta</h2>
<p>Selección de sistema operativo Xubuntu 20.04<br>
Seleccionamos Xubunto por los pocos requsitos que necesita y porque este es basado en Ubuntu ecesitamos Descarga Xubuntu.iso y un programa que nos boote la USB(Que debe estar formateada, sin ningún archivo), que será Balena Etcher, esto lo haremos a continuación:</p>
<h2 id="descarga-de-xubuntu_20.04.iso">1. Descarga de Xubuntu_20.04.iso</h2>
<p><strong>Link y servidor</strong><br>
Vamos al siguiente link <a href="https://xubuntu.org/download/">https://xubuntu.org/download/</a> y elegimos el servidor más cercano, en este caso es United States, damos clic</p>
<p><strong>Selección de iso</strong><br>
Nos aparecé la siguiente venta con el siguiente link <a href="http://mirror.us.leaseweb.net/ubuntu-cdimage/xubuntu/releases/20.04/release/">http://mirror.us.leaseweb.net/ubuntu-cdimage/xubuntu/releases/20.04/release/</a><br>
Elegimos el formato .iso para iniciar descarga</p>
<p><strong>Descarga de iso</strong><br>
He iniciará la descarga en la parte inferior izquierda de la pantalla</p>
<h2 id="descarga-de-balena-etcher">2. Descarga de Balena Etcher</h2>
<p><strong>Link de descarga</strong><br>
Para poder booter la USB necesitaremos este programa, la descarga la haremos del siguiente link <a href="https://www.balena.io/etcher/">https://www.balena.io/etcher/</a> donde daremos clic en Download</p>
<p><strong>Crear booteable de Xubuntu 20.04</strong><br>
Ejecutamos el programa una vez hayamos extraído el archivo y nos aparecerá la siguiente ventana</p>
<p><strong>Selección de iso y USB</strong><br>
Seleccionamos la iso y la USB</p>
<p><strong>Iniciar flash</strong><br>
Una vez este todo listo, clic en Flash</p>
<p><strong>Proceso de boot</strong><br>
Iniciará a crear la USB booteable</p>
<h2 id="instalar-xubuntu-20.04">3. Instalar Xubuntu 20.04</h2>
<p>Reiniciamos el equipo y presionamos la tecla indicada(Dependiente el equipo puede varias entre F1-F4 y F9-F11, también podría ser ESC) para elegir que boot iniciar de arranque, que será la USB en este caso y poder instalar Xubuntu</p>
<p><strong>Carga de inicio de instalación</strong><br>
Nos aparecerá la siguiente pantalla mientras se prepara para mostrarnos las opciones de instalación</p>
<p><strong>Selección de idioma</strong><br>
Una vez este todo cargado y nos arroje lo siguiente, seleccionamos idioma de preferencia y clic en instalar Xubuntu</p>
<p><strong>Selección de idioma y configuración de teclado</strong><br>
Seleccionamos de nuevo idioma y la opción de teclado a la que mejor nos acomodemos</p>
<p><strong>Descarga de actualizaciones</strong><br>
Dejamos seleccionado “Descargar actualizaciones al instalar Xubuntu”(Esto si se tiene el cable de red conectado en el equipo) y clic en continuar</p>
<p><strong>Borrar disco e instalar</strong><br>
Para este caso que el equipo ya tenía información, marcamos la opción “Borrar disco e instalar Xubuntu” después clic en “Instalar ahora”</p>
<p><strong>Escribir cambios en disco</strong><br>
Justo nos aparecerá una ventana donde nos consulta si deseamos escribir los cambios en el disco, damos clic en “Continuar”</p>
<p><strong>Selección de capital</strong><br>
Elegimos capital de nuestro país, en este caso es “Bogotá”</p>
<p><strong>Ingreso de usuario y clave</strong><br>
Nos pedirá ingresar un nombre  y una contraseña, para este caso como nombre le ponemos “<code>ruta</code>” y como clave “<code>ruta123*.*</code>”, también debemos dejar seleccionado la opción “Iniciar sesión automáticamente”</p>
<p><strong>Iniciar instalación</strong><br>
Justo después de eso iniciará la instalación mostrando la siguiente ventana</p>
<p><strong>Reinicio de equipo</strong><br>
Una vez haya finalizado nos pedirá reiniciar, damos clic ahí para comenzar</p>
<p><strong>Retiro de USB</strong><br>
Cuando el equipo reinicie nos aparecerá la siguiente ventana con un mensaje donde nos pedirá retirar la USB y presionar “Enter”</p>
<p><strong>Escritorio de Xubuntu</strong><br>
Ya nos mostrará el escritorio de Xubuntu</p>
<h2 id="preparando-entorno-grafico">4. Preparando entorno grafico</h2>
<p>Necesitamos instalar un entorno grafico que consuma menos recursos y eliminar el actual, para este caso usaremos Openbox</p>
<p><strong>Instalar Openbox y Obconf</strong><br>
Openbox es un entorno de escritorio completamente vació, esto para aprovechar mejor los recursos del equipo.<br>
Obconf es un programa creado para OpenBox que nos permite configurar las ventanas como asignarle temas y configurar los lanzadores.<br>
Para la instalación de ambos abrimos la consola de comandos, tan fácil como dar clic derecho en escritorio y seleccionar “Abrir terminal aquí”<br>
Escribimos el comando:</p>
<pre><code>sudo apt-get install openbox obcon
</code></pre>
<p><strong>Elegir Openbox como entorno grafico</strong><br>
Cerramos sesión, vamos a la parte superior y clic sobre el icono para que se desplieguen los entorno gráficos, elegimos Openbox e iniciamos sesión de nuevo ingresando las credenciales</p>
<p><strong>Openbox</strong><br>
Una vez inicie el escritorio tendremos una pantalla complemente en negro donde las opciones, aplicaciones, etc se desplegarán con clic derecho(Si no aparece pantalla en negro sino otro fondo, es porque nos falta desinstalar los otros entornos gráficos)</p>
<p><strong>Desinstalar entornos graficos</strong><br>
Debemos quitar los demás entornos y dejar solo Openbox, esto lo hacemos con el comando</p>
<pre><code>sudo apt-get purge libxfce4util-common
</code></pre>
<p><strong>Instalar aptitude e ingresar como superusuario</strong><br>
Primero pasamos a ingresar como super usuario para tener mayor privilegio y permisos, esto con el comando</p>
<pre><code>sudo su
</code></pre>
<p>Aptitude nos servirá para instalar lo que necesitamos, pero a diferencia de apt-get, aptitude instala lo que se pide y las dependencias/librerías si así se requieren, para instalarlo, se hace con el comando</p>
<pre><code>apt-get install aptitude
</code></pre>
<p><strong>Instalar pcmanfm</strong><br>
Este es el explorador de archivos, para tener una vista más grafica de acceso a los archivos y no solo vía consola, para instalarlo, usaremos el comando</p>
<pre><code>sudo aptitude install pcmanfm
</code></pre>
<p><strong>Instalar gnome-terminal</strong><br>
Si deseamos una terminal que a la vista sea un poco más agradable, podemos usar gnome-terminal, para la instalación de esta usaremos el comando</p>
<pre><code>sudo aptitude install gnome-terminal
</code></pre>
<p>Ahora podemos usar la actual o gnome terminal que tendría una vista así:</p>
<p>Verificar permisos de archivos sudores<br>
Para esto debemos ingresar a la ruta y archivo especifico con el comando</p>
<pre><code>sudo nano /etc/sudores
</code></pre>
<p>Estando dentro del archivo si vemos algo que diga admin lo comentamos poniendo un # antes del texto, ingresamos lo siguiente:</p>
<pre><code>#User privilege specification root    
ALL=(ALL:ALL) ALL ruta ALL=(ALL:ALL) ALL
#Allow members of group sudo to execute any command 
%sudo   ALL=(ALL:ALL) ALL
</code></pre>
<p><strong>Instalar Lightdm</strong><br>
Es un gestor de sesiones, esa parte en la que nos pide el usuario y clave para acceder a nuestro perfil de sistema operativo, es eso, un entorno grafico para la sesión.<br>
Este se instala con el siguiente comando</p>
<pre><code>sudo apt-get install lightdm
</code></pre>
<p>Ingresar al archivo lightdm.conf con el comando</p>
<pre><code>sudo nano /etc/lightdm/lightdm.conf
</code></pre>
<p>Pondremos lo siguiente:</p>
<pre><code>[SeatDefaults] 
autologin-user = ruta 
autologin-user-timeout=0
</code></pre>
<p>Y guardaremos lo escrito con Ctrl + o, presionamos “Enter” y por ultimo para salir Ctrl + x</p>
<p><strong>Instalar y actualizar x11-xserver-utils</strong><br>
Es un servidor grafico para las personas que no quieren utilizar solo linea de comandos, antes de instalar, debemos actualizar con el comando</p>
<pre><code>sudo apt-get update
</code></pre>
<p><strong>Instalación</strong><br>
Ahora los instalamos con el comando</p>
<pre><code>   sudo apt-get install x11-xserver-utils
</code></pre>
<p>**</p>
<h2 id="instalación-de-docker">5. Instalación de Docker</h2>
<p>Docker es una herramienta para estandarizar software y no corra en un solo equipo(típica situación) que usa contenedores para almacenar un programa(imagen), en estos mismos contenedores están las librerías necesarias para que el programa se puede ejecutar de forma correcta. La instalación la hacemos desde el link <a href="https://docs.docker.com/engine/install/ubuntu/">https://docs.docker.com/engine/install/ubuntu/</a><br>
<strong>Instalar Docker Engine</strong><br>
Debemos usamos el repositorio HTTP, para esto, usamos el comando</p>
<pre><code>sudo apt-get install \
apt-transport-https \
ca-certificates \
curl \
gnupg \
lsb-release
</code></pre>
<p>Agregamos la llave GPG con el comando:</p>
<pre><code> curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
</code></pre>
<p>Agregamos repositorio estable</p>
<pre><code>echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list &gt; /dev/nul
</code></pre>
<p>Antes que nada, debemos actualizar con el comando<br>
<code>sudo apt-get update</code></p>
<p>Ahora para instalar el docker usamos el comando</p>
<pre><code>sudo apt-get install docker-ce docker-ce-cli containerd.io
</code></pre>
<p><strong>Instalar Docker Compuse</strong><br>
Para hacerlo, vamos a <a href="https://docs.docker.com/compose/install/">https://docs.docker.com/compose/install/</a> Ejecutaremos la siguiente linea para descargar una versión estable con el comando</p>
<pre><code>sudo curl -L "https://github.com/docker/compose/releases/download/1.29.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
</code></pre>
<p>Ahora daremos permisos de ejecución al docker con el comando</p>
<pre><code>sudo chmod +x /usr/local/bin/docker-compose
</code></pre>
<p>Verificamos la versión del docker con el comando</p>
<pre><code>docker-compose --version
</code></pre>
<h2 id="crear-archivo-10_ies.rules">6. Crear archivo 10_ies.rules</h2>
<p>Este archivo necesita ejecutar ciertas ordenes pero primero debemos ir a la ubicación con el comando cd /etc/udev/rules.d y creamos el archivo que por nombre tendrá 10_ies,rules con el comando</p>
<pre><code>sudo nano 10_ies.rules
</code></pre>
<p>Nos aparece la siguiente ventana donde pondremos</p>
<pre><code>KERNEL=="js*", SUBSYSTEM=="input", ATTRS{idVendor}== "0079", ATTRS{idProduct}=="0006",
SYMLINK+=”ies/key%n”, MODE:=”0666”
</code></pre>
<p>Estando dentro del archivo para guardar cambios Ctrl + o, presionamos “Enter” y para salir Ctrl + x</p>
<h2 id="instalar-qt">7. Instalar Qt</h2>
<p>Este los descargaremos de <a href="https://www.qt.io/download-qt-installer?hsCtaTracking=99d9dd4f-5681-48d2-b096-470725510d34%7C074ddad0-fdef-4e53-8aa8-5e8a876d6ab4">https://www.qt.io/download-qt-installer?hsCtaTracking=99d9dd4f-5681-48d2-b096-470725510d34|074ddad0-fdef-4e53-8aa8-5e8a876d6ab4</a><br>
Nos redireccionará a la siguiente pagina donde daremos clic en el botón verde Download<br>
Tener presente que la instalación se hará en la ruta /home/ruta/Documents/qt(Las carpetas Documents y qt no están, las creamos más adelante)</p>
<p>Elegimos “Save File” y clic en “ok”</p>
<p>Ahora verificamos que el archivo descargado este en la carpeta Descargas, sobre esta carpeta, escribimos el comando <code>ls</code> que nos servirá para ver lo que tenemos ahí</p>
<p>Damos permisos de ejecución a qt con el comando</p>
<pre><code>sudo chmod +x qt-unified-linux-x64-4.1.0-online.run
</code></pre>
<p>Ejecutamos el archivo con el comando</p>
<pre><code>./Nombre de archivo, así: ./qt-unified-linux-x64-4.1.0-online.run
</code></pre>
<p>Se abrirá la siguiente ventana, donde ingresaremos las credenciales correspondientes</p>
<p>Dejamos seleccionado la opción que empieza con “I have read” y clic en “Next”</p>
<p>Clic en “Next”</p>
<p>Dejamos seleccionada la opción que empieza “Help us” y clic en “Next”</p>
<p>Debemos abrir una terminal nueva para crear la carpeta Documents y qt, estando sobre la carpeta ruta las creamos con el comando mkdir Documents, después ingresamos a Documents con el comando cd Documents/ y creamos carpeta qt con el comando mkdir qt</p>
<p>Ahora volviendo a Qt, elegimos la dirección /home/ruta/Documents/qt/ y seleccionamos la opción Custom installation</p>
<p>Estando en esta parte, seleccionamos solo Archive y clic en Filter, comenzará a cargar</p>
<p>Aparece lo siguiente, desplegamos Qt</p>
<p>Seleccionamos Qt 5.9.2 y clic en “Next”</p>
<p>Seleccionamos la opción que inicia “I have read” y clic en “Next”</p>
<p>Clic en install para iniciar la instalación</p>
<p>La instalación puede tomar varios minutos, esto sería lo que deberíamos estar viendo</p>
<p>Una vez haya terminado la instalación, desmarcamos la opción de Launch y clic en “Finish”</p>
<h2 id="instalar-mysql-client">8. Instalar mysql-client</h2>
<p>Para iniciar la instalación lo haremos con el siguiente comando</p>
<pre><code>sudo apt-get install mysql-client
</code></pre>
<p>Ahora vamos a instalar la librería que este necesita, con el siguiente link iniciará la descarga automáticamente <a href="https://repo.mysql.com/apt/ubuntu/pool/mysql-5.7/m/mysql-community/libmysqlclient20_5.7.33-1ubuntu18.04_amd64.deb">https://repo.mysql.com/apt/ubuntu/pool/mysql-5.7/m/mysql-community/libmysqlclient20_5.7.33-1ubuntu18.04_amd64.deb</a><br>
Seleccionamos “Save File” y clic en “Ok”.</p>
<p>Ahora pasamos a ejecutar el comando</p>
<pre><code>sudo dpkg -i libmysqlclient20_5.7.33-1ubuntu18.04_amd64.deb
</code></pre>
<p>Esto para instalar  mysql-apt-config deb, para que se ejecute sin problemas, debemos ejecutar ese comando desde la carpeta donde se descarga, para este caso, desde Descargas</p>
<p>Actualizamos los paquetes con el comando</p>
<pre><code>sudo apt-get update
</code></pre>
<p>Y ahora instalamos libmysqlclient20 con el comando</p>
<pre><code>sudo apt-get install libmysqlclient20
</code></pre>
<h2 id="instalar-psmsic">9. Instalar psmsic</h2>
<p>Usaremos el comando</p>
<pre><code>sudo aptitude install psmisc
</code></pre>
<h2 id="descarga-e-instalación-de-anydesk">10. Descarga e instalación de AnyDesk</h2>
<p>Para iniciar descarga ingresaremos al siguiente link <a href="https://anydesk.com/es/downloads/linux">https://anydesk.com/es/downloads/linux</a> donde daremos clic en Descargar ahora, clic en Ubuntu 64</p>
<p>Clic en “Guardar archivo” y “Aceptar”</p>
<p>Iniciamos instalación con el comando</p>
<pre><code>sudo dpkg -i anydesk_6.1.1-1_amd64.deb 
</code></pre>
<p>(Este ultimo es el nombre del archivo descargado)</p>
<p>Nos aparece incompleto por falta de librerias, para terminarlo de buena forma, ponemos el comando</p>
<pre><code>sudo apt -f install 
</code></pre>
<p>hecho eso, ya tendríamos el anydesk instalado</p>
<p>Ya podemos ejecutar AnyDesk sin problemas, tendremos esta ventanas</p>
<h2 id="eliminar-carpetas-y-archivos-innecesarios">11. Eliminar carpetas y archivos innecesarios</h2>
<p>Hay cosas que queda por fuera de lo necesarios, para nuestro caso eliminaremos varias cosas que están en ruta con el siguiente comando</p>
<pre><code>sudo rm -r 2021-04-15-101335_1920x1080_scrot_000.png  2021-04-15-101335_1920x1080_scrot.png Documentos Imágenes Público Música Vídeos Escritorio Plantillas
</code></pre>
<h2 id="archivos-libict_bills.s…">12. Archivos libICT_bills.s…</h2>
<p>Estos archivos debemos ubicarlos en la ruta <code>/usr/lib/</code> antes de pasarlos a esta ruta, debemos ir primero a donde estén los archivos actualmente, para moverlos todos, lo haremos con el comando</p>
<pre><code>sudo mv libICT_bill.s* /usr/lib/
</code></pre>
<p>Debemos darle permisos de ejecución a estos archivos con el comando</p>
<pre><code>sudo chmod +x libICT_bill.s*
</code></pre>
<p>También debemos verificar pertenezca a grupo y propietario root, esto con el comando <code>ls -l</code> escrito este comando nos aparecerá una lista de todos los archivos con su respectivo propietario y los permisos</p>
<p>Suponiendo que para este caso no tuvieran grupo y propietario root, el cambio de este lo haríamos con el comando</p>
<pre><code>sudo chown root:root libICT_bills.s*
</code></pre>
<h2 id="archivo-kbitech_ict">13. Archivo kbitech_ICT</h2>
<p>Este archivo debe tener todos los permisos, para esto usamos el siguiente comando</p>
<pre><code>sudo chmod 777 kbitech_ICT
</code></pre>
<p>Una vez hecho esto, debemos ubicarlo en la siguiente ruta <code>/usr/include</code> esto con el comando</p>
<pre><code>sudo mv kbitech_ICT /usr/include
</code></pre>
<p>Por ultimo, debemos verificar que kbitech_ICT pertenezca a grupo y propietario root, esto con el comando <code>ls -l</code> si pertenece a otro como ruta, lo cambiamos con el comando</p>
<pre><code>sudo chown root:root  kbitech_ICT
</code></pre>
<h2 id="instalar-alsa-utils">14. Instalar alsa-utils</h2>
<p>Este archivo es importante para ruta, debemos instalarlo con el siguiente comando</p>
<pre><code>sudo apt-get install alsa-utils
</code></pre>
<h2 id="archivo-autostart">15. Archivo autostart</h2>
<p>Este archivo debemos moverlos a la ruta <code>.config/openbox</code> pero antes, la carpeta openbox no está creada, primero vamos a la ruta con el comando <code>cd .config</code> y creamos la carpeta con el comando <code>mkdir openbox</code>(si no permite por permisos lo hacemos con <code>sudo mkdir openbox</code>) ahora vamos a la ubicación del archivo autostart y lo movemos con el comando</p>
<pre><code>sudo mv autostart .config/openbox
</code></pre>
<p>A este archivo debemos dar grupo y propietario ruta, esto con el comando</p>
<pre><code>sudo chown ruta:ruta autostart
</code></pre>
<p>También debemos darle permisos de ejecución, esto con el comando</p>
<pre><code>sudo chmod +x autostart
</code></pre>
<h2 id="carpeta-ruta">16. Carpeta RUTA</h2>
<p>Debemos ubicar RUTA en la siguiente dirección <code>/home/ruta</code> esto con el comando</p>
<pre><code>sudo mv RUTA /home/ruta
</code></pre>
<p>Dar a como grupo y propietario a ruta con el comando</p>
<pre><code>sudo chown ruta:ruta RUTA
</code></pre>
<p>Por ultimo, debemos dar permisos de ejecución y demás a los archivos dentro de RUTA, con los siguientes dos comandos</p>
<pre><code>chmod +x /home/ruta/RUTA/*/*.x86_64

chmod 777 /home/ruta/RUTA/*/*/*/*.xml
</code></pre>
<h2 id="carpeta-db">17. Carpeta db</h2>
<p>Debemos crear una carpeta llamada db, esto debemos hacerlo en la ruta <code>/home/ruta/RUTA</code> esto con el comando <code>mkdir db</code> hecho esto, correremos el siguiente comando para los permisos</p>
<pre><code>sudo chown -R 999:docker db
</code></pre>
<h2 id="archivos-manager-configuration-genericmodals-docker-clean-docker-compose">18. Archivos manager, configuration, genericModals, docker-clean, docker compose</h2>
<p>Estos archivos deben estar en la siguiente ruta <code>/usr/local/bin</code> los moveremos con el comando</p>
<pre><code>sudo mv manager configuration genericModals docker-clean docker compose /usr/local/bin
</code></pre>
<p>Ahora debemos dar permisos de ejecución con el comando</p>
<pre><code>sudo chmod +x  manager configuration genericModals docker-clean docker compose 
</code></pre>
<p>(Si no funciona, los permisos se deberán dar uno a uno)</p>
<p>También pondremos como propietario y de grupo el usuario ruta con el comando</p>
<pre><code>sudo chown ruta:ruta manager configuration genericModals docker-clean docker compose 
</code></pre>
<p>(Si no funciona, los permisos se deberán dar uno a uno)</p>
<h2 id="librerías-necesarias">19. Librerías necesarias</h2>
<p>Nos hacen falta las siguientes librerías por instalar para un correcto funcionamiento, esto lo haremos con los comandos:</p>
<p>Empezamos con las que necesitar MANAGER<br>
con el comando</p>
<pre><code>sudo aptitude install libqt5printsupport5
</code></pre>
<p>La siguiente con el comando</p>
<pre><code>sudo aptitude install libqt5serialport5
</code></pre>
<p>Y la ultima para MANAGER:</p>
<pre><code>sudo aptitude install libqt5websockets5
</code></pre>
<p>Ahora seguimos con CONFIGURACION instalando la librería necesaria con el comando</p>
<pre><code>sudo aptitude install libqt5sql5
</code></pre>
<p>Ahora seguimos con GENERICMODALS con el comando</p>
<pre><code>sudo aptitude install libqt5quick5
</code></pre>
<p>También con el comando</p>
<pre><code>sudo aptitude install qml-module-qtmultimedia
</code></pre>
<p>Y por ultimo con el comando</p>
<pre><code>sudo aptitude install qml-module-qtquick-window2
</code></pre>
<h2 id="archivo-ttys_enable.sh">20. Archivo ttys_enable.sh</h2>
<p>Este archivo debemos moverlo a la ruta <code>/usr/bin</code> esto con el comando</p>
<pre><code>sudo mv ttys_enable.sh /usr/bin
</code></pre>
<p>Damos permisos de ejecución con el comando</p>
<pre><code>sudo chmod +x ttys_enable.sh
</code></pre>
<p>Verificamos que pertenezca a grupo y propietario root con el comando <code>ls -l</code> en la ruta del archivo</p>
<h2 id="archivo-ttys-enable.service">21. Archivo ttys-enable.service</h2>
<p>Moveremos el archivo a la siguiente ruta <code>/etc/systemd/system/</code> con el comando</p>
<pre><code>sudo mv ttys-enable.service
</code></pre>
<p>Damos permisos de ejecución con el comando</p>
<pre><code>sudo chmod +x ttys-enable.service
</code></pre>
<p>Verificamos que pertenezca a grupo y propietario root con el comando <code>ls -l</code> en la ruta del archivo</p>
<p>Habilitaremos el servicio con el comando</p>
<pre><code>sudo systemctl enable ttys_enable.sh
</code></pre>
<p>Comenzamos el servicio con el comando</p>
<pre><code>sudo systemctl start ttys-enable.service
</code></pre>
<h2 id="archivo-billetero.ini">22. Archivo billetero.ini</h2>
<p>Este archivo debemos moverlo a la ruta <code>/etc/rut</code>a (Si es directorio o ruta no está creado, debemos crearlo con <code>mkdir</code>) para moverlo lo haremos con el comando</p>
<pre><code>sudo mv billetero.ini /etc/ruta
</code></pre>
<p>Damos todos los permisos al archivo con el comando</p>
<pre><code>sudo chmod 777 billetero.ini
</code></pre>
<p>Por ultimo al grupo y propietario le asignamos ruta con el comando</p>
<pre><code>sudo chown ruta:ruta billetero.ini
</code></pre>
<h2 id="archivo-autoverificacion.sh">23. Archivo <a href="http://autoverificacion.sh">autoverificacion.sh</a></h2>
<p>Este archivo debe ir en la ruta <code>/usr/bin</code> lo movemos con el comando</p>
<pre><code>sudo mv autoverificacion.sh /usr/bin
</code></pre>
<p>Damos permisos de ejecución con el comando</p>
<pre><code>sudo chmod +x  autoverificacion.sh
</code></pre>
<p>Damos como propietario y grupo al root con el comando</p>
<pre><code>sudo chown root:root autoverificacion.sh
</code></pre>
<h2 id="archivo-crontab">24. Archivo Crontab</h2>
<p>Debemos ingresar a este archivo para ingresar una linea de texto, para esto ingresamos con el comando</p>
<pre><code>sudo nano /etc/crontab
</code></pre>
<p>y nos arrojará la siguiente ventanas</p>
<p>Estando en este punto, debemos ingresar el siguiente texto</p>
<pre><code>01 * * * * root find     /RUTA/Screenshots/* -mtime +1 -delete 
</code></pre>
<p>este debe estar en la ultima linea, hecho eso, guardamos con Ctrl + o, presionamos Enter y para salir Ctrl + x y volver a la terminal anterior</p>
<p>Por ultimo debemos tener presente que la linea que ingresamos solo se ejecutará si existe la carpeta <code>Screenshots</code> en <code>/RUTA/</code> si no es el caso, la creamos con el comando <code>mkdir Screenshot</code> (En esta carpeta se almacenarán las capturas de pantalla que se hagan sobre el juego)</p>
<h2 id="carpeta-documents">25. Carpeta Documents</h2>
<p>A la carpeta Documents damos como propietario y grupo al usuario ruta con el comando</p>
<pre><code>sudo chown ruta:ruta Documents
</code></pre>
<h2 id="montar-contenedores-de-docker">26. Montar contenedores de Docker</h2>
<p>Para montar los contenedores debemos debemos ubicarnos en la ruta  <code>/home/ruta/Documents/docker</code> y ejecutar los comandos</p>
<pre><code>sudo docker-compose -f docker-compose.yml build
</code></pre>
<p>Montado el anterior podemos seguir con el siguiente con el comando</p>
<pre><code>sudo docker-compose -f docker-compose.yml up -d
</code></pre>
<h2 id="pantalla-de-carga">27. Pantalla de carga</h2>
<p>Uno de los archivos descargados y descomprimidos fue barra de carga, debemos cambiar el nombre por <code>imagenes</code>, esto lo hacemos con el comando</p>
<pre><code>sudo mv barra de carga imagenes 
</code></pre>
<p>(Si no funciona, mientras escribimos barra, dejar que auto complete con tab)</p>
<p><strong>Instalar feh</strong></p>
<p>Por ultimo antes de probar, debemos instalar feh este nos ayudará a mostrar la pantalla de carga junto con la carpeta imagenes, para instalarlo, usamos el comando</p>
<pre><code>sudo apt install feh
</code></pre>
<h2 id="probando-estado">28. Probando estado</h2>
<p>Escribimos el comando</p>
<pre><code>nano autostart
</code></pre>
<p>en la ruta <code>.config/openbox/</code></p>
<p>De acá vamos a probar si nos arroja algún error, tomamos las primeras 3 lineas y las pegamos en la terminal</p>
<p>Si no arroja ningún error para ejecutar pantalla de carga(Estará en pantalla en negro porque nos faltan cosas), entonces ahora copiamos y pegamos desde la linea que dice <code>for</code> hasta <code>done</code></p>
<p>Si sigue todo ejecutando sin problemas copiamos y pegamos en la terminal el resto de lineas para ejecutar el lanzador</p>
<p><strong>Configuration</strong></p>
<p>Vamos revisando los componentes, en la consola escribimos configuracion y debería aparecer lo siguiente:</p>
<p><strong>genericModals</strong></p>
<p>En la consola escribimos lo siguiente</p>
<pre><code>genericModals
</code></pre>
<p>y nos debe aparecer un login con fondo blanco o gris</p>
<p><strong>./RUTA/Lanzador/Lanzador.x86_64</strong></p>
<p>En la consola escribimos</p>
<pre><code>./RUTA/Lanzador/Lanzador.x86_64
</code></pre>
<p>y nos debe aparecer el menú donde tenemos todos los juegos a elegir, terminado este punto podemos reiniciar el equipo para probar todo el funcionamiento, para reiniciar lo haremos con el comando</p>
<pre><code>reboot
</code></pre>

