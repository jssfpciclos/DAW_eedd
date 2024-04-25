# UNIT TESTING JAVA (JUNIT 5)

## Introducción

Las pruebas unitarias son una técnica de programación que consiste en realizar pruebas automatizadas para verificar el correcto funcionamiento de una unidad de código. Una unidad de código puede ser un método, una clase, un paquete, un componente, etc. Las pruebas unitarias se realizan de forma aislada, es decir, se prueban las unidades de código de forma independiente, sin depender de otras unidades de código o componentes.

### Testing tradicional

El testing tradicional se realiza de forma manual:

- Directamente desde el código fuente.
- Via app móvil o web.
- Con herramientas como POSTSMAN para API Rest.

En general podemos decir que:

- Requieren mucho tiempo y es lento. A medida que la aplicación crece, el tiempo de pruebas también crece.
- No nos reporta si falla, dónde y por qué
- Habrá que repetir las pruebas cada vez que se haga un cambio en el código.
- No se pueden automatizar.
- Habrá casos de uso que no se prueben, o que se prueben unas veces y otras no.


### Testing automatizado

Las características del testing automatizado son:

- Automático y rápido.
- Nos permite disponer de un conjunto de pruebas definido.
- Nos ofrece un reporte de las pruebas.
  - Si falla, dónde y pro qué.
- Nos garantiza su funcionamiento tras cambios.


## Tipos de Test

- Pruebas unitarias
  - Menor coste
  - Mayor número de test.
  - Máximo aislamiento.
- Integración
- Aceptación
  - Más coste.
    - Menor número de test.
    - Máxima integración.


<img src="./img/doc_utj_01.png" width="80%">


### Requisitos para hacer Testing

- Comprender el funcionamiento de nuestra aplicación
- Conocer cuáles son nuestras clases.
- Reglas de negocio o casos de uso.

### Pruebas unitarias

- Métodos que permite verificar una parte del código.
- Comprueban que, para unos datos de entrada, devuelve el resultado esperado.
- Permiten la veridicación de las reglas de negocio de forma aislada.


**¿Qué es una prueba?**

Las pruebas unitarias casi siempre se centran en pruebas de "Caja Negra", donde para unos datos de entrada se esperan unos datos de salida.



### JUnit

Realizar las pruebas de forma manual puede ser tedioso y propenso a errores. Por ello, existen frameworks que facilitan la creación y ejecución de pruebas unitarias. Uno de los frameworks más populares para realizar pruebas unitarias en Java es JUnit.

Aparte de JUnit, existen otros frameworks de pruebas unitarias en Java, como TestNG, Mockito, PowerMock, etc, pero por su popularidad y simplicidad, JUnit es el más utilizado.

JUnit es un framework de pruebas unitarias para el lenguaje de programación Java

Características de JUnit:

- Permite escribir y ejecutar pruebas unitarias de forma sencilla.
- Proporciona anotaciones para definir métodos de prueba.
- Proporciona métodos de aserción para verificar los resultados de las pruebas.
- Proporciona herramientas para la ejecución de pruebas y la generación de informes.
- Proporciona herramientas para la organización de pruebas en suites de pruebas.
- Las pruebas son repetibles y se pueden ejecutar de forma automática.


### Instalación de JUnit

Para utilizar JUnit en un proyecto Java, es necesario añadir la librería de JUnit al proyecto, y esto se puede realizar de varias formas:

- Manualmente añadiendo el archivo JAR de JUnit al proyecto.
- Utilizando una herramienta de gestión de dependencias como Maven o Gradle.


#### JUNIT 4 vs JUNIT 5

JUnit 4 es la versión anterior de JUnit, y JUnit 5 es la versión más reciente de JUnit. JUnit 5 es una versión completamente nueva de JUnit que se lanzó en septiembre de 2017. JUnit 5 es una reescritura completa de JUnit 4 y ofrece muchas nuevas características y mejoras sobre JUnit 4.

A continuación, se muestra una tabla comparativa de las características de JUnit 4 y JUnit 5:

