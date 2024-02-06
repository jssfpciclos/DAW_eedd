# TE2.1 - Configuración de Eclipse y JetBrains IntelliJ IDEA

En esta tarea de aprendizaje, aprenderás a instalar el JDK y JREs en Windows y Linux, y a configurar Eclipse y JetBrains IntelliJ IDEA.

## Recursos

- [Instalación del JDK en Linux](https://docs.oracle.com/javase/8/docs/technotes/guides/install/linux_jdk.html)
- [Instalación del JDK en Windows](https://docs.oracle.com/javase/8/docs/technotes/guides/install/windows_jdk_install.html)

### Objetivos

- Conocer cómo instalar el JDK/JRE en Windows y Linux.
- Conocer cómo configurar Eclipse y JetBrains IntelliJ IDEA para utilizar un JDK.
- Conocer cómo configurar Windows y Linux a nivel de sistema para utilizar diferentes versiones de Java.
- Conocer cómo instalar y usar la herramienta SDKMan para instalar diferentes versiones de Java en Linux/MacOS/Windows.

### Entrega

El documento justificativo de la realización de la tarea se realizará en formato `Markdown`, el nombre del fichero será `readme.md` y estará dentro de la carpeta `UT2\TE2.1` dentro del repositorio oficial del alumno para la asignatura.

El fichero `readme.md` debe contener los siguientes apartados:

- Cada uno de los puntos de la tarea.

### 1. Instalar el JDK en Windows

1. Revisa la configuración de tu máquina a través del terminal e indica la versión de Java que tienes instalada.

```bash
# Comprueba la versión de Java instalada
$> java -version
# Comprueba donde está instalado Java
$> where java
# Busca todas las versiones de Java instaladas
$> where java
```

📎 _Adjunta una imagen de los comandos anteriores y responde a las siguientes preguntas_

    ¿Qué versión de Java tienes instalada?

    ¿Cuantas versiones de Java tienes instaladas? ¿ Por qué?

    Si tienes más de una versión indica todas las versiones y rutas de instalación.

2. Variables de entorno.

   📎 _Adjunta una imagen de las variables de entorno de tu sistema, tanto a nivel de usuario como a nivel de sistema._

3. Instala el JDK 19 la implementación de Adoptium.

   - Ves a la página de [Adoptium](https://adoptium.net/) y descarga la versión de Java 19 para Window s y la arquitectura de tu PC (x32/x64).
     (Incluye un gif de la instalación)

   - Una vez instalado, muestra la versión de Java instalada y la ruta de instalación. (a través de comandos y adjunta una imagen)

   - ¿ La versión de Java que te muestra es la 19? ¿ Por qué?

4. Configura tu sistema para que utilice la versión de Java 19 como versión por defecto a nivel de usuario.

   - ¿ Cómo has configurado tu sistema para que utilice la versión de Java 19 como versión por defecto?

5. Instala el JDK

## ¿Cómo configuro Eclipse para que utilice un JDK?

Para

Aquí tienes un ejemplo de cómo configurar Eclipse para utilizar un JDK y establecer el Build Path:

Abre Eclipse y ve al menú "Window" (Ventana) y selecciona "Preferences" (Preferencias).
En la ventana de preferencias, expande la categoría "Java" y selecciona "Installed JREs" (JREs instalados).
Haz clic en el botón "Add" (Agregar) para agregar un nuevo JRE.
Selecciona la opción "Standard VM" (VM estándar) y haz clic en "Next" (Siguiente).
Haz clic en el botón "Directory" (Directorio) y selecciona la ubicación del directorio de instalación de tu JDK.
Haz clic en "Finish" (Finalizar) para agregar el JRE.
Ahora, ve a la categoría "Java" y selecciona "Build Path" (Ruta de compilación).
Haz clic en la pestaña "Libraries" (Bibliotecas) y luego en el botón "Add Library" (Agregar biblioteca).
Selecciona "JRE System Library" (Biblioteca del sistema JRE) y haz clic en "Next" (Siguiente).
Selecciona el JRE que agregaste anteriormente y haz clic en "Finish" (Finalizar).
Haz clic en "Apply and Close" (Aplicar y cerrar) para guardar los cambios.
Recuerda que estos pasos pueden variar ligeramente dependiendo de la versión de Eclipse que estés utilizando.
