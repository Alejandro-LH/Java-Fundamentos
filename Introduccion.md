
# Java-Fundamentos

## Introducción a Java

**Java** es un lenguaje de programación orientado a objetos creado en **1995** por **Sun Microsystems** (actualmente propiedad de **Oracle**). Se utiliza para desarrollar una gran variedad de aplicaciones, como **aplicaciones móviles**, **aplicaciones de escritorio**, **aplicaciones web**, **servicios web**, **videojuegos** y sistemas que se conectan a **bases de datos**.

Es uno de los lenguajes más **populares** del mundo y puede ejecutarse en diferentes plataformas como **Windows**, **macOS**, **Linux** y **Raspberry Pi**, gracias a la **JVM (Java Virtual Machine)**, que permite que el mismo programa funcione en distintos sistemas operativos.

Java es conocido por ser un lenguaje **robusto**, **seguro** y ampliamente utilizado en la industria del software. Cuenta con una comunidad muy grande, con millones de desarrolladores en todo el mundo, y se utiliza tanto para proyectos profesionales como para aprender los fundamentos de la programación.


## Sintaxis

En programación, el código se organiza en estructuras para que sea más fácil de entender, reutilizar y mantener.

- Una **Función**  es un bloque de código que realiza una tarea específica y puede devolver un valor.

- Una **Clase**  es una plantilla que define cómo será un objeto (sus datos y acciones).

- Un **Atributo (o variable)**  es un dato que pertenece a una clase u objeto.

- Un **Método**  es una función que pertenece a una clase.

- Un **Parámetro**  es un valor que se le pasa a un método o función para que lo utilice.

Cada linea de codigo que se ejecuta en Java debe estar dentro de un **`class`**. el nombre de la clase debe comenzar con **la primera letra mayúscula**. 

El nombre del archivo Java debe coincidir con el nombre de la clase. Entonces, si su clase se llama **`Main`**, el archivo debe guardarse como **`Main.java`**. Esto se debe a que Java utiliza el nombre de la clase para encontrar y ejecutar su código. Sí los nombres no coinciden, Java dará un error y el programa no se ejecutará.

El método **`main()`** es obligatorio en cada programa de Java. Es donde el programa comienza a ejecutarse. 

***Por ejemplo:***

```java
public static void main(Strings[] args)
```

Cualquier código colocado dentro del método **`main()`** será ejecutado.

- **`public`**  Indica que el método puede ser accedido desde cualquier parte.

- **`static`**  Permite ejecutar el método sin crear un objeto de la clase.

- **`Main`**  Es el nombre de la clase.

- **`void`**  Significa que el método no devuelve ningún valor.

- **`String[] args`**  Permite recibir argumentos desde la línea de comandos.

- **`public static void main(String[] args)`**  Es el punto de entrada del programa. 

---

Dentro del método **`main()`**, podemos usar el metodo **`println()`** para imprimir una linea de texto en la pantalla.

***Por ejemplo:***

```java
public static void main(String[] args){
	system.out.println("Hello, World");
}	
```

Las llaves **`{}`** marcan el inicio y el final de un bloque de código.

**`System.out.print()`** puede parecer algo largo, pero puede pensar en ello como un solo comando que significa: **`"Enviar este texto a la pantalla"`**.



## Statements

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

## Comments

Los comentarios de una sola línea comienzan con dos diagonales (`//`). Cualquier texto entre  `//`  y el final de la línea es ignorado por Java (no se ejecutará). 

***Ejemplo 1:***

```java
// This is a comment
System.out.println("Hello World");
```

Este ejemplo usa un comentario de una sola línea antes de una línea de código.

***Ejemplo 2:***

```java
System.out.println("Hello World"); // This is a comment
```

Este ejemplo usa un comentario de una sola línea al final de una línea de código.

---

Los comentarios de múltiples líneas comienzan con  `/*`  y terminan con  `*/`. Cualquier texto entre  `/*`  y  `*/`  será ignorado por Java. Un comentario de múltiples líneas (un bloque de comentario) se usa para explicar el código.

***Por ejemplo:***

```java
/* The code below will print the words Hello World
to the screen, and it is amazing */
System.out.println("Hello World");
```

## Variables

Las variables son contenedores para almacenar valores de datos. En Java existen diferentes tipos de variables.

***Por ejemplo:***

- **`String:`** Almacena texto, como **`"Hello"`**. Los valores String se rodean con comillas dobles.
- **`int:`** Almacena números enteros, como **`123`** o **`-123`**. Los valores no llevan comillas dobles.
- **`float:`** Almacenan números con decimales, como **`19.99`** o **`-19.99`**. sin comillas dobles.
- **`char:`** Almacena un solo caracter, como **`'a'`** o **`'B'`**. Se rodean con comillas simples.
- **`boolean:`** Almacenan valores con dos estados: **`true`** o **`false`**.

