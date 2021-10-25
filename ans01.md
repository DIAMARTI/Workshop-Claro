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




**Gestión de la configuración - Soporte Puppet 5**

|Plataforma | Arquitecturas |
| --- | --- |
|Red Hat Enterprise Linux 8 | x86_64, ppc_64, s390x|
|Red Hat Enterprise Linux 7 | x86_64, aarch64, ppc64le|
|Red Hat Enterprise Linux 6 | x86_64, i386|
|Red Hat Enterprise Linux 5 | x86_64, i386|

