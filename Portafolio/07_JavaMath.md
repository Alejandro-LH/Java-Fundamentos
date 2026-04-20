# Java Math

La clase **Math** de Java tiene muchos métodos que te permiten realizar tareas matemáticas con números. 

- El método **`Math.max(x, y)`** se puede usar para encontrar el valor **más alto** entre **`x`** y **`y`**.

	***Por ejemplo:*** 

	```java
	Math.max(5, 10);
	```
	***Resultado:***

	`10`
	
- El método **`Math.min(x, y)`** se puede usar para encontrar el valor **más bajo** entre **`x`** y `y`.

	***Por ejemplo:*** 

	```java
	Math.min(5, 10);
	```
	
	***Resultado:***

	`5`
	
- El metodo **`Math.sqrt(x)`** devuelve la **raíz cuadrada** de **`x`**

	***Por ejemplo:*** 
	
	```java
	Math.sqrt(64);
	```
	***Resultado:***

	`8`
	
- El método **`Math.abs(x)`** devuelve el valor **absoluto (positivo)** de `x`.

	***Por ejemplo:*** 
	
	```java
	Math.abs(-35.4);
	```
	
	***Resultado:***

	`35.4`

- El método **`Math.pow(x, y)`** devuelve el valor de `x` elevado a la potencia de `y`. El método **`Math.pow()`** siempre devuelve un **double**, incluso si el resultado es un número entero.

	***Por ejemplo:*** 
	
	```java
	Math.pow(4, 3);
	```
	***Resultado:***

	`64`

---

### Rounding Methods

Java tiene varios métodos para redondear números:

-   **`Math.round(x)`**  → redondea al entero más cercano

-   **`Math.ceil(x)`**  → redondea hacia arriba (devuelve el entero más pequeño mayor o igual a  `x`)

-   **`Math.floor(x)`**  → redondea hacia abajo (devuelve el entero más grande menor o igual a  `x`)

***Por ejemplo:***

```java
Math.round(4.6);
Math.ceil(4.1);
Math.floor(4.9);
```

***Resultado:***

    5
    5.0
    4.0

---

### Random Numbers

**`Math.random()`** devuelve un número aleatorio entre **0.0 (incluido)** y **1.0 (excluido)**. Para tener más control sobre el número aleatorio, por ejemplo, si solo quieres un número entre **0 y 100**, puedes usar la siguiente fórmula:

***Ejemplo:***

```java
int randomNum = (int)(Math.random() * 101);
```

`Math.random()` devuelve un **double**.  Para obtener un número entero, necesitas convertirlo (**cast**) usando **`(int)`**.
