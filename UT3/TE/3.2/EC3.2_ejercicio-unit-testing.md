# Boletín 3.2. Unit Testing con JUnit 5

### Entrega

- Todos los ejercicios se entregan dentro de un proyecto de IntelliJ.
- El proyecto debe ser gestionado por Maven, y creado o bien a través de IntelliJ o bien a través de la línea de comandos.
- El proyecto debe contener un .gitignore adecuado (ignorando target, .idea, etc.) para no subir ficheros innecesarios al repositorio.
- El proyecto debe subirse en la ruta `UT3/EC/3.2/` de vuestro repositorio.


Dentro de la ruta `UT3/TE/3.2/` incluye un fichero `readme.md` donde se refleje la información solicitada en el ejercicio.

### Recursos

- [JUnit 5 User Guide](https://junit.org/junit5/docs/current/user-guide/)
- [Curso de JUnit 5](https://www.youtube.com/playlist?list=PLTd5ehIj0goPcVH3xhSudzyazW8CtMvsq)
- [Maven in 5 Minutes](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html)


### Proyecto recurso

Todas las clases necesarias para realizar los ejercicios se encuentran en el siguiente proyecto:

- [Proyecto recurso ejercicio](./res/projecto_ejercio_3.2.zip)



Se dispone de las siguientes clases dentro del paquete `eedd.ut3.eje32`:

### Ejercicio 3.2.1. Fibonacci

```java	
package eedd.ut3.eje32;


/// Clase que implementa el cálculo de la serie de Fibonacci
public class Fibonacci {
	public int fib(int n) {
		if(n == 0) {
			return 0;
		}
		if(n == 1 || n == 2) {
			return 1;
		}
		return fib(n-2) + fib(n-1);
	}
}
```

Se pide:

- Crear una clase FibonacciTest
- Crear un método setup que se llame una vez por cada test, y que instancia la clase `Fibonacci`
- Crear un método tearDown que se llame una vez por cada test, y que ponga a null la instancia de la clase `Fibonacci`
- Crear un método testFibonacciTo5 que compruebe que el método `fib` de la clase `Fibonacci` devuelve el valor esperado para los siguientes valores de n: 0, 1, 2, 3, 4, 5
- Crear un método testFibonacciToOthers que compruebe que el método `fib` de la clase `Fibonacci` devuelve el valor esperado para los siguientes valores de n: 8, 10, 13, 15, 20
- Incluir un mensaje en cada `assert` para indicar qué valor se esperaba y qué valor se ha obtenido. Por ejemplo: `assertEquals(5, resultado, "Se esperaba 5");`

> 🧲  Adjuntar un GIF donde se visualize que el resultado de pasar los test para la clases `FinonacciTest`.



### Ejercicio 3.2.2. Cuadrilátero

Un cuadrilátero es una figura geométrica que tiene cuatro lados. 

En la clase `Quadrilateral` se ha implementado un cuadrilátero con los siguientes métodos:

- isRectangle: Devuelve true si el cuadrilátero es un rectángulo, y false en caso contrario.
- isSquare: Devuelve true si el cuadrilátero es un cuadrado, y false en caso contrario.

También usa las clases `Point`, `Line` y `Vector2D` que se proporcionan que también se proporcionan.

```java
package eedd.ut3.eje32;

public class Line {
	private Point p1, p2;
	
	Line(Point p1, Point p2) {
		this.p1 = p1;
		this.p2 = p2;
	}
	
	public Vector2D getVector() {
		return new Vector2D(p1, p2);
	}
	
	public Double getLength() {
		return Math.sqrt(Math.pow((p2.x - p1.x), 2) + Math.pow((p2.y - p1.y), 2));
	}
	
	public Boolean isSameLengthAs(Line l) {
		return (Math.abs(getLength() - l.getLength()) < 0.00001);
	}
}

public class Point {
	public Integer x, y;
	
	Point(Integer x, Integer y) {
		this.x = x;
		this.y = y;
	}
	
	public Point add(Point p) {
		return new Point(x + p.x, y + p.y);
	}
	
	public Point sub(Point p) {
		return new Point(x - p.x, y - p.y);
	}
}

public class Vector2D {
	public Integer x, y;
	
	Vector2D(Integer x, Integer y) {
		this.x = x;
		this.y = y;
	}
	
	/* Construct Vector2D from two points */
	Vector2D(Point p1, Point p2) {
		this.x = p2.x - p1.x;
		this.y = p2.y - p1.y;
	}
	
	public int dotProduct(Vector2D v) {
		return (x * v.x) + (y * v.y);
	}
	
	public boolean isOrthogonalTo(Vector2D v) {
		return (dotProduct(v) == 0);
	}
}
```

La clase `Quadrilateral` es la siguiente:

```java
public class Quadrilateral {
	private Point p1, p2, p3, p4;
	private Line l1, l2, l3, l4;

	Quadrilateral(Point p1, Point p2, Point p3, Point p4) {
		this.p1 = p1;
		this.p2 = p2;
		this.p3 = p3;
		this.p4 = p4;
		this.l1 = new Line(p1, p2);
		this.l2 = new Line(p2, p3);
		this.l3 = new Line(p3, p4);
		this.l4 = new Line(p4, p1);
	}

	public Boolean isRectangle() {
		Vector2D v1 = l1.getVector();
		Vector2D v2 = l2.getVector();
		Vector2D v3 = l3.getVector();
		Vector2D v4 = l4.getVector();

		return (v1.isOrthogonalTo(v2) &&
				v2.isOrthogonalTo(v3) &&
				v3.isOrthogonalTo(v4) &&
				v4.isOrthogonalTo(v1));
	}

	public Boolean isSquare() {
		return (isRectangle() &&
				l1.isSameLengthAs(l2));
	}

}
```

Para encontar si el poligono es un rectángulo, se usa el método `isRectangle`, y para comprobar si es un cuadrado, se usa el método `isSquare`.


Para facilitar el testeo de la clase `Quadrilateral`, se proporciona la clase `QuadrilateralTest` con el siguiente código:

```java
package eedd.ut3.eje32;

    //añadir imports necesarios
    
    @Before
    public void setUp() throws Exception {
   
        square1 = new Quadrilateral(new Point(2, 3), new Point(4, 7), new Point(8, 5), new Point(6, 1));
        square2 = new Quadrilateral(new Point(-1, -1), new Point(-1, 1), new Point(1, 1), new Point(1, -1));
        rectangle1 = new Quadrilateral(new Point(4, 2), new Point(3, 4), new Point(9, 7), new Point(10, 5));
        rectangle2 = new Quadrilateral(new Point(-2, -1), new Point(-2, 1), new Point(2, 1), new Point(2, -1));
        quad = new Quadrilateral(new Point(-2, -2), new Point(-1, 1), new Point(1, 1), new Point(1, -1));
    }

```

**Se pide:**

Completar la clase `QuadrilateralTest` con los siguientes métodos:

- `testIsRectangle` 

    Que compruebe que el método `isRectangle` de la clase `Quadrilateral` devuelve el valor esperado para los cuadriláteros `square1`, `square2`, `rectangle1`, `rectangle2` y `quad`.
   
- `testIsSquare` 

    que compruebe que el método `isSquare` de la clase `Quadrilateral` devuelve el valor esperado para los cuadriláteros `square1`, `square2`, `rectangle1`, `rectangle2` y `quad`.


> 💡 Incluir un mensaje en cada `assert` para indicar qué valor se esperaba y qué valor se ha obtenido. Por ejemplo: `assertEquals(5, resultado, "Se esperaba 5");`



> 🧲  Adjuntar un GIF donde se visualize que el resultado de pasar los test para la clases `QuadrilateralTest`.



### Ejercicio 3.2.3.  Dinero y Moneda

Dentro del proyecto adjunto a este ejercicio se proporcionan las siguientes clases:

- Money
- Currency


En base a ellas, también se incluyen dentro del proyecto las siguientes clases de Test:

- MoneyTest
- CurrencyTest


*Se pide:*

- Rellenar los métodos de test de las clases `MoneyTest` y `CurrencyTest` con los `asserts` correspondientes según se indica en los comentario de cada método de @Test.


> 🧲  Adjuntar la clase `MoneyTest` completa una vez rellenos los métodos.


> 🧲  Adjuntar un GIF donde se visualize que el resultado de pasar los test para la clases `MoneyTest`.


> 🧲  Adjuntar la clase `CurrencyTest` completa una vez rellenos los métodos.


> 🧲  Adjuntar un GIF donde se visualize que el resultado de pasar los test para la clases `CurrencyTest`.



### Ejercicio 3.2.4.  Bancos y Cuentas

Dentro del proyecto adjunto a este ejercicio se proporcionan las siguientes clases:

- Bank
- Account


En base a ellas, también se incluyen dentro del proyecto las siguientes clases de Test:

- AccountTest
- BankTest

La clase `AccountTest` ya tiene los métodos de test creados y rellenos con los `asserts` correspondientes, pero al pasar los test fallan.


*Se pide:*

- Modificar el código de la clase `Account y Bank' para que los test de la clase `AccountTest` pasen correctamente.


> 🧲  Adjuntar la clase `Account` completa una solucionado los problemas.


> 🧲  Adjuntar la clase `Bank` completa una solucionado los problemas.



> 🧲  Adjuntar un GIF donde se visualize que el resultado de pasar los test para la clases `AccountTest`.



- Rellenar los métodos de test de las clases `BankTest` con los `asserts` y realiza un test que compruebe lo que se pide, según el nombre del método.


> 🧲  Adjuntar la clase `BankTest` completa una vez rellenos los métodos.


> 🧲  Adjuntar un GIF donde se visualize que el resultado de pasar los test para la clases `BankTest`.