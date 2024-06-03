# Examen 3ª Evaluación Entornos de Desarrollo

**Normas del Examen**

- Cada uno de los ejercicios hay que contestarlo en un fichero separado, según las indicaciones de cada ejercicio.
- Si necesitas añadir algún fichero adicional, existe una carpeta de `res` donde puedes añadir los ficheros necesarios.
- Se permite la consulta de los apuntes del módulo, así como la consulta de los ejercicios realizados por cada alumno.

**Restriciones**

- No se permite consultar internet, excepto la documentación oficial de las tecnologías utilizadas (PlantUML, Mermaid, JUnit5, etc.).
- No se puede tener activo ninguna herramienta que facilite la generación de código (Copilot, o otros asistentes de código).

**Entrega**

- La entrega se realizará a través del repositorio personal del alumno, en la carpeta `Evaluacion\3eval_examen`.
- También se entrega en un fichero comprimido, con el nombre `3eval_examen_{nombre_alumno}.zip` y subir a Moodle.

## Ejercicio 1: Diagrama de casos de uso  (2 puntos)

**Descripción del sistema**

Se desea desarrollar un sistema para gestionar un ecommerce muy sencillo, que permita a los usuarios realizar pedidos de productos. Un usuario puede visualizar el catálogo de productos, añadir y quitar productos de la cesta y realizar un pedido. Un administrador puede añadir y eliminar productos del catálogo, así como actualizar el inventario de los mismos.
Para poder realizar un pedido, y el usuario debe estar registrado en el sistema, sin embargo, puede visualizar el catálogo de productos sin estar registrado.

> ↘️ Nota aclaratoria: Realizar pedido implica que se genere un pedido con los productos de la cesta, y se actualice el stock de los productos.<br>
> ↘️ Diagrama orientación: Para una mejor visualización del diagrama, se recomienda utilizar una orientación vertical. `left to right direction`.

_Sugerencia: Puedes tratar al usuario registrado y no registrado como si fueran distintos._

### Instruccciones

1. Identifica los actores principales del sistema, indicando nombre y un pequeña descripción de su función dentro del sistema.
2. Identifica los casos de uso, indicando nombre y un pequeño resumen de la funcionalidad.
3. Crea un diagrama de casos de uso utilizando PlantUML, utilizando para ello un bloque de código en markdown.

> ↘️ Nota: No incluir en el diagrama los métodos get y set de los atributos, solo aquellos métodos que sean relevantes. Ej: `getProducto()`.


#### Entrega

Crea un fichero 01.ejercicio.md en la carpeta 3eval_examen.


## Ejercicio 2: Diagrama de clases (2,5 puntos)

Elabora el diagrama de clases siguiendo con el ejemplo anterior.

**Descripción del sistema:**

- Un producto tiene un id, codigo (unico), nombre, una descripción, un precio y un stock.
- La cesta de productos tiene un id, un total y una lista de items. Una cesta puede estar vacia.
  - Un item de la cesta tiene un id, un producto asociado, una cantidad y un total.
- Un usuario tiene un nombre, un email y una contraseña.
- Un cliente tiene un nombre, direccion, telefono y un email.
- Un Administrador tiene un nombre, direccion, telefono y un email.
- Un cliente es un usuario, y un administrador es un usuario.
- Un pedido tiene un id, una fecha, total, una lista de items y el cliente que lo ha realizado.
  - Un item del pedido tiene un id, un producto asociado, una cantidad, un precio y un total.


### Instrucciones

Elabora un diagrama de clases utilizando mermaid, indicando:

- Identifica las clases, atributos y métodos.
- Identifica las relaciones entre las clases.
- Indica la cardinalidad de las relaciones.

#### Entrega

Crea un fichero 02.ejercicio.md en la carpeta 3eval_examen.



## Ejercicio 3: Generar clases a código (2 puntos)

A partir del diagrama de clases anterior, genera las clases en Java que consideres necesarias para el sistema. 

### Instrucciones

Genera un proyecto en IntelliJ IDEA, con el nombre `EcommerceEEDD`, y crea las clases en el paquete raiz `com.iessdf.ecommerce.eedd`, y las clases dentro del paquete `model`.
Para ello, crea un proyecto basado en Maven desde la opción `File -> New -> Project... -> Maven -> Create from archetype -> maven-archetype-quickstart`, y pon el nombre del proyecto `EcommerceEEDD`.

> 💡 Nota: Recuerda crear un fichero .gitignore para ignorar los ficheros de configuración de IntelliJ IDEA.

#### Entrega

Crea un carpeta 03/ en la carpeta 3eval_examen, con el proyecto creado en IntelliJ IDEA.



## Ejercicio 4: Test unitarios (2,5 puntos)

A partir de las clases anteriores, crea los test unitarios que comprueben la clase cesta.

### Instrucciones

Crea una clase de test `CestaTest`, y crea los test unitarios siguientes para la clase `Cesta`.

- `should_BeEmptyWhenCreated`: Comprueba que la cesta está vacía cuando se crea.
- `should_AddProductToBasket`: Comprueba que se añade un producto a la cesta, así como la cantidad y el total son correctos.
- `should_RemoveProductFromBasket`: Comprueba que se elimina un producto de la cesta, así como la cantidad y el total son correctos.
- `should_ClearBasket`: Comprueba que se vacía la cesta, y la cantidad y el total son ceros.


Realiza el test utilizando los asserts de JUnit5 más adecuados según el caso y lo que se desea comprobar.

### Entrega

En la misma carpeta 03/ del ejercicio anterior, crea los test unitarios en la carpeta `test` del proyecto.



## Ejercicio 5: Cobertura de código  (1 punto)

Basado en el ejercicio anterior, genera un informe de cobertura de código desde IntelliJ IDEA, y comprueba que la cobertura de **líneas** para la clase `Cesta` es del 100%.

Si no fuera el 100%, agregar los test que sean necesarios para que la cobertura de **líneas** sea del 100%.

### Entrega

Crea un fichero 05.ejercicio.md en la carpeta 3eval_examen, incluyendo una captura de pantalla de la cobertura de código.
