<h1>Tareas de Mantenimiento</h1>

<p>
<strong>Meta:</strong>
<br>Realizar operaciones de mantenimiento sobre la plataforma RH Satellite
</p>
<p>
<strong>Objetivos:</strong>
<br>- Respaldar la solucion
</p>
<p>
<strong>Secciones:</strong>
<br>- Gestión de clientes de satellite
</p>
<p>
<strong>Laboratorios:</strong>
<br><strong>- Registrar un sistema RHEL a la plataforma Satellite</strong>
<br><strong>- Gestión de actualizaciones de un sistema cliente</strong>
<br><strong>- Ejercicio propuesto 01</strong>
<br><strong>- Ejercicio propuesto 02</strong>
<br><strong>- Ejercicio propuesto 03</strong>
</p>

<strong>Requisitos:</strong>
<br><strong>- Satellite</strong>
<br><strong>- RHEL client</strong>

<h3><br><strong>## Respaldo y restauracion del sistema Satellite</strong></h3>

Para respaldar el sistema, usamos el comando foreman-maintain backup, por temas de laboratorio usamos el comando de bakcup sin respaldar los datos de pulp, estos datos ocupan mucho espacio, por ello para temas de laboratorio usamos la directiva --skip-pupl-content

<br>`# foreman-maintain backup offline --skip-pulp-content /var/satellite-backup/`

En caso hagamos un backup full y luego deseamos crear respaldos incrementales sobre ese backup full usamos

<br>`# satellite-maintain backup offline --incremental /var/backup_directory/full_backup  /var/backup_directory`

Podemos crear algunos usuarios o registros en la plataforma de Satellite y ejecutar un respaldo, luego borrar el registro o usuario y ejecutar un restore con
<br>`# satellite-maintain restore -w restore-installer-reset,pulp-migrate /var/backup_directory/full_backup`

En caso de alertas de error, pueden omitirse ya que los backup y restores son parciales por la directiva --skip-pulp-content, ignore esos errores y recuerde que en un ambiente de produccion el respaldo de pulp si esta presente.

<p><br><a href="sat">volver</a></p>