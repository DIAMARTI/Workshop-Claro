<h1>Qué es Ansible Tower</h1>
<p>
<strong>Meta:</strong>
<br>- Entender el proceso de instalación de la solución Red Hat Ansible Tower así como el diseño sugerido para una correcta implementación.
</p>
<p>
<strong>Objetivos:</strong>
<br>- Instalación de Red Hat Ansible(Demostración)
</p>
<p>
<strong>Secciones:</strong>
<br>-  .(Teórico - Practico)
<br>- Validación de pre-requisitos para la instalación de Red Hat Ansible Tower.(Teórico)
<br>- Instalación de Red Hat Ansible. (Demostración)
</p>
<p>
<strong>Laboratorios:</strong>
<br>- Instalación de Red Hat Ansible Tower
</p>

# Validación de pre-requisitos para la instalación de Red Hat Ansible Tower

Ansible Tower tiene los siguientes requisitos:

Sistemas operativos compatibles:

Red Hat Enterprise Linux 6 de 64 bits

Red Hat Enterprise Linux 7 de 64 bits

Red Hat Enterprise Linux 8 de 64 bits

CentOS 6 de 64 bits

CentOS 7 de 64 bits

CentOS 8 de 64 bits

Ubuntu 12.04 LTS de 64 bits

Ubuntu 14.04 LTS de 64 bits



La última versión estable de Ansible


2 GB de RAM como mínimo (se recomiendan más de 4 GB de RAM)

2 GB de RAM (mínimo y recomendado para instalaciones de prueba de Vagrant)
Se recomiendan 4 GB de RAM por cada 100 bifurcaciones
Disco duro de 20 GB

Se requiere soporte de 64 bits (kernel y tiempo de ejecución)



Para Amazon EC2:

Tamaño de instancia de m3. Mediano o mayor
Un tamaño de instancia de m3.xlarge o mayor si hay más de 100 hosts
Para configuraciones HA MongoDB:

Si planea ejecutar MongoDB, las siguientes pautas proporcionan una estimación aproximada de la cantidad de espacio requerido. El cálculo básico es:

(number of hosts in inventory) * (number of scans) * (average module fact size) * (number of modules scanning)

Por ejemplo:

hosts = 1,000

número de escaneos = 365 (1 escaneo por día durante un año)

tamaño medio de los hechos del módulo = 100 kb

número de módulos = 4 (ansible, paquetes, servicios, archivos)

= 146 GB

La operación de escaneo predeterminada tiene los cuatro (4) módulos enumerados, pero puede agregar los suyos propios. Dependiendo de los tipos de módulos y del tamaño de los datos que esté recopilando, ese tamaño puede ser mayor.

**Requerimientos de puertos y firewall**

Puertos para la comunicación de satélite a Red Hat CDN
| Puerto | Protocolo | Servicio | Requerido para |
| --- | --- | --- | --- |
| 80 | TCP |HTTP|Servicios de administración web|
| 443 | TCP |HTTPS|Servicios de administración web seguro|
| 22| TCP |SSH|Servicios de administración remota via ssh|
| 5432| TCP | DB |Servicios de conexion a la base de datos|



# Instalación de Red Hat Ansible Tower. (Demostración)
**Verificando conectividad y resolución DNS**
```
[root@server08 ~]# ping -c1 localhost
```
```
[root@server08 ~]# ping -c1 $(hostname -f)
```
```
[root@server08 ~]# ping -c1 $(hostname -s)
```
```
[root@server08 ~]# nslookup server08.opennova.pe
Server:         192.168.10.178
Address:        192.168.10.120#53

Name:   server08.opennova.pe
Address: 192.168.10.178
```
```
[root@server08 ~]# nslookup 192.168.10.178
178.10.168.192.in-addr.arpa      name = server08.opennova.pe
```

Es buena idea indicar el el archivo /etc/hosts
<br>**\<IP\> \<FQDN Ansiblee\> \<Short name Ansible\>**
```
192.168.10.178 server08.opennova.pe server08
```
**Habilitación de conexiones de un cliente a un servidor satélite**
```
[root@server08 ~]# firewall-cmd \
--add-port="80/tcp" --add-port="443/tcp" \
--add-port="22/tcp" --add-port="5432/tcp"
```
```
[root@server08 ~]# firewall-cmd --runtime-to-permanent
```
```
[root@server08 ~]# firewall-cmd --list-all
```
<br>**Instalacion**

Registrar el servidor a un sistema que permita el acceso a repositorios de paquetes como Satellite
```
[root@server08 ~]# curl --insecure --output katello-ca-consumer-latest.noarch.rpm https://satellite.opennova.pe/pub/katello-ca-consumer-latest.noarch.rpm
[root@server08 ~]# yum localinstall katello-ca-consumer-latest.noarch.rpm
[root@server08 ~]# subscription-manager register --org="OpenNova" --activationkey="RHEL8"
[root@server08 ~]# subscription-manager attach --auto
[root@server08 ~]# subscription-manager repos --enable=ansible-2.9-for-rhel-8-x86_64-rpms
```
**Borrar metadata yum**
```
[root@server08 ~]# yum clean all
```
**Verificar repositorios configurados**
``` 
[root@server08 ~]# yum repolist enabled
```

