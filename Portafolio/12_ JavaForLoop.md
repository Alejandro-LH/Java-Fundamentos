# Java For Loop

Cuando sabes exactamente cuántas veces quieres repetir un bloque de código, usa el bucle  **`for`**  en lugar de un bucle  **`while`**.

_**Sintaxis:**_

```java
for (sentencia1; sentencia2; sentencia3) {
    // bloque de código que se ejecutará
}

```

-   **Sentencia 1:**  se ejecuta (una vez) antes de ejecutar el bloque de código.
-   **Sentencia 2:**  define la condición para ejecutar el bloque de código.
-   **Sentencia 3:**  se ejecuta (cada vez) después de que el bloque de código ha sido ejecutado.

***Por ejemplo:***

```java
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}

```

***Explicación del ejemplo:*** 

**Sentencia 1:** establece una variable antes de que comience el bucle:

```java
int i = 0

```

**Sentencia 2:** define la condición para que el bucle se ejecute, si la condición es verdadera, el bucle se ejecuta otra vez; si es falsa, el bucle termina.:

```java
i < 5

```

**Sentencia 3:** incrementa el valor cada vez que el bloque de código se ejecuta:

```java
i++

```

---

El siguiente ejemplo solo imprime valores pares entre 0 y 10:

***Ejemplo:***

```java
for (int i = 0; i <= 10; i = i + 2) {
	System.out.println(i);
}

```

***Resultado:***

    2
    4
    6
    8
    10

---

Al igual que un bucle `while`, un bucle `for` también puede **no ejecutarse nunca**.  Si la condición es falsa desde el inicio, el código dentro del bucle se omitirá completamente.

***Por ejemplo:***

```java
for (int i = 10; i < 5; i++) {
	System.out.println("Esto nunca se imprimirá");
}

```

En este ejemplo, el bucle comienza con `i = 10`.  La condición `i < 5` ya es falsa, por lo que el cuerpo del bucle se omite y **no se imprime nada**.

---

También es posible colocar un bucle dentro de otro bucle. A esto se le llama  **bucle anidado**. El  **bucle interno**  se ejecutará una vez por cada iteración del  **bucle externo**.

Por ejemplo:

```java
for (int i = 1; i <= 2; i++) {
	System.out.println("Exterior: " + 1);

	for (int j = 1; j <= 3; j++) {
		System.out.println(" Interior: " + j);
	}
}

```

Resultado: 

    Exterior: 1
    Interior: 1
    Interior: 2
    Interior: 3
    Exterior: 2
    Interior: 1
    Interior: 2
    Interior: 3

---

El siguiente ejemplo usa bucles anidados para imprimir una tabla de multiplicar simple del 1 al 3:

```java
for (int i = 1; i <= 3; i++) {
	for (int j = 1; j <=3; j++){
		System.out.print(i * J + " ");
	}
	System.out.println();
}

```

***Resultado***

    1 2 3
    2 4 6
    3 6 9

Los bucles anidados son útiles cuando trabajas con:

-   tablas
-   matrices
-   estructuras de datos multidimensionales

---

### Bucle `for-each`

También existe un bucle llamado **for-each**, que se usa exclusivamente para recorrer elementos en un **arreglo (array)** u otras estructuras de datos.

***Sintaxis:*** 

```java
for (tipo nombreVariable : nombreArreglo) {
	// Bloque de codigo a ejecutar
}

```

El siguiente ejemplo imprime todos los elementos del arreglo `cars`:

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

for (String car : cars) {
    System.out.println(car);
}

```

No te preocupes si todavía no entiendes completamente los arreglos. Aprenderás más sobre ellos en el capítulo de  **Java Arrays**.
