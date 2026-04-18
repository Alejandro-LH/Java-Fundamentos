## Data Types

Como se especifico en el capitulo anterior, una variable en Java debe tener un tipo de dato especificado.

***Por ejemplo:***

```java
int myNum = 5;          // Entero (número entero)
float myFloatNum = 5.99f; // Número de punto flotante
char myLetter = 'D';    // Carácter
boolean myBool = true;  // Booleano
String myText = "Hello"; // Cadena de texto
```

Los tipos de datos se dividen en dos grupos:

- Tipos de datos primitivos: incluyen byte, short, int, long, float, double, boolean y char.

- Tipos de datos no primitivos: como String, Arreglos (Arrays) y Clases.

---

### Tipos de datos primitivos

Un tipo de dato primitivo especifica el tipo de una variable de valores que pueden almacenar. Hay ocho tipos de datos primitivos en Java.


 1. **`byte`**: Almacena números enteros desde **`-128 hasta 127`**. Puede usarse en lugar de **`int`** u otros tipos enteros para ahorrar memoria cuando estás seguro de que el valor estará dentro de ese rango.

	***Por ejemplo:***

	```java
	byte myNum = 100;
	```

 3. **`short`**: Almacena números enteros desde **`-32,768 hasta 32,767`**.

	***Por ejemplo:***

	```java
	short myNum = 5000;
	```
	
 4. **`int`**: Almacena números enteros desde **`-2,147,483,648 hasta 2,147,483,647`**. En general, **`int`** es el tipo de dato preferido cuando creamos variables con un valor numérico.

	***Por ejemplo:***

	```java
	int myNum = 100000;
	```
	
 5. **`long`**: Almacena números enteros desde **`-9,223,372,036,854,775,808 hasta 9,223,372,036,854,775,807`**. Se usa cuando **`int`** no es lo suficientemente grande para almacenar el valor.

	***Por ejemplo:***

	```java
	long myNum = 15050050000L; // Debes terminar el valor con una "L".
	```
	
 6. **`float`**: Almacena números decimales. suficiente para **`6`** a **`7`** dígitos decimales. 

	***Por ejemplo:***

	```java
	float myNum = 5.75f; // Para float, debe terminar con una "f".
	```
	
 7. **`double`**: Almacena números decimales. Suficiente para **`15`** a **`16`** dígitos decimales. Es mas seguro usar double para la mayoría de calculos. 

	***Por ejemplo:***

	```java
	double myNum = 19.99d; // Para double, debe terminar con una "d".
	```
	
 8. **`boolean`**: Almacena valores **`verdadero`** o **`falso`**.

	***Por ejemplo:***

	```java
	byte myNum = 100;
	```
	
 9. **`char`**: Almacena un solo **`caracter/letra`** o valores **`ASCII`**

	***Por ejemplo:***

	```java
	byte myNum = 100;
	```
	
Una vez que una variable se declara con un tipo, no puede cambiar a otro tipo mas tarde en el programa.

***Por ejemplo:***

```java
int myNum = 5;
myNum = "5"; // Error: no se puede asignar un String a un int.

String myTex = "Cinco";
myTex = 5; // Error: no se puede asignar un int a un String.
```

Esta regla hace que Java sea mas seguro, porque el compilador te detendrá si intentas mezclar tipos por error. 
Si realmente necesitas cambiar entre tipos, debes usar una conversión de tipos (**`type casting`**) o métodos de conversión (por ejemplo convertir un **`int`** en un **`dooble`**).

---

Los tipos de datos primitivos se dividen en dos grupos:

1. **Enteros** (**`Integer`**): Almacenan números enteros, positivos o negativos, sin decimales. Los tipos validos son:
	
		- byte
		- short
		- int
		- long

	El tipo que debes usar depende del valor numerico.

2. **Punto flotante** (**`floating point`**): Representan numeros con una parte fraccionaria, que contienen uno o mas decimales. Hay dos tipos:

		- float
		- double

Aunque hay muchos tipos numéricos en Java, los mas usados para números son: **`int`** (para números enteros) y **`double`** (para números decimales).

---

Un numero de punto flotante también puede ser un **numero científico**, usando una "**`e`**" para indicar la potencia 10.

***Por ejemplo:***

