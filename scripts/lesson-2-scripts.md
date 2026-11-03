# Lección 2 - Variables y Tipos de Datos
## Guion de grabación y anotaciones de pantalla

**Duración estimada:** 8 minutos y 34 segundos.

**Público objetivo:** estudiantes de 12 a 17 años.

**Nivel:** principiante.

**Objetivo:** aprender a crear variables, reconocer sus tipos de datos y mostrar información en la consola utilizando Java.

---

# ESCENA 1. INTRODUCCIÓN

**Tiempo:** 00:03 - 00:19

**Narración:**

¡Hola chicos! Bienvenidos a una nueva lección de programación.

Hoy vamos a aprender algo muy interesante: ¿cómo guardar información utilizando Java?

Y no se preocupen si nunca han programado, porque vamos a aprender paso a paso con ejemplos muy fáciles.

**Anotaciones de pantalla:**

- Mostrar el título: "Lección 2 - Variables y Tipos de Datos".
- Utilizar una animación de entrada para el título.
- Mostrar una ilustración de cajas que representan información almacenada.
- Mantener una música de fondo suave durante la introducción.

---

# ESCENA 2. ¿QUÉ ES UNA VARIABLE?

**Tiempo:** 00:19 - 00:52

**Narración:**

Primeramente, ¿qué es una variable?

Imaginen que tenemos una caja donde podemos guardar cosas.

Una caja puede guardar nuestro nombre, otra nuestra edad y otra nuestro color favorito.

En programación, estas cajas se llaman variables.

Una variable es un espacio donde guardamos un dato para utilizarlo después.

Por ejemplo, si guardamos el número 10 en una caja llamada edad, podemos utilizar ese número cuando lo necesitemos.

**Anotaciones de pantalla:**

- Mostrar tres cajas animadas.
- Primera caja: Nombre.
- Segunda caja: Edad.
- Tercera caja: Color favorito.
- Mostrar el código:

```java
int edad = 10;
```

- Resaltar progresivamente `int`, `edad` y `10`.

---

# ESCENA 3. TIPOS DE DATOS EN JAVA

**Tiempo:** 00:52 - 01:57

**Narración:**

En Java existen diferentes tipos de datos.

Es como tener una caja especial para guardar diferentes cosas.

Una de ellas es int.

Int es un tipo de dato que permite guardar números enteros, es decir, números sin decimales.

Otro tipo es double, que sirve para guardar números con decimales.

También tenemos String, que sirve para guardar palabras, nombres o frases.

Y finalmente tenemos boolean, que solamente puede guardar dos valores: true o false, es decir, verdadero o falso.

Existen muchos otros tipos de datos, pero estos son algunos de los principales.

**Anotaciones de pantalla:**

Mostrar una tarjeta por cada tipo de dato:

```java
int edad = 10;
```

```java
double altura = 1.50;
```

```java
String nombre = "Sofia";
```

```java
boolean leGustaJugar = true;
```

- Añadir un ejemplo visual para cada tipo.
- Resaltar las palabras `int`, `double`, `String` y `boolean`.
- Mostrar las traducciones de `true` y `false`.

---

# ESCENA 4. CONSTRUYENDO NUESTRO PRIMER PROGRAMA

**Tiempo:** 01:57 - 03:17

**Narración:**

Muy bien, continuando.

Ahora que ya sabemos que no todas las cajas son iguales, vamos a realizar un pequeño programa.

Este programa nos ayudará a utilizar los cuatro tipos de datos principales.

Primero, escribimos nuestra clase llamada Main.

Dentro de ella colocamos el método principal main, que es donde comenzará a ejecutarse nuestro programa.

Ahora vamos a crear nuestra primera variable.

Utilizaremos String para guardar un nombre. En este caso, escribiremos Sofia.

Seguidamente, utilizaremos int para guardar la edad, porque representa un número entero.

Después, utilizaremos double para guardar la altura. Por ejemplo, 1.50.

Finalmente, utilizaremos boolean para indicar si a nuestra persona le gusta jugar.

En este caso, colocaremos true.

**Anotaciones de pantalla:**

- Abrir el editor online de Java.
- Mostrar el código progresivamente.
- Resaltar cada variable mientras se explica.
- No mostrar todo el código de golpe.
- Explicar brevemente la estructura de la clase Main y el método main.

**Código mostrado:**

```java
public class Main {
    public static void main(String[] args) {

        String nombre = "Sofia";
        int edad = 10;
        double altura = 1.50;
        boolean leGustaJugar = true;

    }
}
```

---

# ESCENA 5. MOSTRANDO LOS RESULTADOS EN LA CONSOLA

