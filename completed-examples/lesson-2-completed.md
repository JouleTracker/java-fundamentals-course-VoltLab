# Lección 2 - Variables y Tipos de Datos (Solución y Código Terminado)

## 1. Objetivo de la solución

En esta lección aprendimos a utilizar variables para almacenar información en Java.

Ahora veremos el programa completo, con los cuatro tipos de datos principales:

- `String`
- `int`
- `double`
- `boolean`

## 2. Código final resuelto

```java
public class Main {
    public static void main(String[] args) {

        // Variable de tipo String
        String nombre = "Sofia";

        // Variable de tipo int
        int edad = 10;

        // Variable de tipo double
        double altura = 1.50;

        // Variable de tipo boolean
        boolean leGustaJugar = true;

        // Mostrar los resultados en la consola
        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
        System.out.println("Altura: " + altura);
        System.out.println("¿Le gusta jugar?: " + leGustaJugar);
    }
}
```

## 3. Resultado esperado en consola

Al ejecutar el programa, obtendremos el siguiente resultado:

```text
Nombre: Sofia
Edad: 10
Altura: 1.5
¿Le gusta jugar?: true
```

**Nota:** Java puede mostrar `1.50` como `1.5` al imprimir un valor `double`. Ambos representan el mismo valor numérico.

## 4. Explicación del código

### Variable String

```java
String nombre = "Sofia";
```

Utilizamos `String` porque queremos guardar un nombre, es decir, un texto.

### Variable int

```java
int edad = 10;
```

Utilizamos `int` porque la edad se representa mediante un número entero.

### Variable double

```java
double altura = 1.50;
```

Utilizamos `double` porque queremos guardar un número decimal.

### Variable boolean

```java
boolean leGustaJugar = true;
```

Utilizamos `boolean` porque queremos representar una respuesta de verdadero o falso.

En este caso, el valor `true` significa que sí le gusta jugar.

### Mostrar información

```java
System.out.println("Nombre: " + nombre);
```

Utilizamos `System.out.println()` para mostrar información en la consola.

El símbolo `+` permite unir un texto con el valor de una variable.

## 5. Segundo ejemplo: Programa personal

Ahora crearemos un programa que muestre el nombre, la edad y el color favorito de una persona.

### Código completo

```java
public class Main {
    public static void main(String[] args) {

        // Guardar el nombre
        String nombre = "Sofia";

        // Guardar la edad
        int edad = 9;

        // Guardar el color favorito
        String colorFavorito = "Verde";

        // Mostrar la información
        System.out.println("Mi nombre es: " + nombre);
        System.out.println("Mi edad es: " + edad);
        System.out.println("Mi color favorito es: " + colorFavorito);
    }
}
```

### Resultado esperado

```text
Mi nombre es: Sofia
Mi edad es: 9
Mi color favorito es: Verde
```

## 6. ¿Qué aprendimos?

En esta actividad aprendimos que:

1. Las variables permiten almacenar información.
2. Cada variable tiene un tipo de dato.
3. `String` permite guardar textos.
4. `int` permite guardar números enteros.
5. `double` permite guardar números decimales.
6. `boolean` permite guardar valores verdaderos o falsos.
7. `System.out.println()` permite mostrar los resultados.

## 7. Recomendaciones

- Utiliza nombres claros para tus variables.
- Recuerda que los textos deben escribirse entre comillas dobles.
- No olvides colocar el punto y coma `;` al finalizar cada instrucción.
- Respeta las mayúsculas y minúsculas en Java.
- Ejecuta tu programa para comprobar que funciona correctamente.

## 8. Actividad final

Modifica el segundo programa utilizando tus propios datos.

Puedes cambiar tu nombre, edad y color favorito.

¡Felicitaciones! Has completado la lección sobre variables y tipos de datos en Java.