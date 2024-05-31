# Simulacro Examen 3ª Evaluación Entornos de Desarrollo

### Sistema de Biblioteca Digital

Se necesita desarrollar un sistema de software para gestionar una biblioteca digital. El sistema debe permitir a los usuarios realizar las siguientes acciones:

- Registrarse en el sistema.
- Buscar libros por título, autor o género.
- Pedir prestado un libro.
- Devolver un libro.
- Consultar la disponibilidad de un libro.
- Ver el historial de préstamos.

Además, los administradores del sistema deben poder:

- Añadir nuevos libros a la colección.
- Eliminar libros de la colección.
- Ver el historial de préstamos de cualquier usuario.


### Ejercicio 1: Diagrama de casos de uso

**Define los casos de uso del sistema**

1. Identifica los actores principales del sistema, indicando nombre y un pequeña descripción de su función dentro del sistema.

---

2. Identifica los casos de uso, indicando nombre y un pequeño resumen de la funcionalidad.

---

3. Crea un diagrama de casos de uso utilizando PlantUML, utilizando para ello un bloque de código en markdown.

---


### Ejercicio 2: Diagrama de clases

Basado en los casos de uso definidos, elabora un diagrama de clases, incorporando cardinalidad y relaciones con direccionalidad.

```plantuml	
```	



### Ejercicio 3: Generar clases a código

En base al diagrama de clases anterior, genera las clases en Java incluidas en el mismo, incluyendo atributos y métodos, así como las relaciones entre las clases.

> 💡Nota: Para este caso los atributos se permite que sean públicos.

Genera un proyecto en IntelliJ IDEA, con el nombre `BibliotecaDigitalEEDD`, y crea las clases en el paquete raíz `com.iessdf.eedd.digitalbooks`, y las clases dentro del paquete `model`. 

Para ello, crea un proyecto basado en Maven desde la opción File -> New -> Project... -> Maven -> Create from archetype -> maven-archetype-quickstart, y pon el nombre del proyecto BibliotecaDigitalEEDD.

 > 💡Nota: Recuerda crear un fichero .gitignore para ignorar los ficheros de configuración de IntelliJ IDEA.

```java
```


### Ejercicio 4: Generar Test Unitarios

Genera los test siguientes para clase Biblioteca, encargada de la gestión de realizar préstamos y devoluciones de libros.

1. Crea una clase BibliotecaTest en el paquete `com.iessdf.eedd.digitalbooks.model` dentro de la carpeta `test`.
2. Realiza los siguientes test unitarios:
   - should_RegisterUser: Comprueba que se registra un usuario correctamente.
   - should_FindBookByTitle: Comprueba que se encuentra un libro por título.
   - should_SucessfulBorrowBook: Comprueba que se realiza un préstamo de un libro.
   - should_SucessfulReturnBook: Comprueba que se devuelve un libro.





### Ejercicio 5: Cobertura de código

Ejecuta la cobertura de código de IntelljIDEA a tu proyecto, y comprueba que los test unitarios cubren al menos un 80% del código de la clase Biblioteca.

Si no fuera el caso, modifica los test unitarios para que cubran al menos el 80% del código.

> Nota: Este ejercicio no será tomado en consideración si no existen al menos 4 métodos en la clase Biblioteca, referentes a los casos de uso.


