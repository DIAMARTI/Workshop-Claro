<h1>Gestión de Vistas</h1>

<p>
<strong>Meta:</strong>
<br>Conocer las vistas de recursos de Satellite
</p>
<p>
<strong>Objetivos:</strong>
<br>- Registrar una vista nueva dentro de un entorno customizado

</p>
<p>
<strong>Secciones:</strong>
<br>- Gestión de vistas
</p>
<p>
<strong>Laboratorios:</strong>
<br><strong>- Crear un nuevo entorno</strong>
<br><strong>- Crear y publicar una vista en el entorno</strong>
</p>

<strong>Requisitos:</strong>
<br><strong>- Satellite</strong>


<h3><br><strong>## Crear un nuevo entorno</strong></h3>
Para crear un nuevo entorno, nos dirigimos a la seccion Content > Lifecycle Environments  y le damos crear un nuevo entorno
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat10101R.jpg?raw=true"width="800" height="400"></p>
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat10102R.jpg?raw=true"width="800" height="400"></p>
<br>
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat10103R.jpg?raw=true"width="800" height="400"></p>
<br>
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat10104R.jpg?raw=true"width="800" height="400"></p>
<br>
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat10105R.jpg?raw=true"width="800" height="400"></p>


Nombremos el entorno nuevo entorno personal
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat1002.png?raw=true"></p>

<br><h3><strong>## Crear y publicar una vista en el entorno</strong></h3>

Ahora que tenemos un nuevo entorno, podemos crear una nueva vista en la seccion Content > Content Views 
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat1003.png?raw=true"></p>

Nombramos la vista nueva
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat1004.png?raw=true"></p>

En el vista nueva, seleccionamos el repositorio Base del canal de RHEL8 para incluirlo
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat1005.png?raw=true"></p>

Ahora podemos publicar la vista
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat1006.png?raw=true"></p>

Guardamos la version 1 de nuestra vista
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat1007.png?raw=true"></p>

Cuando termine de publicar, con le damos click al boton promover
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat1008.png?raw=true"></p>

Ahora le damos check a nuestro entorno para que la vista sea promovida en ella
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat1009.png?raw=true"></p>

Podemos ingresar a la seccion de Hosts > Todos los hosts y editar las propiedades del host
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat1010.png?raw=true"></p>

Editamos las propiedades para que este host pertenesca a nuestro entorno y vista customizada
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat1011.png?raw=true"></p>

Ahora regresamos a la vista de contenidos y los recursos empezaran a registrarse en el entorno a medida que sean registrados y puedas ser enviados a futuros reportes

<h3><strong>## Ejercicio propuesto 01</strong></h3>
Cree un nuevo entorno y vista que permita registrar el repositorio AppStream, Base y el Tools de Satellite y su cliente personal de Satellite

<h3><br><strong>## Construyendo RPMS</strong></h3>

Satellite despliega contenido vía RPMs, la gran mayoría del contenido como programas, librerías, documentación, etc Red Hat lo entrega a traves de este formato, vamos a crear un RPM versionado, nos conectamos a nuestro cliente satellite y creamos un programa que cree un archivo de configuración y lo empaquetamos

<br>`# mkdir programa-1.0`
<br>`# echo "Hola Andy" >> programa-1.0/programa.conf`
<br>`# tar -czvf programa-1.0.tar.gz programa-1.0`

Al tener un archivo empaquetado con la fuente de nuestro programa, debemos instalar el componente que permite la construir de RPMs
<br>`# yum install -y rpmdevtools`

Creamos una estructura de RPMs con el comando
<br>`# rpmdev-setuptree`

Copiamos el paquete en la ruta de contenidos
<br>`# cp programa-1.0.tar.gz rpmbuild/SOURCES/`

Creamos el archivo spec con el siguiente contenido
<br>`# vi rpmbuild/SPECS/programa.spec`

<br>`Name:           programa`
<br>`Version:        1.0`
<br>`Release:        0`
<br>`Summary:        Programa`
<br>`License:        GPL`
<br>`URL:            http://satellite.opennova.pe`
<br>`Source0:        programa-1.0.tar.gz`
<br>`BuildRequires:  /bin/bash`
<br>`Requires:       /bin/bash`
<br>`%description`
<br>`Programa de ejemplo`
<br>`%define debug_package %{nil}`
<br>`%prep`
<br>`%setup -q`
<br>`%build`
<br>`%install`
<br>`mkdir -p $RPM_BUILD_ROOT/etc`
<br>`install -m 0644 programa.conf $RPM_BUILD_ROOT/etc`
<br>`%files`
<br>`/etc/programa.conf`

Creamos el RPM con el comando
<br>`# rpmbuild -ba rpmbuild/SPECS/programa.spec`

Validamos que tengamos el RPM en la ruta
<br>`# ls rpmbuild/RPMS/x86_64/`

Ahora que tenemos el programa lo instalamos con
<br>`# yum install rpmbuild/RPMS/x86_64/programa-1.0-0.x86_64.rpm`

Con la instalacion del programa validamos que el archivo /tmp/programa.conf exista con el contenido

<h3><br><strong>## Ejercicio propuesto 02</strong></h3>
Actualice el programa para que sea la version 2.0 con contenido nuevo, no borre el rpm anterior ni lo desisntale, actualicelo!!!

Ahora que tiene un RPM versioando, se puede crear repositorios custom en satellite y gestionar su contenido por RPMs

<h3><br><strong>## Ejercicio propuesto 03</strong></h3>

Desinstale el java actual de su cliente con yum remove java luego, cree una 3ra versión de su RPM pero este nueva versión tiene como dependencia a JAVA, su RPM custom debe invocar la instalacion de JAVA por si mismo




<p><br><a href="sat">volver</a></p>
