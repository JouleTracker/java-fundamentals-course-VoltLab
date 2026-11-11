# Lección 1 - Mi primer programa en Java (Completed)

En esta primera clase vimos qué significa programar, para qué sirve Java y cómo ejecutar un programa sencillo. Aquí está el ejemplo que usamos en la práctica, con una explicación de lo que hace cada parte.

## Código de la clase

Para probarlo, abrimos [OnlineGDB](https://onlinegdb.com/hOQLbUZNL), seleccionamos Java y ejecutamos lo siguiente:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hola, mundo!");
    }
}
```

Al presionar **Run**, la consola muestra:

```text
Hola, mundo!
```

## ¿Cómo funciona?

Aunque son pocas líneas, hay algunas cosas importantes:

- **`public class Main`**: es la clase que contiene nuestro programa. En este caso se llama `Main`.
- **`public static void main(String[] args)`**: es el método principal, donde comienza la ejecución.
- **`System.out.println()`**: permite escribir un mensaje en la consola. Lo que está entre comillas es el texto que aparecerá.
- **Las llaves `{ }`**: indican dónde empieza y termina el contenido de la clase y del método.
- **El punto y coma `;`**: marca el final de la instrucción que imprime el mensaje.

Algo que notamos al ejecutar el código es que Java sigue exactamente las instrucciones que escribimos. Si cambiamos el mensaje, también cambia lo que aparece en la consola.

## Una pequeña modificación

Después de probar el “Hola, mundo”, podemos personalizarlo con nuestro nombre y agregar otra línea:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hola, soy Rodrigo.");
        System.out.println("Estoy aprendiendo Java.");
    }
}
```

La salida sería:

```text
Hola, soy Rodrigo.
Estoy aprendiendo Java.
```

Aquí usamos dos veces `println`, por eso cada mensaje aparece en una línea diferente.

## Lo que aprendimos

La programación consiste en darle instrucciones a una computadora para realizar una tarea. Java nos permite escribir esas instrucciones y ejecutarlas. Con este primer ejercicio aprendimos a reconocer la estructura básica de un programa y a mostrar texto en la consola.

Para seguir practicando, se puede cambiar el nombre, escribir un saludo diferente o agregar una tercera línea con otro mensaje.

**Video de la lección:** [¿Qué es Java y la programación?](https://youtu.be/e-CJTcVVT5Y)  
**Código en línea:** [Ejercicio en OnlineGDB](https://onlinegdb.com/hOQLbUZNL)
