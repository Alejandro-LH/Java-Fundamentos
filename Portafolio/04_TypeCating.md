## Type Cating

La conversion de tipos significa convertir un tipo de dato en otro. Por ejemplo convertir un int a un double. En Java hay dos tipos de conversión.

1. **Widening Casting** (automatico): Convertir un tipo mas pequeño a un tipo de mayor tamaño.

***Por ejemplo:***

    byte -> short -> char -> int -> long -> float -> double

2. **Narrowing Casting** (manual): Convertir un tipo mas grande a un tipo de menor tamaño.

***Por ejemplo:***

    double -> float -> long -> int -> char -> short -> byte

---

**Conversión Ascendente (Widening Casting)**

La conversión ascendente se realiza automáticamente cuando se pasa un tipo de menor tamaño a uno de mayor tamaño. Esto funciona porque no hay riesgos de perder información. Por ejemplo un valor **`int`** puede caber de forma segura dentro de un **`double`**.

***Por ejemplo:***

```java
int myInt = 9;
double myDouble = myInt; // Conversion automatica: int a double

System.out.println(myInt);
System.out.println(myDouble);
```

***Resultado:***

    9
    9.0

---

**Conversión Descendente (Narrowing Casting)**

La conversion descendente debe hacerse manualmente colocando el tipo entre paréntesis **`()`** delante del valor. Esto es necesario porque la conversion descendente puede provocar perdida de datos (por ejemplo, eliminar decimales al convertir un **`double`** a un **`int`**).

***Por ejemplo:***

```java
double myDouble = 9.78d;
int myInt = (int) myDouble; // Conversion manual: double a int

System.out.println(myDouble);
System.out.println(myInt);
```

***Resultado:***

    9.78
    9
