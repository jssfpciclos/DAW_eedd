# COVERTURA DE CÓDIGO

## Introducción

La cobertura de código es una técnica utilizada en el desarrollo de software para medir la cantidad de código que ha sido probado. La cobertura de código se utiliza para determinar si el código fuente de un programa ha sido probado adecuadamente y para identificar las partes del código que no han sido probadas.


## Tipos de cobertura de código

Existen varios tipos de cobertura de código, entre los que se incluyen:

- **Cobertura de instrucciones**: Mide la cantidad de instrucciones del código que han sido ejecutadas durante las pruebas.
- **Cobertura de ramas/condiciones**: Mide la cantidad de caminos de ejecución que han sido probados.
- **Cobertura de funciones**: Mide la cantidad de funciones que han sido ejecutadas durante las pruebas.
- **Cobertura de líneas**: Mide la cantidad de líneas de código que han sido ejecutadas durante las pruebas.


## Herramientas de cobertura de código

Existen varias herramientas de cobertura de código disponibles para diferentes lenguajes de programación. Algunas de las herramientas más populares son:

- **JaCoCo**: Herramienta de cobertura de código para Java.
- **Istanbul**: Herramienta de cobertura de código para JavaScript.
- **Cobertura**: Herramienta de cobertura de código para Java.
- **gcov**: Herramienta de cobertura de código para C y C++.
- **Coverlet**: Herramienta de cobertura de código para .NET.


## Ventajas de la cobertura de código

La cobertura de código tiene varias ventajas, entre las que se incluyen:

- **Identificación de código no probado**: Permite identificar las partes del código que no han sido probadas y que pueden contener errores.
- **Mejora de la calidad del código**: Ayuda a mejorar la calidad del código al identificar áreas que necesitan ser probadas.
- **Reducción de errores**: Al probar más partes del código, se reducen los errores en el software final.
- **Mejora de la confianza en el código**: Al tener una mayor cobertura de código, se aumenta la confianza en la calidad del software.
- **Facilita el mantenimiento del código**: Al identificar las partes del código que no han sido probadas, se facilita el mantenimiento del código.


## Integración con los IDEs

Muchos IDEs (Entornos de Desarrollo Integrados) ofrecen soporte para la cobertura de código, lo que facilita la visualización de la cobertura de código directamente desde el IDE. Algunos IDEs populares que ofrecen soporte para la cobertura de código son:

- **IntelliJ IDEA**: IDE para Java que ofrece soporte para la cobertura de código a través de un plugin (Code Coverage for Java).
- **Visual Studio**: IDE para .NET que ofrece soporte para la cobertura de código a través de plugins.
- **Rider**: IDE para .NET que ofrece soporte para la cobertura de código a través de un plugin (dotCover).
- **Eclipse**: IDE para Java que ofrece soporte para la cobertura de código a través de plugins (EclEmma, JaCoCo).




### Ejemplo práctico. Convertura de código en IntellJ IDEA

Para realizar la cobertura de código en IntelliJ IDEA, se puede utilizar el plugin Code Coverage for Java. Este plugin permite visualizar la cobertura de código directamente desde el IDE.

Para utilizar el plugin Code Coverage for Java en IntelliJ IDEA, se pueden seguir los siguientes pasos:

1. Instalar el plugin Code Coverage for Java desde el Marketplace de IntelliJ IDEA (o activarlo si ya está instalado).
2. Ejecutar las pruebas unitarias de la aplicación.
3. Abrir la ventana de cobertura de código desde el menú View > Tool Windows > Coverage.
4. Visualizar la cobertura de código en la ventana Coverage.

El plugin Code Coverage for Java muestra la cobertura de código en diferentes colores, lo que facilita identificar las partes del código que han sido probadas y las que no. Además, permite exportar los resultados de la cobertura de código en diferentes formatos (HTML, XML, etc.) para su análisis posterior.

En la ventana de cobertura de código, se pueden ver diferentes métricas de cobertura como:

- **Line,%**: Porcentaje de instrucciones ejecutadas, y total ejecutadas frente a total de instrucciones.
- **Branch,%**: Porcentaje de ramas/condiciones ejecutadas, y total ejecutadas frente a total de ramas.
- **Method,%**: Porcentaje de métodos ejecutados, y total ejecutados frente a total de métodos.
- **Class,%**: Porcentaje de clases ejecutadas, y total ejecutadas frente a total de clases.

La cobertura de código en IntelliJ IDEA es una herramienta muy útil para identificar las partes del código que no han sido probadas y que pueden contener errores. Además, ayuda a mejorar la calidad del código y a aumentar la confianza en el software final.

### Configurar opciones de covertura de código en IntelliJ IDEA

Para configurar las opciones de cobertura de código en IntelliJ IDEA, se pueden seguir los siguientes pasos:

1. Abrir la ventana de configuración de IntelliJ IDEA desde el menú File > Settings.
2. Ir a la sección de Build, Execution, Deployment > Coverage.
3. Configurar las opciones de cobertura de código según las necesidades del proyecto.
4. Guardar los cambios y cerrar la ventana de configuración.


> 💡 Para más información sobre la cobertura de código en IntelliJ IDEA, se puede consultar la [documentación oficial](https://www.jetbrains.com/help/idea/code-coverage.html) del IDE.