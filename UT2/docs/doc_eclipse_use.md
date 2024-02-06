# Primeros pasos con Eclipse (Java)

Este tutorial le ayudará a familiarizarse rápidamente con Eclipse, unos de los IDE más utilizados a nivel académico para el desarrollo de Java. Para utilizar Eclipse de forma eficaz, debe familiarizarse y comprender algunos conceptos y componentes clave del IDE: 
workspaces,

- Workbech, 
- Workspaces,
- Perpectivas,
- Editor, 
- Vistas
- Barra de herramientas.

Primero, veamos cómo descargar e instalar Eclipse IDE.

## 1. Descargue e instale Eclipse

Eclipse IDE está disponible en los principales sistemas operativos: Windows, Mac OS X y Linux. Admite arquitectura de CPU de 32 y 64 bits. Eclipse IDE es una aplicación basada en Java, por lo que primero requiere la instalación de JDK/JRE.

### Descargue e instale Eclipse IDE usando el instalador de Eclipse:
De esta forma, descargas un pequeño programa llamado Eclipse Installer. Ejecute este programa y elija el paquete que desee instalar:

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/dc61e4b2-c6b9-4a48-92a1-528ab30108cc" width="400px">

La instalación facilita mucho el resultado satisfactorio de la misma, ya que son muchos binarios y configuraciones las requeridas para un funcionamiento óptimo.

[Descargar el instalador de Eclipse de 64 bits](https://www.eclipse.org/downloads/download.php?file=/oomph/epp/2018-09/R/eclipse-inst-win64.exe)


## 2. Workbech

Una instancia de eclipse se le suele llamar "Workbech" o "banco de trabajo" (traducido literalmente). Un Workbech consiste de uno o más Perpectivas. Y una perpectiva contiene editores y vistas.

Se permite abrir múltoples instancias simultaneamente (via menu Windows-> New Window). Por ejemplo, cuando estamos trabajando sobre 2 proyectos (podemos abrir dos instancias), una para cada proyecto. Pero todos los `Workbechs` son udados para solo un `Workspaces`.

## 3. Workspaces

Workspaces o espacio de trabajo es un directorio en tu computadora (donde los proyectos son almacenadas). Se debe elegir un workspaces cuando se inicia Eclipse (aunque esto puede ser saltado si se elige un Workspaces por defecto.)

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/3272b398-dbf5-49c9-9a6b-18a3dd91484b">

Puede haber varios proyectos en un Workspaces, lo que significa que podemos trabajar con múltiples proyectos simultaneamente. Sin embargo, puedes trabajar in un solo workspaces en una sesión de trabajo de Eclipse. A para intercambiar a otro workspaces, click `File -> Switch` Workspaces desde el menu principal.

Elipse almacena las preferencias separadamente para cada workspaces dentro del `.metadata` directorio en la carpeta raíz del worksapces. Esto significa que cada workspaces tiene su propia configuración para diseños, JDKs, servidores, etc...