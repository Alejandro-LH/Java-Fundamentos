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
