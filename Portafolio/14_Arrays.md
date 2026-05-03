# Arrays

Los  **arrays**  se usan para almacenar múltiples valores en una sola variable, en lugar de declarar variables separadas para cada valor.

Para declarar un array, define el tipo de variable con  **corchetes**  `[ ]`:

***Sintaxis:***

```java
String[] cars;

```

---

Ahora hemos declarado una variable que contiene un array de cadenas (strings).  
Para insertar valores, puedes colocarlos en una lista separada por comas dentro de **llaves**  `{ }`:

***Sintaxis:***

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

```
---

Para crear un array de **enteros**:

***Sintaxis:***

```java
int[] myNum = {10, 20, 30, 40};

```

---

### Acceder a los elementos de un array

Puedes acceder a un elemento del array usando su  **índice**  (posición). Esta instrucción accede al valor del  **primer elemento**  en  `cars`:

***Ejemplo:***

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars[0]);

```

***Resultado:***

    Volvo

Los índices de los arrays empiezan en **0**:

    [0] → primer elemento
    [1] → segundo elemento
    [2] → tercer elemento
    [3] → cuarto elemento

--- 

### Cambiar un elemento del array

Para cambiar el valor de un elemento específico, usa su índice:

***Sintaxis:***

```java
cars[0] = "Tesla";

```

***Ejemplo:***

```java

String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

System.out.println(cars[0]);

cars[0] = "Tesla";

System.out.println(cars[0]);

```

***Resultado:***

    Volvo
    Tesla
   
---

### Longitud del array

Para saber cuántos elementos tiene un array, usa la propiedad `length`:

***Ejemplo:***

```java
String[] cars  = {"Volvo", "BMW", "Ford", "Mazda"};

System.out.println(cars.length);

```

***Resultado:***

    4

---

### Palabra clave `new`

También puedes crear un array especificando su tamaño con `new`.  Esto crea un array vacío con espacio para un número fijo de elementos.

***Ejemplo:***

```java
String[] cars = new String[4];

 cars[0] = "Tesla";
 cars[1] = "BMW";
 cars[2] = "Ford";
 cars[3] = "Mazda";

System.out.println(cars[0]);

```

***Resultado:***

    Tesla

Si ya conoces los valores, no necesitas escribir  `new`.  Ambas formas crean el mismo array.

***Ejemplo:***

```java
// Con new
String[] cars = new String[] {"Volvo", "BMW", "Ford", "Mazda"};

// Forma corta (más común)
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

```

---

No puedes escribir esto:

```java
new String[4] {"Volvo", "BMW", "Ford", "Mazda"};
```

En Java, cuando usas  `new`, debes elegir una de estas dos opciones:

**Opción 1: crear un array vacío**

```java
new String[4]

```

**Opción 2: crear el array con valores**

```java
new String[] {"Volvo", "BMW", "Ford", "Mazda"}

```

En la práctica real, el segundo caso aparece mucho cuando el tamaño depende de algo dinámic

-   Usa  `{ }`  cuando ya conoces los valores desde el inicio
-   Usa  `new`  con tamaño cuando crearás el array vacío y lo llenarás después

***Por ejemplo:***

```java
int n = 10;
int[] datos = new int[n];

```

Ahí el programa decide el tamaño en tiempo de ejecución.

---

### Arrays Loop

**Recorrer un Array**

Puedes recorrer los elementos de un array usando un bucle  `for`, y usar la propiedad  `length`  para especificar cuántas veces debe ejecutarse el bucle. 

Este ejemplo crea un array de cadenas y luego usa un bucle  `for`  para imprimir cada elemento, uno por uno.

***Ejemplo:***

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

for (int i = 0; i < cars.length; i++) {
    System.out.println(cars[i]);
}

```

***Resultado:***

    Volvo
    BMW
    Ford
    Mazda

## **Ejemplo con números**

Creamos un array de enteros y usamos un bucle  `for`  para imprimir cada valor:

***Ejemplo:***

```java
int[] numbers = {10, 20, 30, 40};

for (int i = 0; i < numbers.length; i++) { 
	System.out.println(numbers[i]);
}

```

***Resultado:***

    10
    20
    30
    40

---

### Recorrer un Array con For-Each

También existe el bucle  `for-each`, que se usa exclusivamente para recorrer elementos en un array (u otras estructuras de datos).

```java
for (tipo variable : array) {
    // código a ejecutar
}

