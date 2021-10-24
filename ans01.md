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