```java
float f1 = 35e3f;
double d1 = 12E4d;
System.out.println(f1);
System.out.println(d1);
```

***Resultado:***

    35000.0
    120000.0

---

#### Booleans

Muy a menudo en programación, se necesitara un tipo de dato que solo pueda tener uno de dos valores, como:

	- SÍ / NO
	- ENCENDIDO / APAGADO
	- VERDADERO / FALSO

Por eso Java tiene un tipo de dato **`boolean`**, que solo puede tomar valores **`true`** o **`false`**.

---

#### Characters

El tipo de dato **`char`** se usa para almacenar un solo caracter. El caracter debe estar rodeado por comillas simples, como **`'A'`** o **`'c'`**.

***Por ejemplo:***

```java
char MyGrade = 'B';
```

Alternativamente, si estas familiarizado con los valores **ASCII**, puedes usarlos para mostrar ciertos caracteres.

***Por ejemplo:***

```java
char myVar = 65, myVar2 = 66, myVar3 = 67;

System.out,println(myvar);
System.out,println(myVar2);
System.out,println(myVar3);
```

***Resultado:***

    A
    B
    C

En Java, **`char`** guarda **caracteres**, y los números **65, 66 y 67** se interpretan como **códigos ASCII**.

Una lista de todos los valores ASCII se puede encontrar en la **tabla ASCII**.

---

### Tipo de datos no primitivos

Los tipos de datos **no primitivos** se llaman tipos de referencias porque se **refieren a objetivos**. Las principales diferencias entre los tipos primitivos y no primitivos son:

- **Los tipos primitivos** en Java están predefinidos e **integrados en el lenguaje**, mientras que los tipos **no primitivos** son **creados por el programador** (excepto **`String`**).

- Los tipos **no primitivos pueden usar métodos** para realizar ciertas operaciones, mientras que los tipos **primitivos no pueden**.

- Los tipos primitivos **comienzan con la letra minúscula** (como **`int`**), mientras que los no primitivos normalmente **empiezan con una letra mayúscula** (como ***String***).

- Los tipos **primitivos almacenan un valor**, mientras que los **no primitivos** pueden **almacenar `null`**. 
	
	***Por ejemplo:***

		- Strings
		- Arrays
		- Clases

---

#### Strings

El tipo de dato **`String`** se usa para almacenar una secuencia de caracteres (texto).  
Los valores de tipo String deben estar rodeados por comillas dobles.

Por ejemplo:

```java
String greeting = "Hello World";
```

El tipo  **String**  se usa tanto e integrado en Java, que algunos lo llaman el  **"noveno tipo especial"**. Un  **String**  en Java es en realidad un  **tipo de dato no primitivo**, porque se refiere a un objeto.  El objeto String tiene métodos que se usan para realizar ciertas operaciones con cadenas.

---

#### Var KeyWord 

La palabra clave var permite que el compilador detecte automáticamente el tipo de dato de una variable, basándose en el valor que le asignes. Esto ayuda escribir codigo mas limpio y evitar repetir tipos, especialmente largos o complejos. Puede usarse para crear variables de diferentes tipos, basándose en los valores que asignas

***Por ejemplo:***

```java
var myNum = 5;        // int
var myDouble = 9.98;  // double
var myChar = 'D';     // char
var myBoolean = true; // boolean
var myString = "Hello"; // String
```

**`var`** solo funciona cuando asignas un valor al mismo tiempo (no puedes declarar `var x;` sin asignar un valor):

***Por ejemplo:***

```java
var x;     // Error
var x = 5; // Correcto
```

Una vez que el tipo es elegido, se mantiene igual.

***Por ejemplo:***

```java
var x = 5;  // x ahora es un int
x = 10;     // Correcto — sigue siendo int
x = 9.99;   // Error — no se puede asignar un double a un int
```

Para variables simples, normalmente es más claro escribir el tipo directamente (`int`,  `double`,  `char`, etc.). Pero para tipos más complejos, como  **`ArrayList`**  o  **`HashMap`**,  **`var`**  puede hacer el código más corto y fácil de leer

***Por ejemplo:***

```java
// Sin var
ArrayList<String> cars = new ArrayList<String>();

// Con var
var cars = new ArrayList<String>();
```

El ejemplo anterior parece un poco avanzado, pero aprenderás más sobre estos tipos complejos después.
