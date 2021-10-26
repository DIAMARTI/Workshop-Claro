<h1>Ansible Automation</h1>
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans100.png?raw=true"width="800" height="400"></p>
<p>
<strong>Meta:</strong>
<br>- Entendimiento Ansible Automation y Red Hat Automation Platform.
</p>
<p>
<strong>Objetivos:</strong>
<br>- Conceptos de Ansible y Arquitectura (Teórico)
</p>
<p>
<strong>Secciones:</strong>
<br>- Introducción a Ansible. (Teórico)
<br>- Introducción a Red Hat Ansible Automation Platform. (Teórico)
<br>- Planificar setup inicial Ansible. (Demostración) 
</p>
<p>
<strong>Laboratorios:</strong>
</p>

# Introducción a Ansible. (Teórico)
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans100.jpg?raw=true"width="800" height="400"></p>

### **¿Qué es la Automatizacion de TI?**
<br>La automatización de TI o automatización de infraestructura consiste en utilizar un software para crear políticas y procesos que reduzcan o reemplacen la interacción manual con sistemas de TI.

Beneficios:
- Ahorro de costos operativos.
- Mitigar el error humano.
- Simplificar tareas repetitivas.
- Facilitar despliegues e integraciones.
- Reducción del tiempo de ejecución de tareas.
---

<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans101.png?raw=true"width="600" height="400"></p>

### **¿Qué es Infraestructura como código?**
<br>
<br>La infraestructura como código (IaC) es un enfoque para la gestión de infraestructuras de sistemas de TI que se basa en el uso de archivos de configuración repetibles para generar entornos de implementación consistentes para el desarrollo de CI/CD

