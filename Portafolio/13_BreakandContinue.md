# Java Break and Continue

### Break

Ya viste la instrucción  `break`  en un capítulo anterior. Se usaba para  **salir**  de una instrucción  `switch`. La instrucción  `break`  también puede usarse para  **salir de un bucle**.

Este ejemplo detiene el bucle cuando  `i`  es igual a  **4**:

```java
for (int i = 0; i < 10; i++) {
	if (i == 4) {
		break;
	}
	System.out.println(i);
}

```

***Resultado:***

    0
    1
    2
    3

Cuando llega a **4**, el bucle se detiene completamente. Se acabó la fiesta, se apagan las luces.

---

### Continue

La instrucción  `continue`  interrumpe  **solo una iteración**  del bucle si ocurre una condición, y luego continúa con la siguiente vuelta.

Este ejemplo **salta el valor 4**:

```java
for (int i = 0; i < 10; i++) {
	if (i ==4) {
		continue;
	}
	System.out.println(i);
}

```

***Resultado:***

    0
    1
    2
    3
    5
    6
    7
    8
    9

El **4 no aparece**, pero el bucle sigue trabajando como si nada hubiera pasado.
El programa piensa:

> "Ah, es 4.  
> No imprimas nada.  
> Bríncate esta vuelta y sigue."

---

Imagina que procesas una lista de números donde:

-   quieres  **ignorar números negativos**
-   pero  **detenerte completamente si encuentras un cero**

***Ejemplo:***

```java
int[] numbers = {3, -1, 7, 0, 9};

for (int n : numbers) {

    if (n < 0) {
        continue; // saltar números negativos
    }

    if (n == 0) {
        break; // detener el bucle si se encuentra un cero
    }

    System.out.println(n);
}

```

***Resultado:***

    3
    7

-   `-1`  se ignora
-   cuando aparece  `0`, todo se detiene
-   `9`  nunca se procesa
