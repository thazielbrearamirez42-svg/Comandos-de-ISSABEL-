# Comandos-de-ISSABEL-

Instalación de Issabel
====================================================================


#Actualizacion del sistema

dnf install -y wget firewalld 

systemctl enable --now firewalld

# Activación y conf. de Firewall


systemctl start firewall && systemctl enable firewall 

firewall-cmd --permanent --add-service=http 
firewall-cmd --permanent --add-service=https 

# SIP
firewall-cmd --permanent --add-port=5060/udp 


# RTP (audio de llamadas)
firewall-cmd --permanent --add-port=10000-20000/udp 

firewall-cmd --reload 

#Ejecutar el instalador de Issabel

curl http://repo.issabel.org/issabel5-netinstall.sh | bash 

#Definir o cambiar claves de Admin y base de datos

issabel-admin-passwords--change 


=========================================
Modulo 4:
Practica 1: Instalar un servidor HTTP apache2/nginx (1pts)
Practica 2: Instalar un servidor de correos
Practica 3: Instalar un servidor de Impresion

Modulo 5
Requisito: Crear un segundo server (o Clonar su VM actual)

Practica 1: Syncronizacion de carpetas con Rsync
Practica 2: Instalacion y configuracion del Cluster 
Practica 3: Cluster de Alta Disponibilidad HTTP (1Pts) :Configura 2 servidores web (apache/NGINX) con keepalived

modulo 6:
 Cifrado
 Practica 2 - IP tables - UFW/Firewall-cmd 1pts   : Habilite los servicios de http, ftp y ssh 
 Practica 3 -Instalacion de IDS snort
 Practica 4: Configurar 2FA con google authenticator Modulo PAM para Acceso SSH

 Modulo 7:
1.Compartir archivos entre linux utilizando NFS 
 2.Creacion de fileserver compatible con Windows utilizando SAMBA (1Pts)  :Instalar SAMBA y habilitar el servicio
 3.Creacion de controlador de Dominio con cliente Windows

 Modulo 8.
 1: Instalacion y configuracion de Docker  con puerto 8888
  2.Instalacion de Portainer 
  3: IDespliegue de contenedor de Wordpress utilizando Docker-Compose 

Moudlo 9
  Practica 1 Instalacion de Webmin 
 2.Desplieque de una VM con terraform en digital Ocean
 3.Instalación de Ansible 
  4Comandos Ad-Hoc
  5.Playbooks