**Tiempo:** 03:17 - 05:28

**Narración:**

Ahora que ya tenemos nuestras variables, vamos a mostrar sus valores en la consola.

Para hacerlo, utilizamos una instrucción llamada System.out.println.

Primero mostramos el nombre.

Después mostramos la edad.

Continuamos mostrando la altura y finalmente indicamos si le gusta jugar.

Muy bien, ahora vamos a ejecutar nuestro programa.

Cuando termine de ejecutarse, observaremos los valores que establecimos.

En este caso, veremos el nombre Sofia, la edad 10, la altura 1.50 y el valor true.

Esto significa que sí le gusta jugar.

¡Excelente!

Acabamos de utilizar los cuatro tipos de datos principales en un mismo programa.

**Anotaciones de pantalla:**

Mostrar el siguiente código:

```java
public class Main {
    public static void main(String[] args) {

        String nombre = "Sofia";
        int edad = 10;
        double altura = 1.50;
        boolean leGustaJugar = true;

        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
        System.out.println("Altura: " + altura);
        System.out.println("¿Le gusta jugar?: " + leGustaJugar);
    }
}
```

- Resaltar cada instrucción `System.out.println()`.
- Ejecutar el programa.
- Mostrar el resultado de la consola.
- Resaltar cada valor cuando aparezca.

**Resultado esperado:**

```text
Nombre: Sofia
Edad: 10
Altura: 1.5
¿Le gusta jugar?: true
```

---

# ESCENA 6. ACTIVIDAD: CREA UN PROGRAMA SOBRE TI

**Tiempo:** 05:39 - 08:23

**Narración:**

Ahora les toca a ustedes.

Imaginen que van a crear un pequeño programa sobre ustedes mismos.

¿Qué variables necesitarían para guardar su nombre, edad y color favorito?

Les voy a mostrar un ejemplo.

Primero utilizaremos String para guardar nuestro nombre, porque es un texto.

Después utilizaremos int para guardar nuestra edad. Por ejemplo, podemos colocar 9.

Finalmente, crearemos otra variable String para guardar nuestro color favorito.

En este ejemplo, vamos a utilizar el color verde.

Ahora debemos mostrar nuestros resultados utilizando System.out.println.

Recuerden que si solamente creamos las variables, pero no mostramos sus valores, no aparecerán en la consola.

Por eso, vamos a escribir las instrucciones para mostrar nuestro nombre, edad y color favorito.

Ahora ejecutamos nuevamente el programa y observamos el resultado.

En este ejemplo veremos:

Nombre: Sofia.

Edad: 9.

Color favorito: Verde.

¡Muy bien!

Ahora es su turno.

Cambien los ejemplos por sus propios datos, ejecuten el programa y comprueben sus resultados.

**Anotaciones de pantalla:**

Mostrar el código del segundo ejemplo:

```java
public class Main {
    public static void main(String[] args) {

        String nombre = "Sofia";
        int edad = 9;
        String colorFavorito = "Verde";

        System.out.println("Mi nombre es: " + nombre);
        System.out.println("Mi edad es: " + edad);
        System.out.println("Mi color favorito es: " + colorFavorito);
    }
}
```

**Resultado esperado:**

```text
Mi nombre es: Sofia
Mi edad es: 9
Mi color favorito es: Verde
```

**Actividad para los estudiantes:**

- Hacer una pausa para que los estudiantes intenten resolver el ejercicio.
- Mostrar un mensaje: "¡Es tu turno! Escribe tus propios datos".
- Permitir que los estudiantes cambien los valores.
- Mostrar una animación de verificación al ejecutar correctamente.

---

# ESCENA 7. DESPEDIDA

**Tiempo:** 08:23 - 08:34

**Narración:**

Y bueno, eso sería todo por esta lección.

Gracias por acompañarme.

Nos vemos en la próxima clase para seguir aprendiendo Java.

**Anotaciones de pantalla:**

- Mostrar el mensaje: "¡Excelente trabajo!".
- Añadir el texto: "Lección 2 completada".
- Mostrar una transición hacia la siguiente lección.
- Finalizar la música suavemente.

---

# RESUMEN DE LA LECCIÓN

| Concepto | Aprendizaje |
|---|---|
| Variable | Permite guardar información. |
| int | Guarda números enteros. |
| double | Guarda números decimales. |
| String | Guarda textos. |
| boolean | Guarda true o false. |
| System.out.println() | Muestra información en la consola. |

**Resultado esperado:** el estudiante debe poder crear variables, asignarles valores y mostrar su información mediante un programa sencillo en Java.