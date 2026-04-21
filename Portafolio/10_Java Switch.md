# Java  Switch

En lugar de escribir muchas sentencias **`if...else`**, puedes usar la sentencia **`switch`**. Piensa en ello como ordenar comida en un restaurante:  

- Si eliges el número  **1**, obtienes  **Pizza**.  

- Si eliges  **2**, obtienes una  **Hamburguesa**.  

- Si eliges  **3**, obtienes  **Pasta**.  

- De lo contrario, no obtienes nada.

La sentencia  **`switch`**  selecciona uno de muchos bloques de código para ejecutar.

Por ejemplo:

```java
switch(expresion) {
	case x:
		// bloque de codigo
		break;
	
	case y:
		// bloque de codigo
		break;

	default:
		// bloque de codigo
}
```

Así es como funciona:

-   La expresión  `switch`  se evalúa  **una sola vez**.

-   El resultado se compara con cada valor  `case`.

-   Si hay coincidencia, se ejecuta el bloque correspondiente.

-   La sentencia  `break`  detiene el  `switch`  después de ejecutar el caso.

-   La sentencia  `default`  se ejecuta si no hay coincidencia.

El siguiente ejemplo usa el número del día para calcular el nombre del día:

***Ejemplo:***

```java
int day = 4;

switch (day) {
	case 1:
		System.out.println("Lunes");
		break;

	case 2:
		System.out.println("Martes");
		break;

	case 3:
		System.out.println("Miercoles");
		break;

	case 4: 
		System.out.println("Jueves");
		break;

	case 5:
		System.out.println("Viernes");
		break;
}
```

***Resultado:***

    Jueves

Cuando Java llega a la palabra clave  **`break`**, sale del bloque  `switch`.

Esto detiene la ejecución de más código y la evaluación de otros  `case`  dentro del bloque.

Cuando se encuentra una coincidencia y el trabajo está hecho, es momento de usar  `break`.  
No hay necesidad de seguir evaluando.

Un  `break`  puede ahorrar tiempo de ejecución porque  **ignora**  la ejecución del resto del código en el  `switch`.

---

La palabra clave **`default`** especifica código que se ejecuta si ningún `case` coincide.

***Por ejemplo:***

```java
int day = 4;

switch (day) {
	case 6: 
		System.out.println("Hoy es Sabado");
		break;

	case 7:
		System.out.println("Hoy es domingo");
		break;

	default:
		System.out.printn("Esperando el fin de semana");
}
```

***Resultado:***

    Esperando el fin de semana

Si la sentencia `default` se usa como la última instrucción en un bloque `switch`, **no necesita** un `break`.
