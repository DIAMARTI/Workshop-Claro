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
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans203.png?raw=true"width="800" height="400"></p>

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
### **Utilización de Ansible para comandos específicos (Adhoc commands)**

<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans201.png?raw=true"></p>

Puede ejecutar comandos específicos con Ansible si ejecuta uno o llama a un módulo directamente desde la línea de comandos, lo cual implica que no es necesario que utilice playbooks. 

Aunque esta acción sirve para las tareas que ocurren por única vez, deberá usar un playbook de Ansible para las más complejas.

---
# Que son Playbooks, Roles y Colecciones
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans202.png?raw=true"></p>

### **Playbooks, Roles y Colecciones y YAML para Ansible**

<br>Los playbooks de Ansible se utilizan para organizar los procesos de TI. Un playbook es un archivo YAML que contiene por lo menos un play, y que sirve para definir el estado deseado de un sistema. No es lo mismo que un módulo de Ansible, el cual es un script independiente que se puede utilizar dentro de un playbook de Ansible. 

Los plays son un conjunto ordenado de tareas que se ejecutan en las selecciones del host desde el archivo de inventario de Ansible. 

Las tareas son los elementos que llaman a los módulos de Ansible y que conforman un play, y se ejecutan allí en el mismo orden en que se escribieron.  

Cuando Ansible comienza a funcionar, puede hacer un seguimiento del estado de un sistema. Si al hacerlo detecta que la descripción del playbook sobre el sistema no coincide con su estado real, la plataforma implementará todos los cambios necesarios para que se cumpla esta correspondencia. 

Ansible incluye un "modo de verificación" que le muestra lo que la plataforma podría hacer, pero sin que se implementen cambios concretos. De este modo, usted puede validar los playbooks y los comandos específicos antes de llevar a cabo una modificación en el estado del sistema. 

<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans204.png?raw=true"width="800" height="400"></p>

Los controladores en Ansible (handlers) sirven para ejecutar una tarea específica luego de que se haya realizado un cambio en el sistema. Los activan las tareas, y se ejecutan una sola vez, después de todos los demás plays del playbook. 

Las variables, que son un concepto de Ansible que le permite modificar la ejecución de los playbooks, sirven para explicar las diferencias entre los sistemas, como las versiones de los paquetes o las rutas de los archivos. Ansible posibilita la ejecución de playbooks en diferentes sistemas. 

Las variables de Ansible se deben definir en función de la tarea que esté realizando el playbook. 

Estas siguen un orden de prioridad que establece cuáles prevalecerán sobre otras, lo cual debe tener en cuenta a la hora de incluir variables en el playbook.

Para trabajar con Ansible, también tendrá que comprender de qué se tratan las colecciones. Las colecciones son un formato de distribución para el contenido de Ansible que puede incluir playbooks, funciones, módulos y plugins.

Las funciones de Ansible (Roles) son un tipo de playbook especial completamente autónomo y portátil que incluye las tareas, las variables, las plantillas de configuración y otros archivos de soporte que son necesarios para completar una organización compleja. 

Una colección puede contener varias funciones (Roles) y módulos específicos que no estan necesariamente en una instalación de ansible, lo cual posibilita el intercambio sencillo de contenido a través de Automation Hub y Ansible Galaxy. 
<br>
#### Con ansible podemos automatizar toda la infraestructura tecnológica.
<p align="left"><img src="https://github.com/workshopopennova/tecnologiasredhat/blob/master/ans/ans206.png?raw=true"width="600" height="500"></p>
<br>

---

# Trabajando con Playbooks y Roles Ansible. (Demostración)

