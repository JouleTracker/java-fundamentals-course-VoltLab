# Guion de Video - Lección 3: Estructuras de Control (Decisiones y Bucles)

* **Duración grabada:** 11:56 minutos.
* **Público objetivo:** Estudiantes de secundaria (12 a 17 años) sin conocimientos previos de programación.
* **Herramienta demostrada:** Editor de código en línea / IDE.
* **Regla de estilo:** Cero mención a nombres propios, integrantes o marcas de equipo. Lenguaje claro, dinámico, fluido y demostración práctica en vivo paso a paso.

---

## ⏱️ Estructura y Cronograma del Video Grabado

| Minuto | Sección | Acción visual / En pantalla |
|---|---|---|
| 00:00 - 01:05 | Introducción y analogía | Explicación conceptual con analogías de videojuegos (game over, pasar de nivel) y semáforo. |
| 01:05 - 02:40 | Estructura condicional básica `if` / `else` | Código de la montaña rusa en el editor. Prueba con valor inicial 130 (denegado) y cambio en vivo a 180 (concedido). |
| 02:40 - 05:30 | Condicional compuesta con `else if` y operador lógico `&&` | Código de acceso con acompañante adulto. Pruebas exhaustivas de casos en vivo (tabla de verdad de `&&`). |
| 05:30 - 07:40 | Bucles determinados: El bucle `for` | Cuenta regresiva del cohete del 5 al 1. Explicación paso a paso de la traza de ejecución e iteraciones de la variable `i`. |
| 07:40 - 10:45 | Bucles condicionales: El bucle `while` | Carga de batería del robot explorador de 70% a 100%. Explicación detallada de cada ciclo de evaluación y actualización de variable. |
| 10:45 - 11:56 | Recomendaciones fundamentales y Cierre | Explicación de cómo evitar bucles infinitos, importancia de las llaves `{}` y resumen final. |

---

##  Guion y Locución del Video

### [00:00 - 01:05] Introducción: Decisiones y Repetición en Programación
**[En pantalla: Portada de la lección 3 / diapositiva de introducción].**

**Locución:**
> "Bienvenidos a la lección número 3 de nuestro curso de Java para principiantes.
>
> Hasta el momento, hemos aprendido qué son las variables y cómo almacenar datos como números y textos. Pero en el mundo real, los programas no se limitan a seguir una sola línea recta de principio a fin.
>
> Piensa en tus videojuegos favoritos: si tu personaje tiene cero vidas, aparece la pantalla de *Game Over*; si cruza la meta, pasa al siguiente nivel. O piensa en un semáforo: si la luz es verde, avanzamos; si es roja, nos detenemos.
>
> Hoy aprenderás a darle ese poder de decisión a tus programas utilizando **estructuras condicionales** y descubriremos cómo automatizar tareas repetitivas usando **bucles**, así que empecemos."

---

### [01:05 - 02:40] Parte 1: Estructura condicional `if` / `else`
**[En pantalla: Editor de código mostrando el programa de acceso a la montaña rusa].**

**Locución:**
> "La palabra clave en programación para evaluar una condición es `if`, que en inglés significa 'si condicional'.
>
> Imaginemos que estamos programando el sistema de acceso para una montaña rusa en un parque de diversiones. La regla es clara: para subir, necesitas medir al menos 140 centímetros.
>
> Como vemos en el programa, la estatura inicial es 130. Nuestra condicional `if` menciona que la estatura debe ser mayor o igual a 140 centímetros. Si eso cumple, entonces el sistema imprimirá 'Acceso concedido'. De lo contrario, se ejecutará lo que está dentro del `else`, que el acceso es denegado.
>
> Como nuestra estatura inicial es 130, entonces el sistema debe imprimir el acceso denegado. Para ello, procederemos a ejecutar."

**[Acción en pantalla: Código base en el editor y primera ejecución]:**
```java
int estatura = 130;

if (estatura >= 140) {
    System.out.println("Acceso concedido");
} else {
    System.out.println("Acceso denegado");
}
```