| Característica | JUnit 4 | JUnit 5 |
| --- | --- | --- |
| Arquitectura | Basada en JUnit 3 | Basada en JUnit Platform |
| Anotaciones | @Test, @Before, @After, @BeforeClass, @AfterClass | @Test, @BeforeEach, @AfterEach, @BeforeAll, @AfterAll |
| Extensiones | No | Sí |
| Anotaciones de extensión | No | @ExtendWith |
| Anotaciones de repetición | No | @RepeatedTest |
| Anotaciones de parámetros | No | @ParameterizedTest |
| Anotaciones de excepción | @Test(expected = Exception.class) | @Test(expected = Exception.class) |
| Anotaciones de tiempo de espera | @Test(timeout = 1000) | @Test(timeout = 1000) |
| Anotaciones de deshabilitación | @Ignore | @Disabled |
| Anotaciones de etiquetas | No | @Tag |
| Anotaciones de anidamiento | No | @Nested |
| Anotaciones de prueba condicional | No | @EnabledOnOs, @EnabledOnJre, @EnabledIf, @EnabledIfSystemProperty, @EnabledIfEnvironmentVariable |
| Anotaciones de inyección de dependencias | No | @RegisterExtension |
| Anotaciones de configuración de extensión | No | @RegisterExtension |
| Anotaciones de manejo de excepciones | No | @ExceptionHandler |
| Anotaciones de tiempo de vida de la extensión | No | @ExtendWith |
| Anotaciones de prueba de interfaz funcional | No | @Testable |


#### JUnit 5

Anotaciones más importantes de JUnit 5:

- @Test: Indica que el método es un método de prueba.
- @BeforeEach: Indica que el método se ejecuta antes de cada método de prueba.
- @AfterEach: Indica que el método se ejecuta después de cada método de prueba.
- @BeforeAll: Indica que el método se ejecuta antes de todos los métodos de prueba.
- @AfterAll: Indica que el método se ejecuta después de todos los métodos de prueba.

Otras anotaciones de JUnit 5:

- @DisplayName: Permite definir un nombre personalizado para el método de prueba.
- @Disabled: Indica que el método de prueba está deshabilitado.
- @Ignore: Indica que el método de prueba está deshabilitado.
- @Order: Indica el orden de ejecución de los métodos de prueba.
- @EnabledOnOs: Indica que el método de prueba se ejecuta en un sistema operativo específico.
- @EnabledOnJre: Indica que el método de prueba se ejecuta en una versión específica de la JVM.
- @RepeatedTest: Indica que el método de prueba se repite un número específico de veces.
- @ParameterizedTest: Indica que el método de prueba se ejecuta con diferentes parámetros.
- @Tag: Permite etiquetar los métodos de prueba. Se pueden agrupar los métodos de prueba por etiquetas y ejecutar solo los métodos de prueba que tengan una etiqueta específica.
- @Nested: Permite anidar clases de prueba. Se pueden anidar clases de prueba para organizar las pruebas de forma jerárquica. Cada clase de prueba anidada se ejecuta de forma independiente.


### Primeras pruebas unitarias con JUnit

- Cada prueba se realiza en un método anotado con @Test.
- Si falla una condición (assertion) en un test, éste falla.
- Las instancias a nivel de clase son diferentes para cada test.
- **El orden de las pruebas no importa**


#### Asserts

Los asserts son métodos que permiten verificar si una condición es verdadera o falsa. Si la condición es verdadera, la prueba continúa. Si la condición es falsa, la prueba falla.

Algunos métodos de aserción más comunes en JUnit son:

- assertTrue/assertFalse: Verifica si una condición es verdadera/falsa.
- assertEquals: Verifica si dos valores son iguales.
- assertNotEquals: Verifica si dos valores no son iguales.
- assertNull/assertNotNull: Verifica si un valor es nulo/no nulo.
- assertSame/assertNotSame: Verifica si dos referencias apuntan al mismo objeto/no al mismo objeto.
- assertThat: Verifica si un valor cumple una condición.
- assertThrows: Verifica si una excepción es lanzada.
- assertTimeout: Verifica si una operación se ejecuta en un tiempo determinado.
- assertAll: Verifica varias condiciones a la vez.

También podemos hacer que una prueba falle de forma controlada con el método `fail()`.

#### Ejemplo

En el siguiente ejemplo se quiere comprobar que el método `sendProduct`acutaliza el stock de la tienda.

  
```java
@Test
void itShoutldRemoveFromStore() {
  Product product = new Product("Coca-Cola", 10);
  Store store = new Store("Store", List.of(product, product, product));

  storeService.sendProduct(product);
  assertNotNull(store.getProducts());
  assertEquals(2, store.getProducts().size());
}
```

Los métodos `assert`pueden reportar mensajes de fallos personalizados:

