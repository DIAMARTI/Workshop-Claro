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
<br>- Planificar setup inicial. (Teórico) Demostración
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

### **¿Qué es Infraestructura como codigo?**
<br>
<br>La infraestructura como código (IaC) es un enfoque para la gestión de infraestructuras de sistemas de TI que se basa en el uso de archivos de configuración repetibles para generar entornos de implementación consistentes para el desarrollo de CI/CD

Tipos de IaC:
- [Terraform](https://www.terraform.io)
- [CloudFormation](https://aws.amazon.com/es/cloudformation)
- <a href="https://www.terraform.io" target="_blank" rel="noopener noreferrer">Terraform</a>.
- <p>Check out <a href="https://www.freecodecamp.org/" target="_blank" rel="noopener noreferrer">freeCodeCamp</a>.</p>
<p>Check out <a href="https://www.freecodecamp.org/" target="_blank">freeCodeCamp</a>.</p>
- Azure ARM
- Ansible
- Chef, Puppet entre otros.


### **Características y beneficios de Red Hat Satellite**
<br>Red Hat Satellite automatiza muchas tareas relacionadas con la administración del sistema y se integra fácilmente en los marcos de flujo de trabajo existentes. La consola centralizada ofrece a los administradores una ubicación única para acceder a los informes y para aprovisionar, configurar y actualizar sistemas.

**Gestión de contenido**
<br>
<br>Red Hat Satellite ayuda a garantizar la aplicación sistemática de contenido, incluidos los parches, en los sistemas implementados, en infraestructuras físicas, virtuales o en la nube, en todas las etapas. Este enfoque promueve una mayor consistencia y disponibilidad del sistema y libera a TI para responder más rápidamente a las necesidades y vulnerabilidades del negocio.

| Característica | Beneficio |
| --- | --- |
| Vistas de contenido | Las vistas de contenido son colecciones de RPM, módulos Puppet, contenido de contenedor o contenido de OSTree refinado con filtros y reglas. Se publican y promueven a lo largo de los entornos de ciclo de vida, lo que permite la gestión del sistema de un extremo a otro.|
| Integración de Red Hat Content Delivery Network (CDN) |Permite a los usuarios controlar la sincronización del contenido de Red Hat directamente desde la interfaz de usuario.|
|Gestión del ciclo de vida| Permite la distribución, aprovisionamiento, configuración y entrega de contenido a través de Red Hat Satellite Capsule Server.|
|Sincronización de contenido optimizada|Permite a los usuarios crear sistemas casi inmediatamente después de la instalación mientras el contenido se descarga en segundo plano.|

**Gestión de actualizaciones**
<br>
<br>Garantice un entorno operativo estándar (SOE) obteniendo actualizaciones sobre parches de seguridad, actualizaciones y mejoras. Además, mejore rápidamente la seguridad del sistema al parchear varios sistemas a la vez.

| Característica | Beneficio |
| --- | --- |
| Capacidad para definir y gestionar SOE | Garantice SOE obteniendo actualizaciones sobre parches de seguridad, actualizaciones y mejoras.|
| Parche automatizado |Mejore rápidamente la seguridad del sistema parcheando cientos o miles de sistemas a la vez.|
|Gestión del ciclo de vida| Permite la distribución, aprovisionamiento, configuración y entrega de contenido a través de Red Hat Satellite Capsule Server.|
|Implementación y seguimiento de software de Red Hat y software de terceros |Implemente toda la infraestructura de Red Hat, así como el software de terceros, extrayendo todos esos bits de software en Satellite. Una vez que Satellite tiene ese contenido, también realiza un seguimiento de él, lo que mejora la seguridad y garantiza un mejor seguimiento de lo que se implementa en cada sistema.|

**Gestión de Aprovisionamiento**
<br>
<br>Los administradores pueden aprovisionar en infraestructura virtualizada, bare metal y en entornos de nube pública o privada, todo desde una consola centralizada mediante un proceso simple

| Característica | Beneficio |
| --- | --- |
| Aprovisionamiento en bare metal | Aprovisione y actualice rápidamente toda su infraestructura básica.|
|Aprovisionamiento en Red Hat Virtualization, Red Hat OpenStack® Platform, VMware o varios proveedores de nube| Cree y administre fácilmente instancias en infraestructura virtualizada o en entornos de nube pública y privada.|
|Aprovisionamiento mediante plantillas| Cree escenarios complejos de Kickstart y Preboot Execution Environment (PXE) con poderosas variables y fragmentos.|
|System discovery|Descubra y busque en hosts no aprovisionados para una implementación rápida, incluso en entornos donde el Protocolo de configuración dinámica de host (DHCP) y PXE no están disponibles.|

**Gestión de Configuración**
<br>
<br>Analice y corrija automáticamente la desviación y el control de la configuración, y aplique el estado final del host deseado, todo desde la interfaz de usuario de Red Hat Satellite. Esta interfaz le permite configurar de manera eficiente los sistemas Red Hat Enterprise Linux® para una mayor agilidad.

| Característica | Beneficio |
| --- | --- |
| Ejecución remota | Automatiza los flujos de trabajo y permite a los usuarios realizar múltiples acciones contra grupos de sistemas, incluido el reinicio de un sistema después de la instalación de un parche y la realización de actualizaciones continuas en cientos de sistemas.|
|Integración de Red Hat Insights| Utiliza análisis avanzados para ayudar a detectar riesgos, permite la creación de un plan Insights para remediar los riesgos y ayuda a ejecutar los Playbooks de Ansible® a través de la misma interfaz de satélite.|
|Integración de Red Hat Ansible Automation Platform|Permite la ejecución remota, la gestión del estado deseado y la automatización de la gestión de la configuración.|

**Gestión de suscripciones**
<br>
<br>Genere informes y mapee fácilmente sus productos Red Hat a sistemas registrados para una visibilidad de consumo de suscripción de un extremo a otro.

| Característica | Beneficio |
| --- | --- |
| Gestión de suscripciones | Importe y administre fácilmente la distribución de suscripciones de software de Red Hat.|
|Motor de informes integrado| Informe y mapee los productos comprados a los sistemas registrados dentro de Red Hat Satellite para una visibilidad de uso de suscripción de un extremo a otro.|



# Identificar componentes de Red Hat Satellite. (Teórico)


Red Hat Satellite 6 consta de varios proyectos de código abierto que están integrados, verificados, entregados y respaldados como Satellite 6. 
<br>Consta de los siguientes proyectos de código abierto:

<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat108.png?raw=true"width="700" height="280"></p>

### **Foreman**
Foreman es una aplicación de código abierto que se utiliza para el aprovisionamiento y la gestión del ciclo de vida de sistemas físicos y virtuales. Foreman configura automáticamente estos sistemas utilizando varios métodos, incluidos los módulos kickstart y Puppet. Foreman también proporciona datos históricos para informes, auditorías y resolución de problemas.

### **Katello**
Katello es un complemento de Foreman para la gestión de suscripciones y repositorios. Proporciona un medio para suscribirse a los repositorios de Red Hat y descargar contenido. Puede crear y administrar diferentes versiones de este contenido y aplicarlas a sistemas específicos dentro de las etapas definidas por el usuario del ciclo de vida de la aplicación.

### **Candlepin**
Candlepin es un servicio dentro de Katello que se encarga de la gestión de suscripciones.

### **Pulp**
Pulp es un servicio dentro de Katello que se encarga de la gestión de contenido y repositorios. Pulp asegura un espacio de almacenamiento eficiente al no duplicar los paquetes RPM incluso cuando lo solicitan Content Views en diferentes organizaciones.

### **Hammer**
Hammer es una herramienta CLI que proporciona equivalentes de línea de comandos y shell de la mayoría de las funciones de la interfaz de usuario web.

**REST API**
Red Hat Satellite 6 incluye un servicio de API RESTful que permite a los administradores y desarrolladores del sistema escribir scripts personalizados y aplicaciones de terceros que interactúan con Red Hat Satellite.

### **Puppet**
Red Hat Satellite 6 incluye paquetes Puppet compatibles. El programa de instalación permite a los usuarios instalar y configurar Puppet Masters como parte de Red Hat Satellite Capsule Servers. Un módulo Puppet, que se ejecuta en un Puppet Master en Red Hat Satellite Server o Satellite Capsule Server, también es compatible con Red Hat.

## Arquitecturas de cliente compatibles

**Soporte de gestión de contenido**

|Plataforma | Arquitecturas |
| --- | --- |
|Red Hat Enterprise Linux 8| x86_64, ppc_64, s390x |
|Red Hat Enterprise Linux 7| x86_64, ppc64 (BE), ppc64le, aarch64, s390x|
|Red Hat Enterprise Linux 6|x86_64, i386, s390x, ppc64 (BE)|
|Red Hat Enterprise Linux 5|x86_64, i386, s390x|

**Soporte de aprovisionamiento de host**

|Plataforma | Arquitecturas |
| --- | --- |
|Red Hat Enterprise Linux 8 | x86_64 |
|Red Hat Enterprise Linux 7 | x86_64 |
|Red Hat Enterprise Linux 6 | x86_64, i386 |
|Red Hat Enterprise Linux 5 | x86_64, i386 |

**Gestión de la configuración - Soporte Puppet 5**

|Plataforma | Arquitecturas |
| --- | --- |
|Red Hat Enterprise Linux 8 | x86_64, ppc_64, s390x|
|Red Hat Enterprise Linux 7 | x86_64, aarch64, ppc64le|
|Red Hat Enterprise Linux 6 | x86_64, i386|
|Red Hat Enterprise Linux 5 | x86_64, i386|

# Planificar escenarios de despliegue. (Teórico)
### **Arquitectura del sistema Red Hat Satellite 6**
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat101.png?raw=true" width="850" height="600"></p>


### **Topología de satélite con cápsula interna**
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat103.png?raw=true" width="850" height="600"></p>

### **Topología de satélite con cápsula aislada**
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/images/sat/sat102.png?raw=true" width="850" height="600"></p>