Tipos de IaC:
- [Terraform](https://www.terraform.io)
- [CloudFormation](https://aws.amazon.com/es/cloudformation)
- [Azure ARM](https://azure.microsoft.com/es-es/services/arm-templates/)
- [Ansible](https://www.ansible.com)
- [Chef](https://www.chef.io/products/chef-infra)
- [Puppet](https://puppet.com)
- [Saltstack](https://saltproject.io)
- otros
---
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans105.png?raw=true"width="500" height="230"></p>

### **¿Qué es Ansible?**
<br>**Ansible** es una plataforma de automatización de código abierto. Es un lenguaje de automatización simple que puede describir perfectamente una infraestructura de aplicaciones de TI en Ansible Playbooks.

- Ansible es simple.
- Ansible es potente.
- Ansible no necesita agentes.
<br>

**Arquitectura Ansible**
<br>
<br>
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans103.jpg?raw=true"width="700" height="400"></p>

---

# Introducción a Red Hat Ansible Automation Platform. (Teórico)

<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans102.jpg?raw=true"width="800" height="400"></p>

### **¿Qué es Red Hat Ansible Automation Platform?**
Ansible Automation Platform ofrece un marco empresarial para diseñar y gestionar la automatización de la TI según sea necesario. Además, proporciona un panel visual, control de acceso basado en funciones y herramientas de automatización que incluyen sistemas de análisis y contenido certificado y reutilizable, para que los usuarios puedan centralizar y controlar su infraestructura.

Ansible Automation Platform utiliza YAML, un lenguaje de automatización comprensible para las personas que permite que los usuarios de una empresa compartan, evalúen y gestionen el contenido de automatización. Colabore con todos los equipos y ponga en marcha sus sistemas rápidamente, gracias a los conjuntos de funciones y módulos creados previamente en los que se pueden realizar búsquedas, para que cualquier persona logre implementar la automatización.

### **Características y Beneficios**
Red Hat Ansible Automation Platform ayuda a las organizaciones a adoptar una cultura de automatización colaborativa al brindar una experiencia coherente en todas partes, basada en características adaptadas a las necesidades de todo el equipo de TI. Con la plataforma de automatización Ansible:

- Los administradores y arquitectos de TI pueden expandir más fácilmente la automatización en toda la empresa, mientras administran la política de automatización y el gobierno con el catálogo de servicios de automatización y obtienen informes en tiempo real en toda la pila con Red Hat Insights for Ansible Automation Platform.

- Los desarrolladores conservan la libertad de construir, sin la sobrecarga operativa de mantener muchas herramientas y marcos. Los entornos de ejecución brindan una experiencia consistente similar a un contenedor para la automatización de construcción y escalado, con nuevas herramientas incluidas para ayudar a construirlos y administrarlos. Las colecciones de contenido de Ansible ofrecen contenido de automatización prediseñado de más de 100 socios certificados, con soluciones disponibles para casi todos los casos de uso.

- Los administradores y operadores tienen herramientas poderosas en el controlador de automatización y el centro de automatización para administrar y compartir proyectos de automatización de manera más eficiente, con un lenguaje común y una combinación ampliamente accesible de interfaces de línea de comandos (CLI), interfaces gráficas de usuario (GUI) y interfaces de usuarios basados ​​en texto (TUI).

- Su organización puede abordar los desafíos de automatización, desde la automatización de la seguridad y la red, hasta el aprovisionamiento de infraestructura en la nube, la gestión de la configuración, la integración continua y la entrega continua (CI / CD), contenedores y más.

| Componentes de la plataforma  | Usos y beneficios |
| --- | --- |
| Ansible Core| Ansible Automation Platform está alineada con la comunidad global detrás del proyecto Ansible, con capacidades fundamentales adicionales y garantía de Red Hat que ayudan a su empresa a adoptar cómodamente la automatización en toda la organización a cualquier escala. |
| Automation controller| El plano de control de Ansible Automation Platform se denomina controlador de automatización (renombrado Ansible Tower). Incluye una interfaz de usuario (UI), control de acceso basado en roles (RBAC), flujos de trabajo y CI / CD para ayudar a su equipo a escalar. El controlador de automatización ayuda a estandarizar cómo se implementa, inicia, delega y audita la automatización. Administre el inventario, inicie y programe flujos de trabajo, realice un seguimiento de los cambios e integre en los informes, todo desde una interfaz de usuario centralizada y una interfaz de programación de aplicaciones (API) RESTful. |
| Automation execution environments| Empaquetados como contenedores, los entornos de ejecución de automatización (que reemplazan a Ansible Engine) son entornos definidos, consistentes y portátiles para ejecutar playbooks y roles de Ansible. Los entornos de ejecución ofrecen una forma sencilla y flexible de crear, reutilizar y escalar contenido de automatización.|
| Ansible Content Collections| Las colecciones de contenido de Ansible facilitan a los creadores y desarrolladores de contenido de Ansible poner en marcha la automatización más rápido. Las colecciones de contenido certificadas de Ansible están respaldadas por Red Hat y un sólido ecosistema de socios. Son bloques de construcción de contenido de automatización flexibles y confiables para una variedad de casos de uso.|
| Automation hub| El centro de automatización proporciona un lugar para que los clientes de Ansible Automation Platform encuentren, usen y extiendan rápidamente contenido que sea compatible con Red Hat y sus socios tecnológicos, para brindar tranquilidad adicional en los entornos más exigentes. El centro de automatización privado también está disponible y ofrece a los clientes un repositorio de imágenes de contenedor de sus entornos de ejecución como una instancia local de centro de automatización. |
| Ansible content tools | Ansible Automation Platform 2 incluye dos nuevas herramientas diseñadas para ayudar a que la creación y la implementación de entornos de ejecución sean una experiencia de creación más fluida. Se incluirán herramientas de contenido adicionales de Ansible en futuras versiones de la plataforma. El generador de entornos de ejecución (ansible-builder) es una herramienta de línea de comandos que ayuda a construir entornos Ansible en contenedores usando podman. Permite a los creadores y operadores de automatización crear entornos de ejecución personalizados con el contenido exacto de Ansible necesario para su automatización. El navegador de contenido de automatización (ansible-navigator) proporciona una interfaz de plataforma de nivel superior (a través de CLI o TUI) para los creadores de automatización de Ansible. Proporciona una experiencia de creación de contenido de automatización de nivel superior más coherente, coherente y predecible, diseñada para ayudar al desarrollador empresarial de Ansible. |
| Red Hat Insights for Ansible Automation Platform| Red Hat Insights for Ansible Automation Platform permite a los arquitectos rastrear y solucionar problemas de éxito en el trabajo y medir cómo los equipos coordinan los procesos de automatización en los dominios de TI. También ayuda a los operadores y administradores a mantener Red Hat Ansible Automation Platform funcionando de manera eficiente y óptima, a identificar dónde fallan trabajos específicos e informar sobre proyectos de automatización en toda la infraestructura de un extremo a otro.|
| Automation services catalog| El catálogo de servicios de automatización es un medio para que los usuarios administren, aprovisionen y retiren los recursos de automatización, para facilitar el modelado y la entrega. Brinda a los creadores de automatización y usuarios comerciales acceso de autoservicio en entornos físicos, virtuales, en la nube y de contenedores, lo que facilita la ejecución de proyectos de automatización. Simultáneamente brinda a los usuarios de automatización empresarial y de línea de negocios la gobernanza que necesitan para cumplir con los requisitos de cumplimiento y adquisiciones.|

---

# Planificar setup inicial Ansible. (Demostración)

<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans106.png?raw=true"width="800" height="400"></p>
<p>

## **Requerimientos previos**

### **Control Node**

- Suscripcion valida de Red Hat Ansible Automation Platform.
- Registrarse al canal **ansible-2-for-rhel-8-x86_64-rpms** e instalar el paquete ansible con **yum install ansible**.
- Python:2 (version:2.7 o superior) o Python:3 (version:3.5 o superior), para Red Hat Enterprise Linux 8 se puede utilizar **"yum install platform-python"** del AppStream.

### **Managed Node**

- Suscripcion valida de Red Hat Enterprise Linux.
- Python:2 (version:2.6 o superior) o Python:3 (version:3.5 o superior), para Red Hat Enterprise Linux 8 se puede utilizar **"yum install platform-python"**. También se puede utilizar **"yum module install python36"**.
- Si, selinux esta habilitado en los managed nodes asegurarse que el paquete **python3-libselinux** esta instalado.

---
## **Instalar Ansible en el Control Node**

1. Listar repositorios disponibles y validar que contamos con ansible-2.9-for-rhel-8-x86_64-rpms

```
[root@server09 ~]# subscription-manager repos --list
+----------------------------------------------------------+
    Available Repositories in /etc/yum.repos.d/redhat.repo
+----------------------------------------------------------+
Repo ID:   rhel-8-for-x86_64-baseos-rpms
Repo Name: Red Hat Enterprise Linux 8 for x86_64 - BaseOS (RPMs)
Repo URL:  https://satellite.opennova.pe/pulp/repos/OpenNova/Library/content/dist/rhel8/$releasever/x86_64/baseos/os
Enabled:   1

Repo ID:   satellite-tools-6.9-for-rhel-8-x86_64-rpms
Repo Name: Red Hat Satellite Tools 6.9 for RHEL 8 x86_64 (RPMs)
Repo URL:  https://satellite.opennova.pe/pulp/repos/OpenNova/Library/content/dist/layered/rhel8/x86_64/sat-tools/6.9/os
Enabled:   1

Repo ID:   ansible-2.9-for-rhel-8-x86_64-rpms
Repo Name: Red Hat Ansible Engine 2.9 for RHEL 8 x86_64 (RPMs)
Repo URL:  https://satellite.opennova.pe/pulp/repos/OpenNova/Library/content/dist/layered/rhel8/x86_64/ansible/2.9/os
Enabled:   0

Repo ID:   rhel-8-for-x86_64-appstream-rpms
Repo Name: Red Hat Enterprise Linux 8 for x86_64 - AppStream (RPMs)
Repo URL:  https://satellite.opennova.pe/pulp/repos/OpenNova/Library/content/dist/rhel8/$releasever/x86_64/appstream/os
Enabled:   1
```

2. Habilitar en el nodo de control el repositorio **ansible-2.9-for-rhel-8-x86_64-rpms**
```
[root@server09 ~]# subscription-manager repos --enable=ansible-2.9-for-rhel-8-x86_64-rpms
Repository 'ansible-2.9-for-rhel-8-x86_64-rpms' is enabled for this system.

[root@server09 ~]# yum repolist
Updating Subscription Management repositories.
repo id                                                   repo name
ansible-2.9-for-rhel-8-x86_64-rpms                        Red Hat Ansible Engine 2.9 for RHEL 8 x86_64 (RPMs)
rhel-8-for-x86_64-appstream-rpms                          Red Hat Enterprise Linux 8 for x86_64 - AppStream (RPMs)
rhel-8-for-x86_64-baseos-rpms                             Red Hat Enterprise Linux 8 for x86_64 - BaseOS (RPMs)
satellite-tools-6.9-for-rhel-8-x86_64-rpms                Red Hat Satellite Tools 6.9 for RHEL 8 x86_64 (RPMs)
```

3. Instalar Python en el nodo de control
```
[root@server09 ~]# yum install platform-python -y
Updating Subscription Management repositories.
Red Hat Ansible Engine 2.9 for RHEL 8 x86_64 (RPMs)                                                                  7.9 MB/s | 2.0 MB     00:00
Red Hat Enterprise Linux 8 for x86_64 - BaseOS (RPMs)                                                                 26 kB/s | 2.4 kB     00:00
Red Hat Enterprise Linux 8 for x86_64 - AppStream (RPMs)                                                              43 kB/s | 2.8 kB     00:00
Red Hat Satellite Tools 6.9 for RHEL 8 x86_64 (RPMs)                                                                  25 kB/s | 2.1 kB     00:00
Package platform-python-3.6.8-37.el8.x86_64 is already installed.
Dependencies resolved.
=====================================================================================================================================================
 Package                           Architecture             Version                            Repository                                       Size
=====================================================================================================================================================
Upgrading:
 platform-python                   x86_64                   3.6.8-38.el8_4                     rhel-8-for-x86_64-baseos-rpms                    84 k
 python3-libs                      x86_64                   3.6.8-38.el8_4                     rhel-8-for-x86_64-baseos-rpms                   7.8 M

Transaction Summary
=====================================================================================================================================================
Upgrade  2 Packages

Total download size: 7.9 M
Downloading Packages:
(1/2): platform-python-3.6.8-38.el8_4.x86_64.rpm                                                                     818 kB/s |  84 kB     00:00
(2/2): python3-libs-3.6.8-38.el8_4.x86_64.rpm                                                                         55 MB/s | 7.8 MB     00:00
-----------------------------------------------------------------------------------------------------------------------------------------------------
Total                                                                                                                 55 MB/s | 7.9 MB     00:00
Running transaction check
Transaction check succeeded.
Running transaction test
Transaction test succeeded.
Running transaction
  Preparing        :                                                                                                                             1/1
  Upgrading        : platform-python-3.6.8-38.el8_4.x86_64                                                                                       1/4
  Running scriptlet: platform-python-3.6.8-38.el8_4.x86_64                                                                                       1/4
  Upgrading        : python3-libs-3.6.8-38.el8_4.x86_64                                                                                          2/4
  Cleanup          : python3-libs-3.6.8-37.el8.x86_64                                                                                            3/4
  Cleanup          : platform-python-3.6.8-37.el8.x86_64                                                                                         4/4
  Running scriptlet: platform-python-3.6.8-37.el8.x86_64                                                                                         4/4
  Verifying        : python3-libs-3.6.8-38.el8_4.x86_64                                                                                          1/4
  Verifying        : python3-libs-3.6.8-37.el8.x86_64                                                                                            2/4
  Verifying        : platform-python-3.6.8-38.el8_4.x86_64                                                                                       3/4
  Verifying        : platform-python-3.6.8-37.el8.x86_64                                                                                         4/4
Installed products updated.
Uploading Tracer Profile

Upgraded:
  platform-python-3.6.8-38.el8_4.x86_64                                      python3-libs-3.6.8-38.el8_4.x86_64

Complete!
```

4. Instalar ansible en el nodo de control
```
[root@server09 ~]# yum install -y ansible
Updating Subscription Management repositories.
Red Hat Ansible Engine 2.9 for RHEL 8 x86_64 (RPMs)                                               28 kB/s | 2.4 kB     00:00
Red Hat Enterprise Linux 8 for x86_64 - BaseOS (RPMs)                                             29 kB/s | 2.4 kB     00:00
Red Hat Enterprise Linux 8 for x86_64 - AppStream (RPMs)                                          37 kB/s | 2.8 kB     00:00
Red Hat Satellite Tools 6.9 for RHEL 8 x86_64 (RPMs)                                              29 kB/s | 2.1 kB     00:00
Dependencies resolved.
=================================================================================================================================
 Package                         Architecture      Version                   Repository                                     Size
=================================================================================================================================
Installing:
 ansible                         noarch            2.9.26-1.el8ae            ansible-2.9-for-rhel-8-x86_64-rpms             17 M
Installing dependencies:
 python3-babel                   noarch            2.5.1-5.el8               rhel-8-for-x86_64-appstream-rpms              4.8 M
 python3-cffi                    x86_64            1.11.5-5.el8              rhel-8-for-x86_64-baseos-rpms                 238 k
 python3-cryptography            x86_64            3.2.1-4.el8               rhel-8-for-x86_64-baseos-rpms                 559 k
 python3-jinja2                  noarch            2.10.1-2.el8_0            rhel-8-for-x86_64-appstream-rpms              538 k
 python3-markupsafe              x86_64            0.23-19.el8               rhel-8-for-x86_64-appstream-rpms               39 k
 python3-ply                     noarch            3.9-9.el8                 rhel-8-for-x86_64-baseos-rpms                 111 k
 python3-pycparser               noarch            2.14-14.el8               rhel-8-for-x86_64-baseos-rpms                 109 k
 python3-pytz                    noarch            2017.2-9.el8              rhel-8-for-x86_64-appstream-rpms               54 k
 python3-pyyaml                  x86_64            3.12-12.el8               rhel-8-for-x86_64-baseos-rpms                 193 k
 sshpass                         x86_64            1.06-3.el8ae              ansible-2.9-for-rhel-8-x86_64-rpms             27 k
Installing weak dependencies:
 python3-jmespath                noarch            0.9.0-11.el8              rhel-8-for-x86_64-appstream-rpms               45 k

Transaction Summary
=================================================================================================================================
Install  12 Packages

Total download size: 24 M
Installed size: 124 M
Downloading Packages:
(1/12): sshpass-1.06-3.el8ae.x86_64.rpm                                                          288 kB/s |  27 kB     00:00
(2/12): python3-pyyaml-3.12-12.el8.x86_64.rpm                                                    1.7 MB/s | 193 kB     00:00
(3/12): python3-pycparser-2.14-14.el8.noarch.rpm                                                 2.4 MB/s | 109 kB     00:00
(4/12): python3-cffi-1.11.5-5.el8.x86_64.rpm                                                     5.2 MB/s | 238 kB     00:00
(5/12): python3-cryptography-3.2.1-4.el8.x86_64.rpm                                               14 MB/s | 559 kB     00:00
(6/12): python3-ply-3.9-9.el8.noarch.rpm                                                         2.6 MB/s | 111 kB     00:00
(7/12): python3-jmespath-0.9.0-11.el8.noarch.rpm                                                 1.4 MB/s |  45 kB     00:00
(8/12): python3-pytz-2017.2-9.el8.noarch.rpm                                                     1.6 MB/s |  54 kB     00:00
(9/12): python3-markupsafe-0.23-19.el8.x86_64.rpm                                                897 kB/s |  39 kB     00:00
(10/12): python3-jinja2-2.10.1-2.el8_0.noarch.rpm                                                 12 MB/s | 538 kB     00:00
(11/12): ansible-2.9.26-1.el8ae.noarch.rpm                                                        52 MB/s |  17 MB     00:00
(12/12): python3-babel-2.5.1-5.el8.noarch.rpm                                                     45 MB/s | 4.8 MB     00:00
---------------------------------------------------------------------------------------------------------------------------------
Total                                                                                             64 MB/s |  24 MB     00:00
Running transaction check
Transaction check succeeded.
Running transaction test
Transaction test succeeded.
Running transaction
  Preparing        :                                                                                                         1/1
  Installing       : python3-markupsafe-0.23-19.el8.x86_64                                                                  1/12
  Installing       : python3-pytz-2017.2-9.el8.noarch                                                                       2/12
  Installing       : python3-babel-2.5.1-5.el8.noarch                                                                       3/12
  Installing       : python3-jinja2-2.10.1-2.el8_0.noarch                                                                   4/12
  Installing       : python3-jmespath-0.9.0-11.el8.noarch                                                                   5/12
  Installing       : python3-ply-3.9-9.el8.noarch                                                                           6/12
  Installing       : python3-pycparser-2.14-14.el8.noarch                                                                   7/12
  Installing       : python3-cffi-1.11.5-5.el8.x86_64                                                                       8/12
  Installing       : python3-cryptography-3.2.1-4.el8.x86_64                                                                9/12
  Installing       : python3-pyyaml-3.12-12.el8.x86_64                                                                     10/12
  Installing       : sshpass-1.06-3.el8ae.x86_64                                                                           11/12
  Installing       : ansible-2.9.26-1.el8ae.noarch                                                                         12/12
  Running scriptlet: ansible-2.9.26-1.el8ae.noarch                                                                         12/12
  Verifying        : ansible-2.9.26-1.el8ae.noarch                                                                          1/12
  Verifying        : sshpass-1.06-3.el8ae.x86_64                                                                            2/12
  Verifying        : python3-pyyaml-3.12-12.el8.x86_64                                                                      3/12
  Verifying        : python3-pycparser-2.14-14.el8.noarch                                                                   4/12
  Verifying        : python3-cffi-1.11.5-5.el8.x86_64                                                                       5/12
  Verifying        : python3-cryptography-3.2.1-4.el8.x86_64                                                                6/12
  Verifying        : python3-ply-3.9-9.el8.noarch                                                                           7/12
  Verifying        : python3-jmespath-0.9.0-11.el8.noarch                                                                   8/12
  Verifying        : python3-pytz-2017.2-9.el8.noarch                                                                       9/12
  Verifying        : python3-markupsafe-0.23-19.el8.x86_64                                                                 10/12
  Verifying        : python3-jinja2-2.10.1-2.el8_0.noarch                                                                  11/12
  Verifying        : python3-babel-2.5.1-5.el8.noarch                                                                      12/12
Installed products updated.
Uploading Tracer Profile

Installed:
  ansible-2.9.26-1.el8ae.noarch               python3-babel-2.5.1-5.el8.noarch         python3-cffi-1.11.5-5.el8.x86_64
  python3-cryptography-3.2.1-4.el8.x86_64     python3-jinja2-2.10.1-2.el8_0.noarch     python3-jmespath-0.9.0-11.el8.noarch
  python3-markupsafe-0.23-19.el8.x86_64       python3-ply-3.9-9.el8.noarch             python3-pycparser-2.14-14.el8.noarch
  python3-pytz-2017.2-9.el8.noarch            python3-pyyaml-3.12-12.el8.x86_64        sshpass-1.06-3.el8ae.x86_64

Complete!
```

## **Instalar Requerimientos en el Managed Node**
1. Instalar Python en el nodo administrado
```
[root@client91 ~]# yum install platform-python -y
Updating Subscription Management repositories.
Red Hat Ansible Engine 2.9 for RHEL 8 x86_64 (RPMs)                                                                  7.9 MB/s | 2.0 MB     00:00
Red Hat Enterprise Linux 8 for x86_64 - BaseOS (RPMs)                                                                 26 kB/s | 2.4 kB     00:00
Red Hat Enterprise Linux 8 for x86_64 - AppStream (RPMs)                                                              43 kB/s | 2.8 kB     00:00
Red Hat Satellite Tools 6.9 for RHEL 8 x86_64 (RPMs)                                                                  25 kB/s | 2.1 kB     00:00
Package platform-python-3.6.8-37.el8.x86_64 is already installed.
Dependencies resolved.
=====================================================================================================================================================
 Package                           Architecture             Version                            Repository                                       Size
=====================================================================================================================================================
Upgrading:
 platform-python                   x86_64                   3.6.8-38.el8_4                     rhel-8-for-x86_64-baseos-rpms                    84 k
 python3-libs                      x86_64                   3.6.8-38.el8_4                     rhel-8-for-x86_64-baseos-rpms                   7.8 M

Transaction Summary
=====================================================================================================================================================
Upgrade  2 Packages

Total download size: 7.9 M
Downloading Packages:
(1/2): platform-python-3.6.8-38.el8_4.x86_64.rpm                                                                     818 kB/s |  84 kB     00:00
(2/2): python3-libs-3.6.8-38.el8_4.x86_64.rpm                                                                         55 MB/s | 7.8 MB     00:00
-----------------------------------------------------------------------------------------------------------------------------------------------------
Total                                                                                                                 55 MB/s | 7.9 MB     00:00
Running transaction check
Transaction check succeeded.
Running transaction test
Transaction test succeeded.
Running transaction
  Preparing        :                                                                                                                             1/1
  Upgrading        : platform-python-3.6.8-38.el8_4.x86_64                                                                                       1/4
  Running scriptlet: platform-python-3.6.8-38.el8_4.x86_64                                                                                       1/4
  Upgrading        : python3-libs-3.6.8-38.el8_4.x86_64                                                                                          2/4
  Cleanup          : python3-libs-3.6.8-37.el8.x86_64                                                                                            3/4
  Cleanup          : platform-python-3.6.8-37.el8.x86_64                                                                                         4/4
  Running scriptlet: platform-python-3.6.8-37.el8.x86_64                                                                                         4/4
  Verifying        : python3-libs-3.6.8-38.el8_4.x86_64                                                                                          1/4
  Verifying        : python3-libs-3.6.8-37.el8.x86_64                                                                                            2/4
  Verifying        : platform-python-3.6.8-38.el8_4.x86_64                                                                                       3/4
  Verifying        : platform-python-3.6.8-37.el8.x86_64                                                                                         4/4
Installed products updated.
Uploading Tracer Profile

Upgraded:
  platform-python-3.6.8-38.el8_4.x86_64                                      python3-libs-3.6.8-38.el8_4.x86_64

Complete!
```
Repetir los pasos del **1 al 3** para los clientes: **clienteX2, clienteX3, clienteX4**. Donde **X** es el **numero del usuario** asignado. 


## **Configurar espacio de trabajo y recursos en el nodo de control**

Se debe definir un usuario de automatización para toda la infraestructura, en nuestro taller el usuario ansible será el usuario de automatización, el mismo requiere cierta configuración tanto en el nodo de control como en los nodos administrador.

1. Crear el usuario ansible en el nodo de control y asignarle el password redhat
```
[root@server09 ~]# useradd ansible
[root@server09 ~]# id ansible
uid=1000(ansible) gid=1000(ansible) groups=1000(ansible)

[root@server09 ~]# echo "redhat" | passwd stdin ansible
```

2. Configurarle permisos sudo al usuario ansible en el nodo de control
```
[root@server09 ~]# echo "ansible ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/ansible

[root@server09 ~]# cat /etc/sudoers.d/ansible
ansible ALL=(ALL)       NOPASSWD: ALL
```

3. Crear par de llaves ssh para el usuario ansible
```
[root@server09 ~]# su - ansible
[root@server09 ~]# ssh-keygen -t rsa -f ~/.ssh/id_rsa -N ""
```

4. Configurar editor vim y crear espacio de trabajo
```
[ansible@server09 ~]$ echo "autocmd filetype yaml setlocal ai ts=2 sw=2 et" > ~/.vimrc


```



## **Configurar espacio de trabajo y recursos en los nodos administrados (Procedimiento manual clientes)**
1. Crear usuario ansible en el nodo administrado
```
[root@client91 ~]# useradd ansible
[root@client91 ~]# id ansible
uid=1000(ansible) gid=1000(ansible) groups=1000(ansible)
```

2. Configurarle permisos sudo al usuario ansible en el nodo administrador
```
[root@client91 ~]# echo "ansible ALL=(ALL)       NOPASSWD: ALL" > /etc/sudoers.d/ansible

[root@client91 ~]# cat /etc/sudoers.d/ansible
ansible ALL=(ALL)       NOPASSWD: ALL
```

## **Configurar espacio de trabajo y recursos en los nodos administrador (Procedimiento vía ansible)**


|Plataforma | Arquitecturas |
| --- | --- |
|Red Hat Enterprise Linux 8 | x86_64, ppc_64, s390x|

