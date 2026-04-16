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
