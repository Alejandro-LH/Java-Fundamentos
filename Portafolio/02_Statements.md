# Statements

Un programa de computadora es **una lista de instrucciones** que serán ejecutadas por una computadora. En el lenguaje de de programación, estas instrucciones se llaman sentencias (**`Statements`**).

***Por ejemplo:***

```java
System.out.println("Java is fun!");
```

***Resultado:***

`Java is fun!`

---

La **sentencia** le indica al compilador que imprima el texto **`"Java is fun!"`** en la pantalla. Es importante que termines la sentencia con punto y coma (**`;`**).  Si olvidas el punto y coma (**`;`**) ocurrirá un **error** y el programa **no se ejecutará.**

***Por ejemplo:***

```java
System.out.println("Java is fun!")
```

***Resultado:***

    error: ';' expected

---
La mayoría de los programas Java contienen muchas sentencias. Las sentencias se ejecutan una por una, **en el mismo orden que están escritas**.

***Por ejemplo:*** 

```java
System.out.println("Hello World");
System.out.println("Have a good day");
System.out.println("Learning Java is fun");
```

La primera sentencia se ejecuta primero (imprime  **`"Hello World"`**  en la pantalla).  
Luego se ejecuta la segunda sentencia (imprime  **"`Have a good day`"**  en la pantalla).  
Y finalmente, se ejecuta la tercera sentencia (imprime  **`"Learning Java is fun"`**  en la pantalla).

***Resultado:***

    Hello World
    Hava a good day
    Learning Java is fun

Puedes agregar tantos métodos **`println()`** como quieras. Ten en cuenta que se agregaran a una nueva línea por cada método.

---

El texto debe de ir dentro de comillas dobles **`" "`**. Si olvidas las comillas, ocurrirá un error:

***Por ejemplo:***

```java
System.out.println(Java is fun):
```

***Resultado:***

    error: cannot find symbol

---

Tambien existe le método **`print()`**, que es similar al **`println()`**. La única diferencia es que no inserta una nueva linea al final de la salida

***Por ejemplo:***

```java
System.out.print("Hello World ");
System.out.print("Java is fun ");
```

***Resultado:***

    Hello World Java is fun

 ---

### Numbers

Tambien podemos usar el metodo **`println()`** para imprimir números, sin embargo, a diferencia del texto, no ponemos los números detro de comillas dobles (**`" "`**).

***Por ejemplo:***

```java
System.out.println(3);
System.out.println(358);
System.out.println(50000);
```

***Resultado:***

    3
    358
    50000

---

También podemos realizar cálculos matemáticos dentro del **`println()`**.

***Por ejemplo:***

```java
System.out.println(3 + 3);
System.out.println(2 * 5);
```

***Resultado:***

    6
    10