```

El símbolo `:` se lee como **"en"**.

Puedes leerlo así:

    para cada variable en array

***Por ejemplo:***

```java
String[] cars  = {"Volvo", "BMW", "Ford", "Mazda"};

for (String car : cars) {
	System.out.printnl(car);
	
```

Esto significa:

> Para cada  `String`  en el array  `cars`, imprime su valor.

---

 **Comparación rápida**

Usa  **for normal**  cuando necesitas el índice:

```java
for (int i = 0; i < seats.length; i++) {
```

Usa  **for-each**  cuando solo necesitas los valores:

```java
for (String seat : seats) {
```

Ese detalle parece pequeño, pero en proyectos reales evita código innecesario y errores tontos.

---

**Ejemplo de la vida real: Promedio de edades**

Este programa calcula el promedio de diferentes edades:

```java
int ages[] = {20, 22, 18, 35, 48, 26, 87, 70};

float avg, sum = 0;

// Obtener la longitud del array
int length = ages.length;

// Recorrer los elementos del array
for (int age : ages) {
    sum += age;
}

// Calcular el promedio
avg = sum / length;

// Mostrar el promedio
System.out.println("El promedio de edad es: " + avg);

```

---

###  Arrays Multidimensionales

Un  **array multidimensional**  es un array que contiene otros arrays. Puedes usarlo para almacenar datos en una  **tabla con filas y columnas**.

Para crear un array bidimensional, escribe cada fila dentro de sus propias  **llaves**  `{ }`:

```java
int[][] myNumbers = { {1, 4, 2}, {3, 6, 8} };
```

Aquí,  `myNumbers`  tiene dos arrays (dos filas):

-   Primera fila:  `{1, 4, 2}`
-   Segunda fila:  `{3, 6, 8}`

Piensa en algo así:

```
        COLUMNA 0   COLUMNA 1   COLUMNA 2
FILA 0      1           4           2
FILA 1      3           6           8
```

---

 **Acceder a los elementos**

Para acceder a un elemento de un array bidimensional necesitas  **dos índices**:

-   el primero → la fila
-   el segundo → la columna

Recuerda: los índices empiezan en  **0**.

Eso significa:

    fila 0 = primera fila
    columna 0 = primera columna

***Ejemplo:***

```java
int[][] myNumbers = { {1, 4, 2}, {3, 6, 8} };

System.out.println(myNumbers[1][2]);

```

***Resultado:***

    8

---

**Cambiar valores**

Puedes sobrescribir un elemento usando la misma notación de dos índices.

***Ejemplo:***

```java
int[][] myNumbers = { {1, 4, 2}, {3, 6, 8} };

myNumbers[1][2] = 9;

System.out.println(myNumbers[1][2]);

```

***Resultado:***

    9

---

### Filas y columnas (tamaños)

Puedes usar  `length`  para obtener:

-   número de filas
-   número de columnas en una fila específica

Ejemplo:

```java
int[][] myNumbers = { {1, 4, 2}, {3, 6, 8, 5, 2} };

System.out.println("Filas: " +myNumbers.length);
System.out.println("Columnas en fila 0: " + myNumbers[0].length);
System.out.println("Columnas en fila 1: " + myNumbers[1].length);
```

Salida:

```
Filas: 2
Columnas en fila 0: 3
Columnas en fila 1: 5
```

Las filas pueden tener  **diferente tamaño**, y eso es totalmente válido en Java. No todas las tablas tienen que ser perfectamente cuadradas. Java lo permite.

---

**Recorrer un array multidimensional**

Puedes usar un  `for`  dentro de otro  `for`  para visitar cada elemento fila por fila.

```java
int[][] myNumbers = { {1, 4, 2}, {3, 6, 8, 5, 2} };

for (int row = 0; row < myNumbers.length; row++) {    
	for (int col = 0; col < myNumbers[row].length; col++) {        
		System.out.println("myNumbers[" + row + "][" + col + "] = " + myNumbers[row][col]);
	}
}
```

Aquí ocurre lo clásico:

```
for externo → filasfor interno → columnas
```

Ese patrón aparece en:

-   matrices
-   tablas
-   juegos
-   imágenes
-   datos científicos
-   algoritmos
