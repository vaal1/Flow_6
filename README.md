# Flow_6
Clima y MySQL

(mardownpreview extension)
` al final formatea el texto para que se vea como codigo en las notas 
Instrucciones para la creacion de la base de datos correspondiente a este ejercicio

1.Instalar MySQL Server
`sudo apt install mysql-server`
2. Entrar a MySQL
`sudo mysql`
CREATE DATABASE codigoIoT;
USE codigoIoT;
CREATE TABLE clima (id INT (6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,fecha TIMESTAMP DEFAULT CURRENT_TIMESTAMP, nombre CHAR (248) NOT NULL, temperatura FLOAT (4,2), humedad INT (3));
DESCRIBE clima;
CREATE USER 'newuser'@'localhost' IDENTIFIED BY '12345';
CREATE USER 'valerie'@'localhost' IDENTIFIED BY '12345';
GRANT ALL PRIVILEGES ON *.* TO 'valerie'@'localhost';
node-red-node-mysql
-------------

Installar Grafana
https://grafana.com/grafana/download
version 9.1.3
Enterprise
sudo apt-get install -y adduser libfontconfig1
wget https://dl.grafana.com/enterprise/release/grafana-enterprise_9.1.3_amd64.deb
sudo dpkg -i grafana-enterprise_9.1.3_amd64.deb

opciones para arrancar grafana
sudo /bin/systemctl start grafana-server

Iniciar sesión en Grafana
http://localhost:3000/login
credenciales
usuario : admin
contraseña : admin
(La primera vez)
colocar nueva contraseña
contraseña : 12345

Agregar data source
Configuraciones > Data Source ó directamente en Add Source

usaremos mysql
Agregar panel (boton en esquina superior derecha)

https://grafana.com/docs/
https://www.timeanddate.com/worldclock/mexico/mexico-city


function '"+msg.payload+

etc/grafana/
clic der->abrir en terminal (porque necesitamos permisos de admin)

sudo nano grafana.ini
seccion secutiry
allow_embedding = true

sudo /bin/systemctl restart grafana-server

--Paneles de aguja de grafana 

