# Java Conditions and If Statements


Las condiciones y las sentencias  **`if`**  te permiten controlar el flujo de tu programa, decidiendo qué código se ejecuta y qué código se omite. Es como en la vida real:  **Si llueve, toma un paraguas. De lo contrario, no hagas nada.**

Cada sentencia  **`if`**  necesita una condición que resulte en  **`true`**  o  **`false`**. Esto significa que las sentencias  **`if`**  trabajan de la mano con valores  **`boolean`**.

***Por ejemplo:***

```java
boolean llueve = true;

if (llueve) {
	System.out.println("Trae un paraguas, esta lloviendo");
}
```

***Resultado:***

    Trae un paraguas, esta lloviendo

La mayoría de las veces, las condiciones se crean usando comparativos de comparación, como los siguientes:

-   Menor que:  `a < b`

-   Menor o igual que:  `a <= b`

-   Mayor que:  `a > b`

-   Mayor o igual que:  `a >= b`

-   Igual a:  `a == b`

-   Diferente de: `a != b`

Puedes usar estas condiciones para realizar diferentes acciones según diferentes decisiones. Java tiene las siguientes sentencias condicionales:

- Usar **`if`** para epecificar un bloque de codigo que se ejecutara si una condición es verdadera.

- Usar **`else`** para especificar un bloque de codigo que se ejecutara si la misma condición es falsa.

- Usar **`else if`** para especificar una nueva condición si la primera condición es falsa.

- Usar **`switch`** para especificar muchos bloques alternativos de codigo que se ejecutaran.

---

### La Sentencia if

La sentencia **`if`** especifica un bloque de código que se ejecutará si una condición es **`true`**.

La  **condición**  dentro de la sentencia  **`if`**  debe resultar en un valor  **`boolean`**; puede ser una expresión booleana (como  `x > y`) o una variable booleana (como  `isLightOn`). También nota que  **`if`**  se escribe en letras minúsculas. Las letras mayúsculas (**`If`**  o  **`IF`**) generarán un error.


***Por ejemplo:***

```java
if (condición) {
    // bloque de código que se ejecutará si la condición es verdadera
}

if (20 > 10) {
	System.out.println("20 es mayor que 10");
}
```

***Resultado:***

    20 es mayor que 10

Si una sentencia **`if`** tiene solo una línea de código, puedes escribirla sin llaves `{ }`:

***Por ejemplo:***

```java
if (20 > 18)
    System.out.println("20 es mayor que 10");
```

***Resultado:***

    20 es mayor que 10

Sin llaves, solo la **primera línea** después del **`if`** pertenece a él.  Cualquier otra línea se ejecutará siempre, lo que puede causar resultados inesperados. Para evitar errores, usa siempre llaves `{ }`.   Esto deja claro qué líneas pertenecen a la sentencia **`if`**.

---

### La sentencia else

La sentencia **`else`** te permite ejecutar un bloque de código cuando la condición en la sentencia **`if`** es **`false`**.

***Ejemplo:*** 

```java
boolean llueve = false;

if (llueve) {
	System.out.println("Esta lloviendo, trae paraguas");
} else {
	System.out.println("No esta lloviendo, no traigas el paraguas");
```
  
***Resultado:***

    No esta lloviendo, no traigas el paraguas

Como **`llueve`** es **`false`**, la condición dentro del **`if`** no se cumple.  Eso significa que el bloque **`if`** se omite y se ejecuta el bloque **`else`**.


-   **`else`**  no tiene una condición; se ejecuta cuando la condición del  **`if`**  es  **`false`**.

-   No pongas un  **punto y coma `(;)`**  justo después de  `if (condición)`.  
    Eso terminaría la sentencia antes de tiempo y haría que  **`else`**  se comporte de forma inesperada.

---

### La Sentencia else if

Usa la sentencia **else if** para especificar una nueva condición que se probará si la primera condición es **false**.

***Por ejemplo:***

```java
if (condición1) {
    // código si condición1 es verdadera
} else if (condición2) {
    // código si condición1 es falsa y condición2 es verdadera
} else {
    // código si ambas condiciones son falsas
}
```

Piénsalo como en la vida real:  

1. **Si llueve, lleva un paraguas.**

2. **Si hace sol, usa lentes de sol.** 

3. **Si no, sal normalmente.**

***Por ejemplo:***

```java
int weather = 2;  // 1 = lluvia, 2 = soleado, 3 = nublado

if (weather == 1) {
    System.out.println("Trae un paraguas");
} else if (weather == 2) {
    System.out.println("Usa lentes de sol");
} else {
    System.out.println("Sal normalmente");
}
```

***Resultado:***

    Usa lentes de sol

Como **weather** es **2**, la primera condición (`weather == 1`) no se cumple.  Luego el programa verifica la condición **else if** (`weather == 2`), que es **true**,  por lo que se ejecuta ese bloque.

---

### Java Short Hand If...Else

