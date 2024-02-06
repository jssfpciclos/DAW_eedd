# SDKMAN, ¿Qué es, cómo se instala y cómo se usa?

SDKMan es una heramienta que permite instalar y gestionar múltiples versiones de SDKs de diferentes lenguajes de programación, como Java, Groovy, Kotlin, Scala, entre otros.

### ¿Qué es un SDKMAN? <hr>


**SDKMAN!** es una herramienta que nos permite manejar la instalación y configuración de diversas versiones de SDKs (Software Developments Kits) mediante línea de comandos. Inicialmente, fue conocido como GVM (Groovy enVironment Manager) y está inspirado en otras herramientas utilizadas por la comunidad Ruby.

En nuestro día a día como desarrolladores, nos encontramos a veces ante aplicaciones que funcionan y deben compilar en versiones muy diferentes su SDK. Por ejemplo, de Java 1.8, 11, posterior, anterior, etc. También nos ocurre lo mismo con `Maven` y con otros SDKs. 

Cada vez que queremos cambiar de versión, se hace tedioso el tener que buscar, descargar, instalar y configurar nuestro sistema operativo para que utilice esta versión recientemente instalada. Para ello, tenemos a nuestra disposición aplicaciones como SDKMAN!.

### Características de SDKMAN! <hr>

- Centrado en JDKs de la JVM: Java, Groovy, Scala, Kotlin y Ceylon. Ant, Gradle, Grails, Maven, SBT, Spark, Spring Boot, Vert.
- Ligero al ser por lineal de comandos.
- Multiplataforma
- Open Source con licencia Apache 2.0.


### Instalación de SDKMAN! en Windows

En su [web](https://sdkman.io/), nos proporciona una instalación muy sencilla para Linux y Mac, pero en nuestro caso vamos a instalarlo en nuestro Windows 10/11.

La instalación en Windows nos plantea un problema inicial, y es que se realiza con un `script bash`. Para la instalación hemos utilizado la consola de `GitBash` que se nos instaló junto al Git.

```bash
curl -s "https://get.sdkman.io" | bash
```

> 🚧 **Aviso**
> Una vez ejecutamos este comando, nos da un error: no encuentra zip, unzip. Para solventarlo, se puede realizar de dos formas.
> 1. Instalar `zip` y `unzip` dentro de GitBash.
> 2. Modificar el script de instalación.


#### Modificar el script de instalación

1. Descargar el script de instalación.

```bash
curl -s "https://get.sdkman.io" > sdkman.sh
```

2. Modificar el script `sdkman.sh` y comentar el fragmento de código que se indica a continuación.

```bash
#echo "Looking for unzip..."
#if ! command -v unzip > /dev/null; then
#    echo "Not found."
#    echo "======================================================================================================"
#    echo " Please install unzip on your system using your favourite package manager."
#    echo ""
#    echo " Restart after installing unzip."
#    echo "======================================================================================================"
#    echo ""
#    exit 1
#fi

#echo "Looking for zip..."
#if ! command -v zip > /dev/null; then
#    echo "Not found."
#    echo "======================================================================================================"
#    echo " Please install zip on your system using your favourite package manager."
#    echo ""
#    echo " Restart after installing zip."
#    echo "======================================================================================================"
#    echo ""
#    exit 1
#fi
```

Una vez comentado este fragmento de código, podemos instalarlo mediante el comando:

```bash
bash sdkman.sh
```


### Ejemplo de cómo usar SDKMAN!

Una vez tengamos instalado el SDKMAN! mediante nuestra terminal podemos realizar la instalación de distintas versiones de SDKs en nuestro sistema. A continuación, ilustraremos ejemplos de cómo instalar varias versiones de Java.

```bash	
sdk list java
```

Mediante este comando, podemos visualizar un listado de todas las versiones de la JDK de Java que tenemos instaladas, la que tenemos configurada por defecto, las que podemos instalar, etc. Tal y como se muestra en la siguiente imagen:

<img src="https://profile.es/wp-content/media/versiones-jdk-java.jpg.webp">

Para instalar/desinstalar/cambiar uso o cambiar el que usaremos por defecto, utilizaremos el identificador de la columna Identifier. Observamos que actualmente tenemos instalada por defecto la 11.0.12 open de Java.net. Si quisiéramos cambiar a la 8.322.06.1 de Amazon, tendríamos que realizar el siguiente comando:

```bash
$ sdk use java  8.322.06.1-amzn

Using java version 8.322.06.1-amzn in this shell.
```

Tenemos la opción de utilizar para esta consola, por defecto o de manera predeterminada.

Como hemos indicado, todo esto se puede hacer para Java, Kotlin, Groovy, Maven, Scala y un largo etcétera de SDKs que nos proporciona esta herramienta. Seguidamente, se incluye enlaces al portal de SDKMAN! en los que podemos ver todas las JDKs y SDKs que nos proporcionan, así como más ejemplos de uso de los comandos:

- JDKs: https://sdkman.io/jdks
- SDKs: https://sdkman.io/sdks
- Ejemplos de uso: https://sdkman.io/usage

### Configurando nuestro IDE y las variables de entorno

Una vez instalado SDKMAN!. deberemos configurar las variables de entorno de nuestro Windows (si queremos usarlo en consola) o bien la ruta de la SDK de nuestro IDE para que apunte a la carpeta donde se encuentra la versión current seleccionada por SDKMAN!.

```bash	
~/.sdkman/candidates/java/current
```

En este caso, para cada SDK que SDKMAN! tenga instalado, tendremos varias carpetas con las versiones y una carpeta llamada current, donde se encuentra la versión que hayamos configurado como current.

Si utilizamos la ruta a esta current para la variable del entorno de Windows o de nuestro IDE, cada vez que cambiemos por consola la versión current tendremos nuestra consola y nuestros IDEs tirando de la versión que hayamos dictaminado por consola en el SDKMAN!. Esta es la gran ventaja que nos proporciona SDKMAN!: mediante un comando podemos ir saltando de una versión a otra de la SDK de una forma simple y rápida.

### Conclusión

En este artículo hemos diseccionado SDKMAN!, una poderosa herramienta para instalar y configurar diversas versiones de SDKs mediante línea de comandos. Así, hemos visto en qué consiste, sus características principales, cómo instalarla y un ejemplo de uso de cómo instalar varias versiones de Java con ella.
