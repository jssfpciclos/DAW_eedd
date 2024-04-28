# Boletín 3.3. Unit Testing con Convertura de código

### Entrega

- Todos los ejercicios se entregan dentro de un proyecto de IntelliJ.
- El proyecto debe ser gestionado por Maven, y creado o bien a través de IntelliJ o bien a través de la línea de comandos.
- El proyecto debe contener un .gitignore adecuado (ignorando target, .idea, etc.) para no subir ficheros innecesarios al repositorio.
- El proyecto debe subirse en la ruta `UT3/TE/3.3/` de vuestro repositorio.

Dentro de la ruta `UT3/TE/3.3/` incluye un fichero `readme.md` donde se refleje la información solicitada en el ejercicio.


### Recursos

- [Intellj IDEA - Code Coverage](https://www.jetbrains.com/help/idea/code-coverage.html)
- [Covertura de Código](../../docs/doc_unit-testing-coverage.md)
- [¿Qué es la cobertura de código](https://www.atlassian.com/es/continuous-delivery/software-testing/code-coverage)

### Proyecto recurso

En base al proyecto del ejercicio anterior, copiar el proyecto y cambiar los paquetes de las clases tanto de código como de test a `eedd.ut3.eje33`.

Para refactorizar el código, usa la opción usar la opción de IntelliJ `Refactor -> Move` y seleccionar el nuevo paquete.


### 3.3.0 Ejecutar los test de cobertura de código inicial

Lo primero es ejecutar los test de cobertura de código para ver el porcentaje de cobertura que tenemos en el proyecto, y así poder ir mejorando el código y los test para aumentar la cobertura.

Ejecutar los test de cobertura de código y adjuntar la captura de pantalla donde se visualice el porcentaje de cobertura obtenido.


> 🧲  Adjuntar imagen con la covertura de código inicial



### Ejercicio 3.2.1. Métricas a conseguir

Se debe conseguir una cobertura de código mínima para el proyecto del 80%.

En la siguiente tabla se muestra la cobertura de código actual y la cobertura de código que se debe conseguir para cada clase del proyecto.

| Clases | Cobertura clase | Método | Linea | Rama |
|--------|-----------------|--------|-------|------|
| Fibonacci | 100% | 100% | 100% | 100% |
| Quadrilateral | 100% | 100% | 100% | 75% |
| Line | 100% | 100% | 100% | 100% |
| Point | 100% | 100% | 100% | 100% |
| Vector2D | 100% | 100% | 100% | 100% |
| Money | 100% | 100% | 80% | 0% |
| Currency | 100% | 100% | 100% | 100% |
| Account | 80% | 100% | 80% | 80% |
| Bank | 100% | 80% | 80% | 80% |


*Se pide:*

- Agregar los test necesarios para conseguir la cobertura de código mínima exigida en la tabla anterior.


> 🧲  Adjuntar imagen con la covertura de código inicial



> 🧲  Adjuntar un GIF donde se visualize la realización de los `test con covertura`con la opción *Run 'Test in Java' con Coverage*.




### Ejercicio 3.2.2. Covertura de ramas

En base a los ejercicios [EC 3.1 Casos de prueba](../../EC/EC3.1_ejercicio.md).

Se requiere realizar la covertura de ramas para los siguientes funciones:


En base a la clase siguiente:

```java
package eedd.ut3.ejerc32.C;

public class CasosPrueba {

    public static int Metodo2(int x, int y) {
        if (x<0 || y<0) {
            System.out.println("Error: los valores no pueden ser negativos");
            return -1;
        }

        if (x==1 && y==1) {
            return 1;
        }

        while (x!=y) {
            if (x>y) {
                x=x-y;
            } else {
                y=y-x;
            }
        }

        return x;
    }

}
```

*Se pide:*

- Crear una clase de test `CasosPruebaTest`.
- Crear un método de test para cada uno de los caminos de la función `Metodo2`, calculados en la realización del ejercicio EC 3.


> 🧲  Adjuntar imagen con la covertura de la clase Casos de Prueba, donde la `covertura de ramas` debe ser el 100%.