Validamos que el sistema tenga al menos los siguientes repositorios

ansible-2.9-for-rhel-8-x86_64-rpms
rhel-8-for-x86_64-appstream-rpms
rhel-8-for-x86_64-baseos-rpms

**Realizar una lista de paquetes necesarios para la administración de la maquina virtual.**

```
[root@server08 ~]# yum install ansible git
```


**Actualizar el sistema en conjunto y reiniciar**
```
[root@server08 ~]# yum update
```
```
[root@server08 ~]# reboot
```

**Instalar paquetes de instalación para Red Hat Satellite**

``` 
[root@satellite ~]# yum install satellite
```
**Instalar Red Hat Ansible Tower**

Descargamos desde el ftp del salon el instalador de Ansible Tower y descomprimirlo

```
[root@server08 ~]# wget ftp://classroom.opennova.pe/ansible-automation-platform-setup-bundle-1.2.5-1.tar.gz
[root@server08 ~]# tar -xzvf ansible-automation-platform-setup-bundle-1.2.5-1.tar.gz
[root@server08 ~]# cd ansible-automation-platform-setup-bundle-1.2.5-1
---

Modificar el archivo inventory para que pueda uztomizar las claves de admin y de awx a redhat

---
[root@server08 ~]# vi inventory
---

Ejecutar el instalador con

---
[root@server08 ~]# ./setup.sh

```

**Nota: Para evitar problemas de perdida de conectividad hacia la terminar virtual se recomienda ejecutar elprocedimiento de instalación por screen**
<br>**Instalar screen**
```
[root@satellite ~]# yum install -y screen
```
**Generar un alias de conexión screen**
```
[root@satellite ~]# screen -S jaime 
```
**Listar conexión screen, identificar el id ejemplo: 3081**
```
[root@satellite ~]# screen -ls
There is a screen on:
        3081.jaime      (Attached)
1 Socket in /var/run/screen/S-root.
```
**En caso de des-conexión abrir otro terminal y ejecutar el comando indicado para restablecer la conexión, recordar poner el id que se genere en su terminal**
```
[root@server08 ~]# screen -r 3081
```

### **Instalacion**

Registrar el sistema a una plataforma que permita el acceso a repositorios como Satellite


```
curl --insecure --output katello-ca-consumer-latest.noarch.rpm https://satellite.opennova.pe/pub/katello-ca-consumer-latest.noarch.rpm
yum localinstall katello-ca-consumer-latest.noarch.rpm
subscription-manager register --org="OpenNova" --activationkey="RHEL8"
subscription-manager attach --auto
subscription-manager repos --enable=ansible-2.9-for-rhel-8-x86_64-rpms
```
```
[root@satellite ~]# yum repolist
```
Es buena idea indicar el el archivo /etc/hosts
<br>**\<IP\> \<FQDN Satellite\> \<Short name Satellite\>**
<br>**NOTA: Utilizar las ips y nombres dns asignados**
```
192.168.0.151 server01.opennova.pe server01
```

Instalar paquetes necesarios para su administracion
```
[root@satellite ~]# yum install sos git net-tools vim mlocate chrony screen bash-completion
[root@satellite ~]# systemctl start chronyd
[root@satellite ~]# systemctl enable chronyd
```

```
[root@satellite ~]# firewall-cmd \
--add-port="80/tcp" --add-port="443/tcp" \
--add-port="5647/tcp" --add-port="8000/tcp" \
--add-port="8140/tcp" --add-port="9090/tcp" \
--add-port="53/udp" --add-port="53/tcp" \
--add-port="67/udp" --add-port="69/udp" \
--add-port="5000/tcp"
```
```
[root@satellite ~]# firewall-cmd --runtime-to-permanent
```
```
[root@satellite ~]# firewall-cmd --list-all
```
```
[root@satellite ~]# rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-redhat-release
[root@satellite ~]# mkdir /mnt/sat67
[root@satellite ~]# mount /dev/cdrom /mnt/sat67
[root@satellite ~]# cd /mnt/sat67; ./install_packages
[root@satellite ~]# satellite-installer --help
[root@satellite ~]# satellite-installer --scenario satellite \
--foreman-initial-admin-username admin \
--foreman-initial-admin-password redhat
```

Ingresar a la url `https://satellite.opennova.pe`
<br>usuario: **admin**
<br>password: **redhat**

<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat200.png?raw=true" width="800" height="400"></p>

Una vez indicada las credenciales podremos logearnos y accesar al dashboard de satellite
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat201.png?raw=true" width="800" height="400"></p>

