# Java operators

Los operadores se utilizan para realizar operaciones sobre variables y valores. 

Por ejemplo:

```java
int x = 100 + 50;
```

Aunque el operador **+** se usa frecuentemente para sumar dos valores, como en el ejemplo anterior, también se puede usar para sumar una variable y un valor, o una variable y otra variable.

Por ejemplo:

```java
int sum1 = 100 + 50;   // 150 (100 + 50)
int sum2 = sum1 + 250; // 400 (150 + 250)
int sum3 = sum2 + sum2; // 800 (400 + 400)
```

Java divide los operadores en los siguientes grupos:

-   Operadores aritméticos
-   Operadores de asignación
-   Operadores de comparación
-   Operadores lógicos
-   Operadores a nivel de bits (bitwise)

---

### Arithmetic Operators

Los operadores aritméticos se utilizan para realizar operaciones matemáticas comunes.

| Operador | Nombre          | Descripción                                 | Ejemplo |
|----------|-----------------|---------------------------------------------|---------|
| `+`      | Suma            | Suma dos valores                            | `x + y` |
| `-`      | Resta           | Resta un valor de otro                      | `x - y` |
| `*`      | Multiplicación  | Multiplica dos valores                      | `x * y` |
| `/`      | División        | Divide un valor entre otro                  | `x / y` |
| `%`      | Módulo          | Devuelve el residuo de la división          | `x % y` |
| `++`     | Incremento      | Aumenta el valor de una variable en 1       | `++x`   |
| `--`     | Decremento      | Disminuye el valor de una variable en 1     | `--x`   |

***Por ejemplo:***

```java
int  x  =  10;  
int  y  =  3;  
  
System.out.println(x  +  y);
System.out.println(x  -  y); 
System.out.println(x  *  y); 
System.out.println(x  /  y); 
System.out.println(x  %  y);

int z = 5;

++z;
System.out.println(z);

--z
System.out,println(z);
```

***Resultado:***

    13 
    7
    30
    3
    1
    6
    5

Cuando divides dos números enteros en Java, el resultado también será un entero.  
Por ejemplo,  `10 / 3`  da  **3**.  
Si quieres un resultado decimal, usa valores  **double**, como  `10.0 / 3`.

***Por ejemplo:***

```java
int a = 10;
int b = 3;
System.out.println(a / b);

double c = 10.0d
double d = 3.0d
System.out.println(c / d);
```

***Resultado:***

    3
    3.33333...

Incrementar y decrementar es muy común en programación, especialmente cuando se trabaja con contadores, ciclos y arreglos.

El operador  **++**  aumenta un valor en 1, mientras que el operador  **--**  lo disminuye en 1.

***Por ejemplo:***

```java
int x = 5;

++x; // Incrementa x en 1
System.out.println(x); // 6

int y = 5;

--y; // Disminuye x en 1
System.out.println(y); // 4
```

***Resultado:***

    6
    4

A veces puedes incrementar y luego decrementar la misma variable.  Recuerda que si aumentas un valor y luego lo disminuyes, subirá en uno y después bajará en uno, terminando donde empezó:


***Por ejemplo:***

```java
int x = 5;

++x; // x se convierte en 6
--x; // x vuelve a 5
```

---

### Assignment Operators

Los operadores de asignación se utilizan para asignar valores a variables. 

En el siguiente ejemplo, usamos el operador de asignación  **(=)**  para asignar el valor  **10**  a una variable llamada  **x**:

```java
int x = 10;
```

El operador de asignación de suma **(+=)** agrega un valor a una variable.

***Por ejemplo:***

```java
int x = 10;
x += 5;
```
 La mayoría de los operadores de asignación son solo formas mas cortas de escribir codigo.

***Por ejemplo:***

| Operador | Ejemplo | Equivale a  |
|----------|--------|--------------|
| `=`   | `x = 5`   | `x = 5`      |
| `+=`  | `x += 3`  | `x = x + 3`  |
| `-=`  | `x -= 3`  | `x = x - 3`  |
| `*=`  | `x *= 3`  | `x = x * 3`  |
| `/=`  | `x /= 3`  | `x = x / 3`  |
| `%=`  | `x %= 3`  | `x = x % 3`  |
| `&=`  | `x &= 3`  | `x = x & 3`  |
| `|=`  | `x |= 3`  | `x = x | 3`  |
| `^=`  | `x ^= 3`  | `x = x ^ 3`  |
| `>>=` | `x >>= 3` | `x = x >> 3` |
| `<<=` | `x <<= 3` | `x = x << 3` |

---

### Comparison Operators

Los operadores de comparación se utilizan para comparar dos valores (o variables). Esto es importante en la programación, porque nos ayuda a encontrar respuestas y tomar desiciones.

El valor de retorno de una comparación es **`true`** o **`false`**. Estos valores se conocen como calores booleanos. 

En el siguiente ejemplo, usamos el operador **mayor que ( > )** para verificar si **`5`** es mayor que **`3`**:

```java
int x = 5;
int y = 3;

System.out.println(x > y); // devuelve true, porque 5 es mayor que 3
```

Los operadores de comparación se usan con frecuencia en situaciones reales, como verificar si una persona tiene la edad suficiente para votar:

```java
int age = 18;

System.out.println(age >= 18); // true, tiene la edad suficiente para votar
System.out.println(age < 18);  // false
```

---

### Logical Operators

Al igual que con los operadores de comparación, tambien puedes evaluar valores true o false usando operadores lógicos. 
Los operadores lógicos se utilizan para determinar la logica entre variables o valores, combinando múltiples condiciones.

| Operador | Nombre      | Descripción  | Ejemplo     |
|----------|-------------|-----------------------------------------------------------|----------------------|
| `&&`     | AND lógico  | Devuelve **true** si ambas condiciones son verdaderas     | `x < 5 && x < 10`    |
| `||`     | OR lógico   | Devuelve **true** si al menos una condición es verdadera  | `x < 5 || x < 4`     |
| `!`      | NOT lógico  | Invierte el resultado; devuelve **false** si era **true** | `!(x < 5 && x < 10)` |

---

### Operator Precedence

Cuando un calculo contiene mas de un operador, Java sigue las reglas en orden de operaciones para dicidir que parte calcular primero.

Por ejemplo:

```java
int result1 = 2 + 3 * 4;   // 2 + 12 = 14
int result2 = (2 + 3) * 4; // 5 * 4 = 20

System.out.println(result1);
System.out.println(result2);
```

En  `2 + 3 * 4`, la multiplicación se realiza primero, por lo que la respuesta es  **14**.

Si quieres que la suma se realice primero, debes usar paréntesis:  
`(2 + 3) * 4`, lo que da  **20**.

Usa siempre paréntesis `()` si quieres asegurarte de que el cálculo se realice en el orden que esperas. También hace que tu código sea más fácil de leer.

Aquí hay algunos operadores comunes, de mayor a menor prioridad:

- Paréntesis: `()`

- Multiplicación, División, Módulo: `*`, `/`, `%`

- Suma, Resta: `+`, `-`

- Comparación: `>`, `<`, `>=`, `<=`

- Igualdad: `==`, `!=`

- AND lógico: `&&`

- OR lógico: `||`

- Asignación: `=`