**Locución:**
> "Como vemos acá a la derecha, el acceso es denegado, ya que nuestra estatura es 130.
>
> Así que probaremos con una estatura de 180... y ejecutamos.
>
> Como la estatura es mayor o igual a 140, entonces el sistema imprimió 'Acceso concedido'."

---

### [02:40 - 05:30] Parte 2: Opción intermedia con `else if` y operador `&&`
**[En pantalla: Se amplía el código incorporando la variable booleana y la cláusula else if].**

**Locución:**
> "Ahora demos un paso más: ¿qué ocurre si queremos contemplar una opción intermedia? Por ejemplo, si el estudiante mide entre 120 y 139 centímetros, pero viene acompañado por un adulto, también podría ingresar.
>
> Para eso utilizamos `else if` con el operador lógico doble ampersand (`&&`).
>
> Volviendo al código: tenemos una estatura inicial de 110 y una condicional de `true` de que el estudiante viene con un adulto. Según nuestra condición, se cumple que si la estatura es mayor o igual a 140, el acceso es concedido. Acá tenemos una condición intermedia utilizando el `else if`, que menciona que si la estatura es mayor o igual a 120 y además el estudiante viene con un adulto, también se le dará el acceso concedido. Si no cumple ninguna de esas dos condicionales, entonces se ejecutará lo del `else`: el acceso es denegado."

**[Acción en pantalla: Estructura condicional completa]:**
```java
int estatura = 110;
boolean conAdulto = true;

if (estatura >= 140) {
    System.out.println("Acceso concedido");
} else if (estatura >= 120 && conAdulto) {
    System.out.println("Acceso concedido");
} else {
    System.out.println("Acceso denegado");
}
```

**[Acción en pantalla: Demostración de los 4 casos en vivo]:**

**Locución:**
> 1. *"Probemos primero con una estatura mayor a 140 centímetros (por ejemplo 180). Procedemos a ejecutar el programa y como vemos nos dio el acceso concedido."*
> 2. *"Ahora, ¿qué pasa si la estatura, como menciona acá el `else if`, es mayor o igual a 120 y además se cumple que el estudiante viene con un adulto, o sea, es `true`? También le da acceso. Para probarlo, ponemos una estatura de 130, ejecutamos y, como vemos, también se le dio acceso."*
> 3. *"Ahora, ¿qué pasaría si la estatura es mayor que 120, pero el estudiante no viene con un adulto, o sea, cambiamos esto a `false`? Ejecutamos y vemos que ya no se cumple. Se cumple esta condición, pero esta ya no se cumple (da Acceso denegado)."*
> 4. *"Ahora, ¿qué pasaría si esta se cumple (`conAdulto = true`), pero esta no se cumple (`estatura = 110`)? Ejecutamos y nos dio el acceso denegado.*
>
> *Esto nos quiere decir que para que el sistema nos dé el acceso concedido en el `else if`, ambas condiciones deben ser verdaderas (`true` y estatura mayor o igual a 120). Pasemos con el siguiente ejemplo."*

---

### [05:30 - 07:40] Parte 3: Bucles determinados con `for`
**[En pantalla: Se pasa al bloque del bucle for para la cuenta regresiva].**

**Locución:**
> "Ahora que ya sabemos tomar decisiones, pasemos a otra gran necesidad en programación: repetir instrucciones.
>
> Imagina que quieres imprimir una cuenta regresiva del 5 al 1 en la pantalla. Escribir cinco veces 'imprimir' sería poco práctico. Para eso existen los bucles, que nos permiten repetir bloques de código automáticamente.
>
> Cuando sabemos con anticipación cuántas veces queremos repetir una acción, usamos el bucle `for`.
>
> Así que programemos la cuenta regresiva para el lanzamiento de un cohete espacial:"

**[Acción en pantalla: Bucle for en el editor]:**
```java
for (int i = 5; i >= 1; i--) {
    System.out.println(i + "...");
}
System.out.println("Despegue con éxito");
```

