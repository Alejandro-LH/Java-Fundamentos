# Java Booleans

Muy a menudo en programación, necesitarás un tipo de dato que solo pueda tener uno de dos valores, como:

-   **SÍ / NO**
-   **ENCENDIDO / APAGADO**
-   **VERDADERO / FALSO**

Un tipo booleano se declara con la palabra clave **boolean** y solo puede tomar los valores **true** o **false**.

***Por ejemplo:***

```java
boolean isJavaFun = true;
boolean isFishTasty = false;

System.out.println(isJavaFun); 
System.out.println(isFishTasty);  
```

***Resultado:***

    true
    false

En la práctica, los booleanos son más comúnmente el resultado de  **expresiones**, y se usan para probar  **condiciones**  en los programas.

---

Una expresión booleana devuelve un valor booleano:  **true**  o  **false**. Esto es útil para construir lógica y tomar decisiones en los programas. Por ejemplo, puedes usar un  **operador de comparación**, como el operador  **mayor que (>)**, para averiguar si una expresión (o una variable) es verdadera o falsa o también usamos el operador **igual a (==)** para evaluar una expresión.

***Por ejemplo:***

```java 
int x = 10;
int y = 5;

System.out.println(x > y);
System.out.println(10 < 5);
System.out.println(x == y);
System.out.println(x == 10);
```

***Resultado***

    true
    false
    false
    true

---

También puedes guardar el resultado de una comparación en una variable  **boolean**. Depende de ti si guardas el resultado de una comparación en una variable booleana o usas la comparación directamente.   Guardar el resultado puede hacer que tu código sea más fácil de leer, especialmente si quieres reutilizarlo.

***Por ejemplo:***

```java
int x = 10;
int y = 9;
boolean z = x > y;

System.out.println(z);
```

***Resultado:***

    true
