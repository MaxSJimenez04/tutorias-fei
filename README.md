# TutoriasFEI

## Descripción  
El proyecto **TutoriasFEI** tiene como objetivo registrar las sesiones de tutoría, gestionar los reportes generados y dar seguimiento a las problemáticas reportadas por los estudiantes.

## Tecnología Utilizada  
- **PHP**


## Base de Datos  
La base de datos del proyecto se encuentra en el archivo **db.sql**.

El diagrama de la base de datos muestra la estructura lógica de las tablas que conforman el sistema, así como sus relaciones. Este permite comprender mejor cómo fluye la información entre las entidades principales, como los estudiantes tutorados, los tutores, las sesiones de tutoría, las problemáticas reportadas, entre otras. Esta visualización facilita tareas como el mantenimiento, la ampliación de funcionalidades o la depuración de errores.


## Diagramas  
Los diagramas proporcionados se encuentran en la carpeta **diagrams**.

## Archivos de Datos  
En la carpeta **data**, se incluyen:  
- **insertTutoriados.xlsx**: Contiene información sobre los estudiantes tutorados. Aún falta agregar algunos datos, lo cual ya se comentó con la Mtra. Erika.  
- Archivos de Excel proporcionados originalmente, los cuales serán unificados en un solo documento con la información completa de los estudiantes.

## Despliegue del Proyecto  
- Durante el despliegue, asegúrese de configurar correctamente el archivo **.env** para la gestión del entorno.
- Instalar o tener instalado el gestor de dependencias Composer
- Ejecutar en la raíz del proyecto el comando:

```composer install```

- Se recomienda practicar el despliegue en un entorno local antes de realizarlo en un entorno de producción, ya que de lo contrario suelen surgir varios problemas técnicos durante el proceso.

## Control de versiones

A continuación se describen las convenciones para el nombrado de _commits_, _Pull Requests_ y ramas en Git, todos deberán escribirse en idioma inglés.

### Nombrado de commits

Cada commit deberá estar nombrado siguiendo la siguiente especificación:

```[TAG](OPCIONAL: Módulo afectado): Descripción del commit```
El `TAG` debe ser cualquiera de los siguientes, el que más se ajuste a lo que el cambio realizó:
* `feat`: indica que el commit está incluyendo un `feature` o funcionalidad nueva.  
* `config`: indica que el commit está cambiando algún archivo de configuración, instaló alguna biblioteca para el proyecto o cambió la estructura de organización de algún módulo o carpeta.  
* `fix`: indica que el commit está realizando un cambio sobre alguna funcionalidad existente, ya sea para resolver un bug, cambiar la lógica o mejorar el rendimiento.  
* `docs`: indica que el commit está realizando un cambio en documentos del repositorio fuera del código, como el archivo md README que se encuentra leyendo.  
* `revert`: reversión a un commit anterior.  
* `test`: indica que el commit agrega, corrige o elimina una prueba unitaria del proyecto.

La descripción debe ser concisa, si ocupa más de una línea, es mejor revisar si se deben realizar dos commits.

Ejemplos:
- ``fix(SessionReport): shows the table data correctly``
- ``feat: add French language``
- ``docs: spell correctly PROFESOR header in the report table``
[NOTA: Tanto el TAG como la descripción no deben empezar con Mayúsculas. No importa si se escribe en 3ra persona (shows, implements) o en imperativo/infinitivo (show, implement, create)]
El módulo es opcional si, este debe abarca alguna sección del sistema (ej. AdministrarEstudiantes, EditarReporte)
### Nombrado de pull requests (PR)
Para realizar un Pull Request, se debe nombrar de la siguiente manera:
- ```[TAG]: Resumen de lo que resuelve PR```
El [TAG] de los Pull Request es similar a los del commit, pero este se limita a los siguientes:

* `feat`: — Nueva funcionalidad
* `fix`: — Corrección de un error
* `refactor`: — Reestructuración interna de código sin cambiar comportamiento
* `chore`: — Mantenimiento, configuración, dependencias o tareas técnicas
* `docs`: — Cambios en documentación

El _resumen de lo que resuelve el PR_ es simplemente una descripción breve de qué realizan los commits del PR, por ejemplo:
* `refactor: optimize grades inquiry`, en este PR puede haber varios commits de diferentes módulos.
* `chore: update PHP version`, este puede ser un único commit (el cual puede tener el mismo título que el commit)

El pull request sigue las mismas reglas de escritura e idioma que el commit
### Nombrado de ramas
La estructura para el nombrado de ramas es la siguiente:
`[TAG]/descripcion-corta`

Los TAG para las ramas son los mismos que en los Pull Request, la diferencia radica en la descripción.
La descripción del commit debe estar en kebab-case, y debe tener máximo de 3 a 4 palabras

Ejemplos:
`feat/register-ee`
`fix/import-students-csv`
`fix/mail-sending-bug`