**Instalar software adicional posterior a la instalacion**
```
[root@satellite ~]# foreman-maintain packages install bind-utils
```
NOTA: Foreman bloquea la instalación post-instalación para evitar que se instalen paquetes que hagan conflicto con satellite, pero si se necesita instalar alguna herramienta para la administración y/o resolución de problemas este lo hará con el comando indicado. Tomar en cuenta que cada instalación hará que satellite valide su integridad por lo que posterior a la instalación el reiniciara los servicios y verificara sus componentes.

<br>**Extras**
<br>**Hammer Authentication Session**
```
[root@satellite ~]# vim /root/.hammer/cli.modules.d/foreman.yml
```
<br>Agregar el parámetro **:use_sessions:** true como se muestra en la siguiente imagen
```
[root@satellite ~]# cat /root/.hammer/cli.modules.d/foreman.yml
:foreman:
  :use_sessions: true
  # Credentials. You'll be asked for the interactively if you leave them blank here
  :username: 'admin'
  :password: 'redhat'

  # Check API documentation cache status on each request
  :refresh_cache: false

  # API request timeout in seconds, set -1 for infinity
  :request_timeout: 120
```
```
[root@satellite ~]# hammer auth login basic
[Foreman] Username: admin
[Foreman] Password for admin:
Successfully logged in as 'admin'.
```
```
[root@satellite ~]# hammer auth status
Session exists, currently logged in as 'admin'.
```
```
[root@satellite ~]# hammer organization list
---|----------------------|----------------------|-------------|---------------------
ID | TITLE                | NAME                 | DESCRIPTION | LABEL
---|----------------------|----------------------|-------------|---------------------
1  | Default Organization | Default Organization |             | Default_Organization
3  | Opennova             | Opennova             |             | ON
---|----------------------|----------------------|-------------|---------------------
```
```
[root@satellite ~]# hammer settings list | grep ^idle_timeout
idle_timeout                                           | Idle timeout                                                | 60                                                                               | Log out idle users after a certain number of minutes
```
**Cambiar el tiempo de sesión de 60 minutos a 30 minutos**
```
[root@satellite ~]# hammer settings set --name idle_timeout --value 30
Setting [idle_timeout] updated to [30].
```
```
[root@satellite ~]# hammer settings list | grep ^idle_timeout
idle_timeout                                           | Idle timeout                                                | 30                                                                               | Log out idle users after a certain number of minutes
```
**Revisar el estado de los servicios principales o core de Satellite**
```
[root@satellite ~]# hammer ping
database:
    Status:          ok
    Server Response: Duration: 0ms
candlepin:
    Status:          ok
    Server Response: Duration: 16ms
candlepin_auth:
    Status:          ok
    Server Response: Duration: 14ms
pulp:
    Status:          ok
    Server Response: Duration: 51ms
pulp_auth:
    Status:          ok
    Server Response: Duration: 19ms
foreman_tasks:
    Status:          ok
    Server Response: Duration: 4ms
```

**Gestionar los servicios de red hat satellite**

Listar servicios Red Hat Satellite
```
[root@satellite ~]# satellite-maintain service list
```
Listar estado Red Hat Satellite
```
[root@satellite ~]# satellite-maintain service status
```
Parar servicios Red Hat Satellite
```
[root@satellite ~]# satellite-maintain service stop
```
Reiniciar servicios Red Hat Satellite
```
[root@satellite ~]# satellite-maintain service restart
```

**Configurar mensaje personalizado para pagina de Login**

<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat202.png?raw=true"width="800" height="400"></p>

<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat203.png?raw=true"width="800" height="400"></p>

<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat204.png?raw=true"width="800" height="400"></p>

**Resetear el password del Administrador**
Generar una contraseña aleatoria
```
[root@satellite ~]# foreman-rake permissions:reset
Reset to user: admin, password: zaJxRftxb7Gbvca
```
**Ingresar con el password y cambiar por uno nuevo**

<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat205.png?raw=true"width="800" height="400"></p>
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat206.png?raw=true"width="800" height="400"></p>

**Asignar una contraseña nueva**
```
[root@satellite ~]# foreman-rake permissions:reset password=redhat123
```

# Laboratorio: Instalando Red Hat Satellite

<br>**1. Instalar Red Hat Satellite utilizando el procedimiento INSTALACIÓN OFFLINE**
<br>- Utilizar el procedimiento indicado en la explicación.
<br>- Una vez finalizada la instalación logearse con el usuario: admin password: redhat
<br>- Post-instalación instalar el paquete bind-utils
<br>**2. Configurar el cliente hammer**
<br>- Configurar hammer para que utilice sesiones **:use_sessions:**
<br>- Logearse al satellite por la herramienta hammer utilizando **hammer auth login basic**
<br>- Setear el timeout de sesión a 30 minutos
<br>- Validar por hammer los servicios principales
<br>- Utilizar satellite-maintain service para listar, ver el estado y reiniciar los servicios de satellite.
<br>- Configurar un mensaje de inicio de sesión que diga la frase: "Red Hat Satellite Global Bank"
<br>- Cambiar la contraseña del usuario admin por los 2 métodos: Con el uso de clave autogeneradas luego cambiarlo por la GUI y luego cambiarla indicando el password exacto que debe tener.
