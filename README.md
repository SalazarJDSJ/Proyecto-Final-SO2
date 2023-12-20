[![UPDS-OFI.jpg](https://i.postimg.cc/bYx0cLy5/UPDS-OFI.jpg)](https://postimg.cc/YjSLQ6mN)

# UNIVERSIDAD PRIVADA DOMINGO SAVIO
# PROYECTO FINAL SISTEMAS OPERATIVOS II
## INTEGRANTES GRUPO 6 
##### EDWARD ALEXIS CLAROS REYES 
##### JOSE DANIEL SALAZAR JUSTINIANO
##### NAIDAR JOAN CASTRO GUZMAN
## DOCENTE
##### Ing.JAIME ZAMBRANA CHACON


## INTRODCCION
En nuestro análisis, desglosaremos la arquitectura modular de Drupal, revelando cómo sus componentes se entrelazan para ofrecer una flexibilidad sin igual. Desde módulos básicos hasta extensiones especializadas, cada elemento contribuye a la construcción de un ecosistema web adaptativo y poderoso.
A lo largo de este informe, también exploraremos la funcionalidad clave de Drupal, destacando su capacidad para organizar y presentar información de manera estructurada, así como su capacidad para gestionar usuarios y permisos de manera efectiva. Al comprender cómo Drupal facilita la colaboración y la interactividad en línea, revelaremos las razones detrás de su prominencia en el desarrollo web moderno.
## ABSTRAC
In our analysis, we will break down the modular architecture of Drupal, revealing how its components interconnect to offer unparalleled flexibility. From basic modules to specialized extensions, each element contributes to the construction of an adaptive and powerful web ecosystem.
Throughout this report, we will also explore Drupal's key functionality, highlighting its ability to organize and present information in a structured manner, as well as its effective management of users and permissions. By understanding how Drupal facilitates online collaboration and interactivity, we will unveil the reasons behind its prominence in modern web development.
## MARCO TEORICO
## DRUPAL
Drupal es un CMS flexible basado en el entorno LAMP, con un diseño modular que permite incorporar o quitar funcionalidad instalando o desinstalándo módulos, y permite que la apariencia o diseño del sitio web se pueda cambiar instalando o desistalando temas. La descarga básica de Drupal, conocida como el núcleo de Drupal, contiene los archivos PHP necesarios para ejecutar la funcionalidad básica del CMS, varias opciones de módulos y temas, y múltiples recursos JavaScript, CSS e imágenes. Se pueden descargar muchos más módulos y temas en el sitio web

[![drupal.jpg](https://i.postimg.cc/QCBvz73h/drupal.jpg)](https://postimg.cc/Wqv9FhzH)

## MYSQL
MySQL es el sistema de gestión de bases de datos relacional más extendido en la actualidad al estar basada en código abierto. Desarrollado originalmente por MySQL AB, fue adquirida por Sun MicroSystems en 2008 y esta su vez comprada por Oracle Corporation en 2010, la cual ya era dueña de un motor propio InnoDB para MySQL.

[![mysqlw.webp](https://i.postimg.cc/cLmX7tck/mysqlw.webp)](https://postimg.cc/0zzYPQF7)

## APACHE
es un servidor web HTTP de código abierto, para plataformas Unix (BSD, GNU/Linux, etc.), Microsoft Windows, Macintosh y otras, que implementa el protocolo HTTP/1.1 y la noción de sitio virtual según la normativa RFC 2616. Cuando comenzó su desarrollo en 1995 se basó inicialmente en código del popular NCSA HTTPd 1.3, pero más tarde fue reescrito por completo.

[![apache.webp](https://i.postimg.cc/7ZJDRD5k/apache.webp)](https://postimg.cc/sMztBkP6)
## PASOS PREVIOS PARA USO Y FUNCIONALIDAD DE DRUPAL
Sudo apt update: actualiza la lista de paquetes disponibles 
sudo apt install apache2: Instalamos servidor web apache

[![PASO-1.jpg](https://i.postimg.cc/jSK7h8gt/PASO-1.jpg)](https://postimg.cc/N5JFsxvz)

Sudo apt install mysql_server: instalamos servdor de base de datos de mysql

[![paso2.jpg](https://i.postimg.cc/1RB2Pz2Q/paso2.jpg)](https://postimg.cc/Yj4bzttn)

sudo apt install php libapache2-mod-php php-mysql php-gd php-xml php-mbstring php-xmlrpc php-curl unzip : Instalamos php.

![image](https://github.com/SalazarJDSJ/Proyecto-Final-SO2/assets/154374679/53d61388-ad70-49e4-9b98-69628377516e)

sudo mysql -u root -p : Iniciamos mysql como superusuario

![image](https://github.com/SalazarJDSJ/Proyecto-Final-SO2/assets/154374679/7ae6704f-6da5-4447-b715-c7090ab7dcce)


## INSTALACION DE DRUPAL

wget https://www.drupal.org/download-latest/tar.gz -O drupal.tar.gz : Descargamos drupal

![image](https://github.com/SalazarJDSJ/Proyecto-Final-SO2/assets/154374679/4e5fced0-b568-4a67-9ab6-cf3b7b471c19)

tar -zxvf drupal.tar.gz : Descomprimimos el archivo descargado

![image](https://github.com/SalazarJDSJ/Proyecto-Final-SO2/assets/154374679/4e1242d3-5bcc-4c50-90e8-3b27b1ce03bd)

sudo mv drupal-10.2.0 /var/www/html/drupal : Movemos los archivos de drupal al servidor web.sudo chown -R www-data:www-data /var/www/html/drupal : Cambiamos de dueño y grupo.

![image](https://github.com/SalazarJDSJ/Proyecto-Final-SO2/assets/154374679/1e2a95dd-39e0-45d0-a838-59989d638c02)

sudo nano /etc/apache2/sites-available/drupal.conf : Crea y edita un nuevo archivo de llamado drupal.conf.

![image](https://github.com/SalazarJDSJ/Proyecto-Final-SO2/assets/154374679/209b5f72-f36a-480b-83e1-e969a90993c0)

Contenido del archivo de configuracion para apache que indica como servidor a Drupal

![image](https://github.com/SalazarJDSJ/Proyecto-Final-SO2/assets/154374679/681f95a2-535a-4c3a-ae89-f217c7acf0af)

sudo systemctl reload apache2 : Recargamos el servidor web para habilitar la configuracion.
sudo a2ensite drupal.conf : Habilitamos la configuracion.
sudo systemctl restart apache2 : Reiniciamos el servidor web para aplicar cambios.

![image](https://github.com/SalazarJDSJ/Proyecto-Final-SO2/assets/154374679/e7ff66e1-0010-4df9-8d5f-3311aba115df)

## CONFIGURACION E INGRESO AL SITIO WEB

Entramos al navegador web y ponemos http://localhost/.

![image](https://github.com/SalazarJDSJ/Proyecto-Final-SO2/assets/154374679/c8d66981-9f1e-4fa3-9088-b90df8966227)

Verificamos que cumplimos los requisitos.

![image](https://github.com/SalazarJDSJ/Proyecto-Final-SO2/assets/154374679/52df1342-bfb1-4357-836e-a45ea7794986)

Agregamos nuestra base de datos previamente creada y configurada y continuamos

![image](https://github.com/SalazarJDSJ/Proyecto-Final-SO2/assets/154374679/5becb20a-2f3c-42f6-ba42-7f8784745241)

Terminando con la configuración del sitio

![image](https://github.com/SalazarJDSJ/Proyecto-Final-SO2/assets/154374679/d57bc6cb-bea9-41c7-805f-03beb40ca8bb)

### Videos de instalacion de drupal
https://youtu.be/ZDDXlolhw9Q?si=37Fgt1erkhwDyvr6
### Video de instalacion de Apache 2 , MySQL , PHP
https://youtu.be/yxiOaaiE_QY?si=RneuGj57ixbxduHV

## CONCLUSION

Concluimos nuestro proyecto como grupo llevandonos el aprendizaje de la materia y logrando entender mas acerca de servidores y de la materia Sistemas Operativos 2
La creación de nuestro sitio web mediante la instalación previa y el uso de las herramientas Drupal, MySQL y Apache. Así como la instalación de algunos módulos para darnos mas opciones de personalización a sido un éxito dejando como producto un sitio web básico y dinámico.

## BIBLIOGRAFIA

https://es.wikipedia.org/wiki/Drupal
https://es.wikipedia.org/wiki/MySQL
https://openwebinars.net/blog/que-es-mysql/
https://www.hostinger.es/tutoriales/que-es-apache/
https://es.wikipedia.org/wiki/Servidor_HTTP_Apache
https://www.hostinger.es/tutoriales/linux-comandos






























