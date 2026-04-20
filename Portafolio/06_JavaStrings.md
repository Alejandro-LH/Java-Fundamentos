# Java Strings

Las cadenas se utilizan para almacenar texto.  Una variable de tipo  **String**  contiene una colección de caracteres rodeados por comillas dobles (`""`).

***Por Ejemplo***

```java
String greeting = "Hello";
```

Una  **String**  en Java en realidad es un objeto, lo que significa que contiene  **métodos**  que pueden realizar ciertas operaciones sobre las cadenas.

Por ejemplo, puedes encontrar la longitud de una cadena con el método  **length()**:

***Ejemplo***

```java
String txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
System.out.println("La longitud de la cadena de txt es: " + txt.length());
```

***Resultado:***

    La longitud de la cadena de txt es: 26

---

### More strings methods

Hay muchos métodos disponibles para cadenas en Java.

***Por ejemplo:***

- El método **`toUpperCase()`**: Convierte una cadena a letras mayúsculas. 
- El método **`toLowerCase()`**: Convierte una cadena a letras minúsculas.

```java
String txt = "Hello World";
System.out.println(txt.tuUpperCase());
System.out.println(txt.toLowerCase());
```

***Resultado:***

    HELLO WORLD
    hello world

---

### Finding a character in String

El metodo indexOf() devuelve el indice (la posición) de la primera aparición de un texto especifico en una cadena (incluyendo espacios).

***Por ejemplo:***

```java
String txt = "Please locate where 'locate' occurs";
System.out.println(txt.indexOf("locate"));
```

***Resultado***

    7

Java cuenta las posiciones desde **cero**:

-   0 es la primera posición en una cadena.

-   1 es la segunda.

-   2 es la tercera y así sucesivamente.

Se puede usar el metodo chartAt() para acceder a un caracter en una posición especifica de una cadena de texto.

***Por ejemplo:***

```java
String txt = "Hello";
System.out.println(txt.charAt(0));
System.out.println(txt.charAt(4));
```

***Resultado:***

    H
    o

---

### Comparing Strings

Para comparar dos cadenas, puedes usar el metodo equals().

***Por ejemplo:***

```java
String txt1 = "Hello";
String txt2 = "Hello";

String txt3 = "Greetings";
String txt4 = "Great things";

System.out.println(txt1.equals(txt2));
System.out.println(txt3.equals(txt4));
```

***Resultado:***

    true
    false

---

### Removing Whitespace

El método **`trim()`** elimina los espacios en blanco al inicio y al final de una cadena.

***Por ejemplo:***

```java
String txt = "   Hello World   ";
System.out.println("Antes: [" + txt + "]");
System.out.println("Despues: [" + txt.trim() + "]");
```

***Resultado:***

    Antes: [  Hello World  ]
    Despues: [Hello World]

---

### String Concatenation

El operador **`+`** puede usarse entre cadenas para combinarlas. A esto se le llama concatenación.

***Por ejemplo:***

```java
String firstName = "John";
String lastName = "Doe";

System.out.println(firstName + " " + lastName);
```

***Resultado:***

    John Doe

Se agregó un texto vacío (`" "`) para crear un espacio entre `firstName` y `lastName` al imprimir.

---

### Concatenation in Sentences

Puedes usar la concatenación de cadenas para construir oraciones con texto y variables.

***Por ejemplo:***

```java
String name = "John";
int age = 25;
System.out.println("Mi nombre es " + name + " y tengo " + age + " años.");
```

***Resultado:***

    Mi nombre es John y tengo 25 años.

---

### Concat Method

También puedes usar el método **`concat()`** para unir cadenas.

***Por ejemplo:***

```java
String  firstName  =  "John ";  
String  lastName  =  "Doe";

System.out.Println(firstName.concat(lastName));
```

***Resultado:***

    John Doe

---

También puedes unir más de dos cadenas encadenando llamadas a **`concat()`**.

***Por ejemplo:***

```java
String  a  =  "Java ";  
String  b  =  "es ";  
String  c  =  "divertido!";
String result = a.concat(b).concat(c);

System.out.println(result);
```

***Resultado:***

    Java es divertido!

Aunque puedes usar **`concat()`** para unir múltiples cadenas, la mayoría de los desarrolladores prefieren el operador **`+`** porque es más corto y fácil de leer.

---

### Adding Numbers and Strings

Java usa el operador  **`+`**  tanto para  **sumar**  como para  **concatenar**.

-   Los  **números**  se suman.

-   Las  **cadenas**  se concatenan.

Si sumas dos números, el resultado será un número, si sumas dos cadenas, el resultado será una concatenación, si sumas un número y una cadena, el resultado será una concatenación.

Por ejemplo:

```Java
int x1 = 10;
int y1 = 20;
int z1 = x + y;   // z será 30 (un número entero)

String x2 = "10";
String y2 = "20";
String z2 = x + y;   // z será "1020" (una cadena)

String x3 = "10";
int y3 = 20;
String z3 = x + y;   // z será "1020" (una cadena)
```

---

### Special Characters

Debido a que las cadenas deben escribirse entre comillas, Java puede interpretar mal una cadena y generar un error. La solución para evitar este problema es usar el  **carácter de escape backslash (`\`)**. El carácter  **`\`**  convierte caracteres especiales en caracteres de texto dentro de una cadena.

| Carácter de escape | Resultado | Descripción                     |
|--------------------|-----------|---------------------------------|
| `\'`               | '         | Comilla simple                  |
| `\"`               | "         | Comilla doble                   |
| `\\`               | \         | Barra invertida (backslash)     |

***Por ejemplo:***

```java
String txt = "Somos los llamados \"Vikingos\" del norte.";
String txt = "Está bien.";
String txt = "El carácter \\ se llama backslash.";
```

Otras secuencias de escape comunes válidas en Java:

| Código | Resultado                |
|--------|--------------------------|
| `\n`   | Nueva línea              |
| `\t`   | Tabulación               |
| `\b`   | Retroceso (backspace)    |
| `\r`   | Retorno de carro         |
| `\f`   | Salto de página          |

Las secuencias más comunes en la programación moderna son:

-   `\n`  (nueva línea)
-   `\"`  (comillas dobles)
-   `\\`  (backslash)
