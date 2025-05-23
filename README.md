# FreshLinux
Pasos a seguir para una instalación reciente de Linux

# Actualizar todos los paquetes:
```
sudo apt update && apt upgrade -y
```

# Comprobar si el comando sudo está instalado intentando instalar el paquete:
```
apt install sudo
```
# Dar permisos sudo al usuario XXXX:
```
usermod -aG sudo XXXX
```
# Dar permisos de grupo www-data al usuario XXXX:
```
sudo usermod -aG www-data XXXX
```
Los permisos no se actualizan hasta que reinicias el equipo. Después de reiniciar comprobar permisos del usuario con el comando:
```
groups
```


# Instalar SSH:
```
sudo apt install openssh-server
```  
Comprobar que está activo con systemctl status ssh (o sshd)

# Instalar curl:
```
sudo apt install curl
```

# Instalar Docker y Docker-compose:
```
sudo apt install docker.io
```
# para dar permisos en docker
```
sudo usermod -aG docker XXXX
```
(siendo XXXX el nombre usuario)  
```
sudo curl -SL https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-x86_64 -o /usr/local/bin/docker-compose
```
```
sudo chmod +x /usr/local/bin/docker-compose
```
Comprobar versión de docker compose:
```
docker-compose -v
```

Reiniciar PC para que se apliquen los cambios en la configuración del grupo de usuarios de Docker.

# Sin terminal:
Instalar extension manager con el asistente de aplicaciones. Después usarlo para instalar Allow locked remote conections (o algo así. Buscar "allow" y sale).
Configurar escritorio remoto y activar vnc (con contraseña). Rdp usa el puerto 3389 y vnc el 5900