También existe una forma corta de  **`if else`**, conocida como el  **operador ternario**  porque consta de tres operandos. Puede usarse para reemplazar múltiples líneas de código con una sola línea y se utiliza con mayor frecuencia para reemplazar sentencias simples de  **`if else`**.

***Sintaxis:***

```java
variable = (condicion) ? expresionVerdadera : expresionFalsa
```

***Por ejemplo:***

```java
int time = 20;

// En lugar de escribir:
if (time < 18) {
  System.out.println("Buen día.");
} else {
  System.out.println("Buenas noches.");
}

// Puedes simplemente escribir:
String result = (time  < 18) ? "Buen dia." : "Buenas noches";
System.out.println(result);
```

***Resultado:***

    Buenas noches.
    Buenas noches.

---

También puedes usar el operador ternario directamente dentro de `System.out.println()` sin una variable temporal.

***Por ejemplo:***

```java
int time = 20;

System.out.println((time < 18) ? "Buen día." : "Buenas noches.");
```

***Resultado:***

    Buenas noches.

---

### Java Nested If

También puedes colocar una sentencia `if` dentro de otra `if`.   Esto se llama una sentencia **if anidado**. Un **if anidado** te permite verificar una condición solo si otra condición ya es **verdadera**.

***Sintaxis:***

```java
if (condicion1) {
	// codigo que se ejecuta si condicion es verdadera

	if (condicion2) {
		// codigo que se ejecuta si condicion1 y condicion2 son verdadera
	}
}
```

En el siguiente ejemplo, primero verificamos si **x** es mayor que 10.  Si lo es, entonces verificamos si **y** es mayor que 20.

***Ejemplo:***

```java
int x = 15;
int y = 20;

if (x > 10) {
	System.out.println("x es mayor que 10");
	if (y > 20) {
	System.out.println("y tambien es mayor que 20");
	}
}
```

***Resultado:***

    x es mayor que 10

---

Las sentencias **`if`** anidadas son útiles cuando necesitas probar múltiples condiciones que dependen unas de otras.  Por ejemplo, verificar si una persona tiene la edad suficiente para votar y si es ciudadana.

***Ejemplo:***

```java
int edad = 20;
boolean ciudadano = true;

if (edad >= 18) {
	System.out.println("Tienes edad para votar ");
	
	if (ciudadano) {
		System.out.print("Tambien eres ciudadano, asi que puedes votar ");
	} else {
	System.out.println("Tienes edad, pero no eres ciudadano para poder votar");
	}
	
} else {
System.out.println("No tienes edad para votar");
}
```

***Resultado:***

    Tienes edad para votar. También eres ciudadano, así que puedes votar 

Puedes anidar tantos  `if`  como quieras, pero evita que el código sea demasiado profundo, ya que puede volverse difícil de leer.

El  `if`  anidado se usa frecuentemente junto con  `else`  y  `else if`  para tomar decisiones más complejas.

---

### Java Logical Operators in Conditions

Puedes  **combinar o invertir condiciones**  usando  **operadores lógicos**. Estos trabajan junto con  `if`,  `else`  y  `else if`  para construir decisiones más complejas.

-   **AND (`&&`)** : todas las condiciones deben ser verdaderas. Usa **AND (`&&`)** cuando **ambas condiciones** deben ser verdaderas:

	***Por ejemplo:***
	
	```java
	int a = 200;
	int b = 33;
	int c = 500;
	
	if (a > b && c > a) {
		System.out.println("Ambas condiciones son verdaderas");
	}
	```

	***Resultado:***

	    Ambas condiciones son verdaderas


-   **OR (`||`)** : al menos una condición debe ser verdadera. Usa **OR (`||`)** cuando **al menos una** de las condiciones puede ser verdadera:

	***Por ejemplo:***
	
	```java
	int a = 200;
	int b = 33;
	int c = 500;
	
	if (a > b || c > a) {
		System.out.println("Al menos una condicion es verdadera");
	}
	```

	***Resultado:***

	    Al menos una condicion es verdadera


-   **NOT (`!`)** : invierte una condición (verdadero = falso, falso = verdadero). Usa **NOT (`!`)** para **invertir** una condición:


	***Por ejemplo:***
	
	```java
	int a = 33;
	int b = 200;

	
	if (!(a > b)) {
		System.out.println("'a' NO es mayor que 'b'");
	}
	```

	***Resultado:***

	    'a' NO es mayor que 'b'

En programas reales, los operadores lógicos se usan frecuentemente para  **control de acceso**.  
Por ejemplo, para acceder a un sistema, hay requisitos específicos:

Debes haber iniciado sesión, y luego necesitas ser administrador  **o**  tener un nivel de seguridad alto (nivel 1 o 2):

```java
boolean isLoggedIn = true;
boolean isAdmin = false;
int securityLevel = 3; // 1 = nivel mas alto

if (isLoggedIn && (isAdmin || securityLevel <=2)) {
	System.out.println("Acceso Concedido");
} else { 
	System.out.println("Acceso Denegado");
}
```

***Resultado:***

    Acceso Denegado