- Se pasan como último parámetro del método como un `String` o como una expresión lambda.

Ejemplos:

- assertEquals(2, store.getProducts().size(), "El tamaño de la lista de productos no es correcto");
- assertEquals(2, calculadora.suma(1,1), () -> "La suma debería ser 2");


### Ciclo de vida de una prueba

El ciclo de vida de una prueba en JUnit 5 es el siguiente:

1. **@BeforeAll**: Se ejecuta una vez antes de todos los métodos de prueba.
2. **@BeforeEach**: Se ejecuta antes de cada método de prueba.
3. **@Test**: Método de prueba.
4. **@AfterEach**: Se ejecuta después de cada método de prueba.
5. **@AfterAll**: Se ejecuta una vez después de todos los métodos de prueba.

El orden en el que se ejecutan los test es aleatorio, por lo que no se puede garantizar el orden de ejecución de los test.

Pero si se necesita garantizar el orden de ejecución de los test, se puede utilizar la anotación `@Order`.

```java
@Test
@Order(1)
void test1() {
  // Test 1
}

@Test
@Order(2)
void test2() {
  // Test 2
}
```

En este caso, el test1 se ejecutará antes que el test2. 

> 💡 Si algún test no tiene la anotación `@Order`, se ejecutará después de los test que sí la tengan.

#### Setup y TearDown

En JUnit 5, se pueden utilizar los métodos `@BeforeEach` y `@AfterEach` para realizar la configuración y limpieza de los recursos necesarios para la ejecución de las pruebas.

```java
@BeforeEach
void setUp() {
  // Configuración de recursos
}

@AfterEach
void tearDown() {
  // Limpieza de recursos
}
```

#### Deshabilitar pruebas

Los test pueden ser deshabilitados con la anotación `@Disabled` o `@Ignore`. (JUnit 5 recomienda indicar un motivo)

```java
public class DisabledTest {

    @Test
    //@Disabled("Until bug #12300 fix")
    void test1() {
        System.out.println("test1");
        assertTrue(true);
    }

    @Test
    @Disabled("Until feature #11900")
    void test2() {
        System.out.println("test2");
        assertTrue(true);
    }

}
```

#### Test condicionales

En JUnit 5, las pruebas unitarias se puede ejecutar conforma a diferentes condiciones.

**@EnabledOnOs**

- Permite habilitar/deshabilitar una prueba en función del sistema operativo. @EnabledOnOs({OS.WINDOWS, OS.LINUX}), @DisabledOnOs({OS.MAC})
- Permite habilitar/deshabilitar una prueba en función de la versión de Java. @EnabledOnJre(JRE.JAVA_8), @DisabledOnJre(JRE.JAVA_11)
- o incluso por rangos:
  - @EnabledForJreRange(min = JRE.JAVA_8, max = JRE.JAVA_11)
  - @DisabledForJreRange(min = JRE.JAVA_8, max = JRE.JAVA_11)

**@EnabledIfSystemProperty**

- Permite habilitar/deshabilitar una prueba en función de una propiedad del sistema. @EnabledIfSystemProperty(named = "os.arch", matches = ".*64.*")
- Se puede usar con: System.getProperty("os.arch")
- Si no existe la propiedad, no se ejecuta.
  - @EnabledIfSystemProperty(named = "os.arch", matches = ".*64.*", disabledReason = "Solo para 64 bits")

**@EnabledIfEnvironmentVariable**

- Permite habilitar/deshabilitar una prueba en función de una variable de entorno. @EnabledIfEnvironmentVariable(named = "ENV", matches = ".*dev.*")
  - Número de núcleos, memoria, etc.
  - Entorno local, DEV, QA, PROD, etc.

**@EnabledIf / @DisableIf**

- Permite habilitar/deshabilitar una prueba en función de una expresión booleana. - El método encargado de ello estará especificado en el test mediante la anotación @EnabledIf o @DisabledIf.
- Será estático si se usa a nivel de clase.


Ejemplos de todo esto:

```java
    @EnabledOnJre(JRE.JAVA_8)
    @Test
    void test1() {
        System.out.println("test1 java 8");
    }
    @EnabledOnJre(JRE.JAVA_16)
    @Test
    void test2() {
        System.out.println("test2 java 16");
    }

    @EnabledForJreRange(min = JRE.JAVA_8, max=JRE.JAVA_11)
    @Test
    void test3() {
        System.out.println("test3 range");
    }


    @Test
    @EnabledOnOs(OS.LINUX)
    void test4() {
        System.out.println("test4 linux");
    }
```	