**Locución:**
> "Como vemos aquí en el código, tenemos un bucle `for` del 5 al 1. En cada iteración se imprime el número y tres puntos. Luego de que se cumpla la iteración, el programa debe imprimir 'Despegue con éxito'. Para comprobar, ejecutaremos el programa.
>
> Como vemos, se imprime el número y los tres puntos. Hay que tener en cuenta que el número es `i`, que empieza en 5, evalúa la condición de que este sea mayor o igual a 1, y si cumple la condición, se le resta en una unidad.
>
> Así que como el número inicia en 5, se imprime el 5 y los tres puntos. Luego se le resta una unidad y se evalúa nuevamente. Así es como se imprime el 4, el 3, el 2 y cuando llega a 1, como el 1 sigue siendo mayor o igual que 1, pues se imprime el 1, pero se le resta 1, entonces quedaría `i = 0`.
>
> Cuando `i` queda igual a 0, se sale de la condición, rompiendo el bucle `for`. Entonces el sistema procederá a imprimir la siguiente instrucción, que vendría a ser 'Despegue con éxito'."

---

### [07:40 - 10:45] Parte 4: Bucles condicionales con `while`
**[En pantalla: Bloque del bucle while para la recarga del robot].**

**Locución:**
> "¿Y qué ocurre si no sabemos de antemano cuántas vueltas dará el bucle, sino que debe repetirse mientras una condición siga cumpliéndose? Para eso usamos el bucle `while`, que se traduce como 'mientras'.
>
> Pensemos en un robot explorador cuya batería inicia al 70% y queremos recargarla de 10 en 10 hasta alcanzar el 100%. El bucle `while` comprueba la condición antes de cada vuelta. Mientras la batería sea menor a 100, suma 10 y lo muestra en pantalla. En el momento en que llega a 100, la condición se vuelve falsa, el bucle termina y el programa continúa con la siguiente instrucción.
>
> Pasemos entonces al programa:"

**[Acción en pantalla: Bucle while en el editor]:**
```java
int bateria = 70;

while (bateria < 100) {
    bateria += 10;
    System.out.println("Cargando batería " + bateria + "%");
}
System.out.println("Batería completamente cargada al 100%");
```

**Locución:**
> "Inicia la batería al 70%. El `while` menciona que se debe cumplir que la batería sea menor a 100. Si la batería es menor a 100, se ejecuta toda la lógica: primero, se le agregan 10 unidades a la batería y luego se imprime 'Cargando batería', el valor de la batería y el porcentaje.
>
> Cuando la batería ya sea mayor a 100, entonces el `while` se rompe y se imprime la siguiente instrucción: 'Batería completamente cargada al 100%'.
>
> Procedemos entonces a ejecutar el programa para verificar su funcionamiento.
>
> Como podemos observar:
> 1. Primero imprime 'Cargando batería 80%'. Esto se debe a que la batería ingresa con un valor de 70, se le agregan 10 unidades y luego se imprime.
> 2. En la siguiente iteración, la batería ingresa como 80. 80 sigue siendo menor a 100, entonces se le suman 10 unidades y se imprime la batería al 90%.
> 3. Como 90 sigue siendo menor que 100, entonces a 90 se le agregan 10 unidades y se imprime 'Cargando batería 100%'.
> 4. Como 100 ya no es menor que 100, entonces se rompe el bucle `while` y el sistema imprime que la batería ha sido completamente cargada al 100%."

---

### [10:45 - 11:56] Parte 5: Recomendaciones fundamentales y Cierre
**[En pantalla: Diapositiva o panel de resumen visual con buenas prácticas].**

**Locución:**
> "Para finalizar, ten presente dos recomendaciones fundamentales para evitar errores habituales:
>
> 1. **Evita bucles infinitos:** En un bucle `while`, asegúrate siempre de modificar la variable que se evalúa en la condición. Si olvidamos aumentar la batería, la condición nunca dejará de cumplirse y el programa se quedará ejecutándose de por vida.
> 2. **El uso de llaves:** Aunque Java permite omitir llaves en sentencias de una sola línea, la mejor práctica recomendada es escribirlas siempre para que tu código sea claro, ordenado y fácil de mantener.
>
> ¡Así que buen trabajo! En esta sesión aprendiste lo que es un `if-else` y a automatizar tareas con `for` y con `while`."
