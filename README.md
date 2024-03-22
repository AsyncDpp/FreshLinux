# FreshLinux
Pasos a seguir para una instalación reciente de Linux

# Actualizar todos los paquetes:
sudo apt update && apt upgrade -y

# Comprobar si el comando sudo está instalado intentando instalar el paquete:
apt install sudo
# Dar permisos sudo al usuario XXXX:
usermod -aG sudo XXXX

# Instalar SSH:
sudo apt install openssh-server
comprobar que está activo con systemctl status ssh (o sshd)

# Instalar curl:
sudo apt install curl

# Instalar Docker y Docker-compose:
sudo apt install docker.io
# para dar permisos en docker
sudo usermod -aG docker XXXX (siendo XXXX el nombre usuario)

sudo apt install docker-compose

# Sin terminal:
Instalar extension manager con el asistente de aplicaciones. Después usarlo para instalar Allow locked remote conections (o algo así. Buscar "allow" y sale).
Configurar escritorio remoto y activar vnc (con contraseña). Rdp usa el puerto 3389 y vnc el 5900
