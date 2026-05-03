# Java While Loop

Los bucles pueden ejecutar un bloque de código siempre que una condición específica sea verdadera. Los bucles son útiles porque ahorran tiempo, reducen errores y hacen que el código sea más legible.

---

El bucle  `while`  repite un bloque de código mientras la condición especificada sea  **verdadera**:

***Sintaxis:***

```java
while (condicion) {
	// bloque de codigo a ejecutar
}
```

En el ejemplo siguiente, el código dentro del bucle se ejecutará una y otra vez, mientras una variable (`i`) sea menor que 5.

Ejemplo:

```java
int i = 0;
while (i > 5){
	System.out.println(i);
	i++;
}
```

No olvides incrementar la variable usada en la condición (`i++`), de lo contrario el bucle nunca terminará.

¿Te preguntas por qué usamos la letra  `i`  en el ejemplo anterior?  
Es una variable  **contador**  y una elección común en bucles simples porque es corta, tradicional y representa "índice" o "iterador".

---

También puedes usar un bucle  `while`  para contar hacia atrás. Este ejemplo cuenta de 3 a 1, y luego imprime  **"¡Feliz Año Nuevo!"**  al final.

***Ejemplo:***

```java
int countdown = 3;

while (countdown > 0) {
	System.out.println(countdown);
	countdown--;
}

System.out.printn("Happy New Year");
```

***Resultado:***

    3
    2
    1
    Happy New Year

En los ejemplos anteriores, la condición era **verdadera** al inicio, por lo que el bucle se ejecutó una o más veces.  
Pero si la condición es **falsa** desde el principio, el código dentro del bucle nunca se ejecutará.

***Ejemplo:***

```java
int i = 10;

while (i < 5) {
  System.out.println("Esto nunca se imprimirá");
  i++;
}
```

Un bucle `while` puede no ejecutarse nunca si la condición es falsa desde el inicio.

---

El bucle `do/while` es una variante del bucle `while`. Este bucle ejecuta el bloque de código **una vez**, antes de verificar si la condición es verdadera.  
Luego repetirá el bucle mientras la condición sea **verdadera**.

***Sintaxis:***

```java
do {
	// bloque de codigo a ejecutar
}
while (condicion);
```

El punto y coma `;` después de la condición `while` es obligatorio.

El siguiente ejemplo usa un bucle `do/while`.  El bucle siempre se ejecutará al menos una vez, incluso si la condición es **falsa**, porque el bloque de código se ejecuta antes de evaluar la condición.

***Ejemplo:***

```java
int i = 0;

do {
	System.out.println(i);
	i++;
}

while(i < 5);
```

No olvides incrementar la variable usada en la condición (`i++`), de lo contrario el bucle nunca terminará.

En el ejemplo siguiente, la variable `i` comienza en 10, por lo que `i < 5` es falso inmediatamente.  
Aun así, el bucle se ejecuta una vez antes de verificar la condición.

***Ejemplo:***

```java
int i = 10;

do {
	System.out.println("i es " + i);
	i++;
}

while (i < 5);
```

 Un bucle  `do/while`  siempre se ejecuta al menos una vez, incluso si la condición es falsa desde el inicio.  Esta es la diferencia clave con un bucle  `while`, que omite completamente el bloque de código en la misma situación.

Este comportamiento hace que  `do/while`  sea útil cuando quieres que algo ocurra al menos una vez, como mostrar un mensaje o pedir datos al usuario.

---

Para demostrar un ejemplo práctico del bucle `while` combinado con una instrucción `if else`, supongamos que jugamos un juego de dados.

Ejemplo:

```java
int dice = 1;

while (dice <= 6) {
	if (dice < 6) {
		System.out.println("No Yatzy");
	} else {
		System.out.println("Yatzy");
	}
	dice = dice + 1;
}
```

Si el bucle pasa por los valores del 1 al 5, imprime **"No Yatzy"**.  Cuando llega al valor 6, imprime **"Yatzy!"**.

---