Para declarar una variable en Java, necesitas:

 1. Elegir el tipo (**`String, int, float...`**).
 2. Darle a la variable un nombre (**`x, age, name...`**).
 3. Opcionalmente agregarle un valor (usando **`=`**).

***Por ejemplo:***

```java
// type variableName = value;
int age = 22;
String name = "Jahir";
```

***Resultado:***

    Jahir tiene 22 años

---

Tambien puedes declarar una variable sin asignarle un valor y asignarlo después.
 
 ***Por ejemplo:***
 
```java
int num = 15;
num = 20; // ahora 'num' es igual a 20.
system.out.println(num);
```

***Resultado:***

    20

---

Si no quieres que nadie mas cambien o sobrescriban el valor existente de una variable, usa la palabra calve **`final`** al inicio de la declaración (esto declara la variable como final o constante, lo que significa que no puede cambiar).

***Por ejemplo:***

```java
final int num = 15;
num = 20;  // generará un error: no se puede asignar un valor a una variable final
```

Debes declarar variables como **`final`** cuando sus valores nunca deban cambiar. Por ejemplo, el número de minutos en una hora o tu año de nacimiento.

***Por ejemplo:***

```java
final int minutes_per_hour = 60;
final int birthyear = 1980;
```

---

En Java, el simbolo **`+`** tiene dos significados:

 1. Para texto (**`Strings`**), los une (llamado ***concatenación***).
 2. Para numeros, ***suma valores***.

Para valores numéricos, el carácter **`+`** funciona como un operador matemático

El meted **`println()`** a menudo se usa para mostrar variables. Tambien se puede usar para combinar tanto **texto** como una **variable**, usando el carácter **`+`**. También puedes usar el carácter **`+`** para agregar una variable a otra variable.

***Por ejemplo:***

```java
// type variableName = value;
int age = 22;
String name = "Jahir";
System.out.println(name + " tiene " + age + " años");
```

***Resultado:***

    Jahir tiene 22 años

---

Para declarar más de una variable del mismo tipo, puedes usar una lista separada por comas.

***Por ejemplo:***

```java
int x = 5, y = 6, z = 50;
system.out.println(x + y + z);
```

***Resultado:***

    61

Declarar muchas variables en una sola línea es más corto, pero escribir una variable por línea a veces hace que el código sea más fácil de leer.

También puedes asignar el mismo valor a múltiples variables en una sola línea.

***Por ejemplo:***

```java
int x, y, z;
x = y = z = 50
System.out.println(x + y + z);
```

***Resultado:***

`150`

---

### Identifiers

Todas las variables en Java deben identificarse con nombre únicos. Estos nombres únicos se llaman **identificadores**. Los identificadores pueden ser nombres cortos (como **`x`** y **`y`**) o nombres mas descriptivos (**`agénciales`**, **`sum`**, **`totalVolume`**).

Se recomienda usar nombres descriptivos para crear código comprensible y fácil de mantener.

```java
// Bueno
int age = 20;

// Aceptable, pero no es facil de entender realmente que quiere decir.
int a = 20;
```

Las reglas generales para nombrar variables son:

- Los nombres pueden contener **`letras`**, **`dígitos`**, **`guiones bajos`** y **`signos de dolar`**.
- Los nombres deben comenzar con **una letra**.
- Los nombres deben comenzar con **una letra minúscula** y no pueden contener espacio.
- Los nombres tambien pueden comenzar con **`$`** y **`_`**.
- Los nombres distinguen entre mayúsculas y minúsculas (**`"myVar"`** y **`"myvar"`** son variables diferentes).
- Las palabras reservadas (palabras clave de Java), como **`int`** o **`boolean`**, **NO PUEDEN** usarse como nombres.

***Ejemplos de identificadores inválidos que causarían errores:***

```java
int 2ndNum = 5; 
int my num = 10;
int int = 15;
```


El método **`main()`** es obligatorio en cada programa de Java. Es donde el programa comienza a ejecutarse. 

***Por ejemplo:***

```java
public static void main(Strings[] args)
```

Cualquier código colocado dentro del método **`main()`** será ejecutado.

- **`public`**  Indica que el método puede ser accedido desde cualquier parte.

- **`static`**  Permite ejecutar el método sin crear un objeto de la clase.

- **`Main`**  Es el nombre de la clase.

- **`void`**  Significa que el método no devuelve ningún valor.

- **`String[] args`**  Permite recibir argumentos desde la línea de comandos.

- **`public static void main(String[] args)`**  Es el punto de entrada del programa. 

---

Dentro del método **`main()`**, podemos usar el metodo **`println()`** para imprimir una linea de texto en la pantalla.

***Por ejemplo:***

```java
public static void main(String[] args){
	system.out.println("Hello, World");
}	
```

Las llaves **`{}`** marcan el inicio y el final de un bloque de código.

**`System.out.print()`** puede parecer algo largo, pero puede pensar en ello como un solo comando que significa: **`"Enviar este texto a la pantalla"`**.

---