#### Escribir propias condiciones

Dentro de los test-condicionales podemos tener un tipo de test, que se ejecuta en función de una condición que nosotros mismos definimos.

- Permiten habilitar parte de un test en función de si se cumple una condición.
  - assumeTrue(boolean condition)
  - assumeFalse(boolean condition)
- Si la condición no se cumple, el código a partir de ahí se deshabilita, evitando el fallo, es decir, solo queremos probar si se cumple una condición, sino se cumple, no quremos que falle el test.

```java
    @Test
    void test5() {
        assumeTrue("DEV".equals(System.getenv("ENV")));
        System.out.println("test5");
        // imprime si la variable de entorno ENV es DEV, en caso contrario no se ejecuta y el test queda deshabilitado.
    }
```	

otros ejemplos:

```java
    @Test
    void name() {
        String jdk = System.getenv("JAVA_HOME");
        assumeTrue(jdk.contains("jdk-11"));
        assumeFalse(jdk.contains("jdk-16.0.2"));

        System.out.println("El test continua");
    }

    @Test
    void name2() {
        String jdk = System.getenv("JAVA_HOME");

        assumingThat(jdk.contains("jdk-11"),
                () -> {


                }
        );

    }
```	

### Test anidados

En JUnit 5, se pueden anidar clases de prueba para organizar las pruebas de forma jerárquica, por diferentes criterios: funcionalidad, condicionalidad, ...

- Se trata de inner classes en Java.
- Se anotan las clases con @Nested.
- @BeforeAll y @AfterAll no se pueden usar en clases anidadas.
- Se puede incluir una descripción en dichas clases y los métodos que contienen con @DisplayName.
- Los test aparecerán en el `reporting` agrupados por clases.
- Si falla un test de una clase anidada, falla la clase anidada y la clase padre.

```java	
@DisplayName("Tests para servicio SmartPhone")
public class ANestedTest {

    @Test
    @DisplayName("Test1")
    void test1() {
        System.out.println("test1");
        assertTrue(true);
    }

    @Nested
    @DisplayName("operaciones recuperar datos")
    class Grupo1 {
        @Test
        @DisplayName("Find all()")
        void test2() {
            System.out.println("test2");
            assertTrue(true);
        }

        @Test
        @DisplayName("Find one()")
        void test3() {
            System.out.println("test3");
            assertTrue(true);
        }

        @Test
        @DisplayName("Find by CPU cores()")
        void test4() {
            System.out.println("test4");
            assertTrue(true);
        }

    }

    @Nested
    @DisplayName("operaciones insercion nuevos datos")
    class Grupo2 {

        @Test
        @DisplayName("Insert one")
        void test5() {
            System.out.println("test5");
            assertTrue(true);
        }

        @Test
        @DisplayName("Insert in batch")
        void test6() {
            System.out.println("test5");
            assertTrue(true);
        }
    }
}

```

### Test repetidos

En JUnit 5, se pueden repetir las pruebas un número específico de veces.

- Se anotan los métodos con @RepeatedTest.
  - Útil para pruebas de rendimiento.
  - Útil en métodos que presentan comportamiento aleatorio.

- En el reporting se mostrará el número de veces que se ha repetido el test.
- Se puede combiar el nombre con @DisplayName.
  - @DisplayName: será el título principal.
  - @RepeatedTest: Nombre de cada repetición.

```java
  public class BRepeatedTest {

    @Test
    void test1() {
        System.out.println("Prueba concepto test1");
    }

    @RepeatedTest(value = 3)
    void test2() {
        System.out.println("Prueba concepto test2");
    }

    @DisplayName("Caso de test 3")
    @RepeatedTest(value = 3, name = RepeatedTest.SHORT_DISPLAY_NAME)
    void test3() {
        System.out.println("Prueba concepto test3");
    }

    @DisplayName("Caso de test 4")
    @RepeatedTest(value = 3, name = RepeatedTest.LONG_DISPLAY_NAME)
    void test4() {
        System.out.println("Prueba concepto test3");
    }

    @DisplayName("Caso de test 4")
    @RepeatedTest(value = 3, name = "{displayName} - {currentRepetition} / {totalRepetitions}")
    void test5() {
        System.out.println("Prueba concepto test3");
    }
}
```

