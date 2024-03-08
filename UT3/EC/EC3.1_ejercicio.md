# Ejercicios Casos de prueba

### Entrega

Realiza el grafo en papel, y anota los números de cada parte sobre el papel, así como la tabla de pruebas y los caminios.
Después escanea y pasa a PDF para entregar en Moodle.

## Ejercicio 1

Dado el siguiente fragmento de programa en Java:

```java
static int visualizarMedia(int a, int b) {
    float resultado = 0;
    if (x<0 || y<0)) {
        System.out.println("Error: los valores no pueden ser negativos");
    } else {
        resultado = (x+y)/2;
        System.out.println("La media es: " + resultado);
    }
}
```

**Se pide:**

1. Obtener el grafo de flujo asociado al fragmento de programa.

2. Calcular la complejidad ciclomática del grafo.

3. En base a la complejidad calculada, indica la tabla de pruebas necesaria para alcanzar la cobertura de caminos.

- Indica los caminos.

- Indica las pruebas necesarias.

## Ejercicio 2

A partir del siguiente algoritmo en pseudocódigo, se pide:

```java
Leer x,y
Si x < 0 o y < 0 entonces
    Escribir "Error: los valores no pueden ser negativos"
    retorna -1
FinSi

Si x ==1 y y == 1 entonces
    retorna 1
FinSi

Mientras x != y hacer
    Si x > y entonces
        x = x - y
    SiNo
        y = y - x
    FinSi
FinMientras

retorna x
```

- Obtener el grafo de flujo asociado al fragmento de programa.
- Calcular la complejidad ciclomática del grafo.
- En base a la complejidad calculada, indica la tabla de pruebas necesaria para alcanzar la cobertura de caminos.
- Indica los caminos.

Fragmento de Java, algoritmo (método completo):

## Ejercicio 3

A partir del siguiente algoritmo en pseudocódigo, se pide:

```java
Leer cantidad
costo1 = cantidad * 125

numcaja = rendondea(0.5 + cant/4)
flete = numcaj*50

Si cant > 1000 entonces
    descuento = costo1 * 0.10
SiNo
    Si cant > 100 entonces
        descuento = costo1 * 0.05
    SiNo
        descuento = 0
    FinSi
FinSi

costoTotal = costo1 + flete - descuento

Esribir "El costo total es: " + costoTotal
```

- Obtener el grafo de flujo asociado al fragmento de programa.
- Calcular la complejidad ciclomática del grafo.
- En base a la complejidad calculada, indica la tabla de pruebas necesaria para alcanzar la cobertura de caminos.

### Ejericio 4

A partir del siguiente algoritmo en pseudocódigo, se pide:

```java
// Generar un algoritmo con varias condiciones y más de un bucle
public void algoritmo(int x, int y) {
    int resultado = 0;
    if (x < 0 || y < 0) {
        System.out.println("Error: los valores no pueden ser negativos");
    } else {
        resultado = (x + y) / 2;
        System.out.println("La media es: " + resultado);
    }
    for (int i = 0; i < x; i++) {
        if (i % 2 == 0) {
            System.out.println("El número " + i + " es par");
        } else {
            System.out.println("El número " + i + " es impar");
        }
    }
}

```
