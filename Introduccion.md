
# Java

**Java** es un lenguaje de programación creado en **1995** por **Oracle**.
Se utiliza para crear **aplicaciones móviles**, **aplicaciones de escritorio**, **aplicaciones web**, **servicios web**, **juegos**, conexiones a **bases de datos** y mucho más.

Es uno de los lenguajes más **populares** del mundo y puede ejecutarse en **diferentes plataformas** como **Windows**, **Mac**, **Linux** y **Raspberry Pi**.

Java es un lenguaje **fácil de aprender** y **simple de usar**. Es **gratuito**, **seguro**, **rápido** y **poderoso**.
Cuenta con una comunidad muy grande, con cerca de **10 millones** de desarrolladores.

A menudo se utiliza para programar tareas del día a día.

---

## Introducción a Java

Como primera practica haremos el famoso "Hello, World"

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World");
    }
}
```
**Resultado:**
```
Hello, World
```

**`public class`**  
Se usa para definir una clase que puede ser accedida desde cualquier parte del programa.

### ¿Por qué usamos `public static void main(String[] args)` dentro de un `public class`?

Porque en Java, el método `main` debe estar dentro de una clase.  
La **JVM (Java Virtual Machine)** busca el método `main` en la clase especificada para iniciar la ejecución del programa.

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

---


