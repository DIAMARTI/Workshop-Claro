<h1>Ansible Playbooks</h1>
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans100.png?raw=true"width="800" height="400"></p>
<p>
<strong>Meta:</strong>
<br>- Entendimiento Ansible Playbooks, Roles y Collecciones.
</p>
<p>
<strong>Objetivos:</strong>
<br>- Conceptos Playbooks, Roles y Collecciones (Teórico)
</p>
<p>
<strong>Secciones:</strong>
<br>- Ansible funcionamiento y comandos adhoc. (Teórico)
<br>- Que son Playbooks, Roles y Colecciones. (Teórico)
<br>- Trabajando con Ansible Playbooks y Roles. (Demostración) 
</p>
<p>
<strong>Laboratorios:</strong>
</p>

# Ansible funcionamiento y comandos adhoc. (Teórico)
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans100.jpg?raw=true"width="800" height="400"></p>

### **¿Cómo funciona Ansible?**
Ansible se conecta a los nodos y les inserta pequeños programas denominados módulos, los cuales permiten llevar a cabo tareas de automatización en la plataforma.

Esta ejecuta esos programas, los cuales funcionan como modelos de recursos del estado deseado de los sistemas, y, luego, los retira cuando finaliza la tarea.

Sin ellos, usted dependería de comandos específicos y de la creación de scripts para concretar una tarea. 

Como Ansible no necesita agentes, no se requiere instalar ningún software en los nodos que gestiona.

La plataforma lee información en el inventario para saber qué máquinas desea gestionar. Aunque Ansible cuenta con un archivo de inventario predeterminado, usted puede crear uno propio y definir los servidores que desea que administre. 

La plataforma utiliza el protocolo SSH para conectarse a los servidores y ejecutar las tareas. De forma predeterminada, utiliza claves y un agente SSH para conectarse a las máquinas virtuales con su nombre de usuario actual. No es necesario que inicie sesión como superusuario; puede hacerlo como cualquier otro y luego utilizar los comandos su o sudo para adquirir nuevos privilegios.

Una vez que Ansible se conecta, transfiere los módulos que requiere el comando o el playbook a la máquina remota para que los ejecute.

La plataforma utiliza plantillas YAML comprensibles para las personas, para que los usuarios no tengan que aprender un lenguaje de programación avanzado cuando deseen establecer la ejecución automática de tareas repetitivas.

---

<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans101.png?raw=true"width="600" height="400"></p>

### **Utilización de Ansible para comandos específicos (Adhoc commands)**
<br>
Puede ejecutar comandos específicos con Ansible si ejecuta uno o llama a un módulo directamente desde la línea de comandos, lo cual implica que no es necesario que utilice playbooks. 

<br>Aunque esta acción sirve para las tareas que ocurren por única vez, deberá usar un playbook de Ansible para las más complejas.

---
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans105.png?raw=true"width="500" height="230"></p>

# Que son Playbooks, Roles y Colecciones

### **Playbooks, Roles y Colecciones y YAML para Ansible**
<br>Los playbooks de Ansible se utilizan para organizar los procesos de TI. Un playbook es un archivo YAML que contiene por lo menos un play, y que sirve para definir el estado deseado de un sistema. No es lo mismo que un módulo de Ansible, el cual es un script independiente que se puede utilizar dentro de un playbook de Ansible. 

Los plays son un conjunto ordenado de tareas que se ejecutan en las selecciones del host desde el archivo de inventario de Ansible. 

Las tareas son los elementos que llaman a los módulos de Ansible y que conforman un play, y se ejecutan allí en el mismo orden en que se escribieron.  

Cuando Ansible comienza a funcionar, puede hacer un seguimiento del estado de un sistema. Si al hacerlo detecta que la descripción del playbook sobre el sistema no coincide con su estado real, la plataforma implementará todos los cambios necesarios para que se cumpla esta correspondencia. 

Ansible incluye un "modo de verificación" que le muestra lo que la plataforma podría hacer, pero sin que se implementen cambios concretos. De este modo, usted puede validar los playbooks y los comandos específicos antes de llevar a cabo una modificación en el estado del sistema. 

Los controladores en Ansible (handlers) sirven para ejecutar una tarea específica luego de que se haya realizado un cambio en el sistema. Los activan las tareas, y se ejecutan una sola vez, después de todos los demás plays del playbook. 

Las variables, que son un concepto de Ansible que le permite modificar la ejecución de los playbooks, sirven para explicar las diferencias entre los sistemas, como las versiones de los paquetes o las rutas de los archivos. Ansible posibilita la ejecución de playbooks en diferentes sistemas. 

Las variables de Ansible se deben definir en función de la tarea que esté realizando el playbook. 

Estas siguen un orden de prioridad que establece cuáles prevalecerán sobre otras, lo cual debe tener en cuenta a la hora de incluir variables en el playbook.

Para trabajar con Ansible, también tendrá que comprender de qué se tratan las colecciones. Las colecciones son un formato de distribución para el contenido de Ansible que puede incluir playbooks, funciones, módulos y plugins.

Las funciones de Ansible (Roles) son un tipo de playbook especial completamente autónomo y portátil que incluye las tareas, las variables, las plantillas de configuración y otros archivos de soporte que son necesarios para completar una organización compleja. 

Una colección puede contener varias funciones, lo cual posibilita el intercambio sencillo de contenido a través de Automation Hub y Ansible Galaxy. 
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