# Clase 1 - ¿Qué es Java y la Programación? (Completed)

Este documento contiene la solución completa, explicada y comentada paso a paso de la lección 1. El objetivo es conocer la estructura básica de un programa Java y mostrar el mensaje **"Hola, mundo!"** en la consola.

---

## 🎯 Código Completo Resuelto

A continuación se presenta el código final, listo para ejecutarse en **OnlineGDB**, **Replit**, **JDoodle** o un entorno local.

Guarda el archivo como `Main.java` si lo ejecutas localmente:

```java
// =============================================================================
// LECCIÓN 1: INTRODUCCIÓN A JAVA - PRIMER PROGRAMA
// =============================================================================

// Definición de la clase principal: su nombre coincide con Main.java
public class Main {

    // Método principal: punto de entrada del programa
    public static void main(String[] args) {

        // Muestra un mensaje en la consola y luego salta de línea
        System.out.println("Hola, mundo!");
    }
}
```

---

## 🖥️ Demostración y Salida en Consola

Al ejecutar el programa, sin necesidad de ingresar datos, se obtiene:

```text
Hola, mundo!
```

**Práctica en línea:** [Abrir el ejemplo en OnlineGDB](https://onlinegdb.com/hOQLbUZNL)

**Video de la lección:** [Ver la explicación en YouTube](https://youtu.be/e-CJTcVVT5Y)

---

## 🔍 Explicación Técnica Paso a Paso

1. **Clase principal (`public class Main`):**
   - `class` define una clase, que permite organizar el código Java.
   - `Main` es el nombre de la clase. Como es `public`, en un archivo fuente local debe llamarse `Main.java`.
   - Las llaves `{ }` delimitan el contenido de la clase.

2. **Método principal (`public static void main(String[] args)`):**
   - Es el punto de entrada de esta aplicación Java.
   - `public` permite que el método sea accesible desde fuera de la clase.
   - `static` permite que Java lo ejecute sin crear primero un objeto `Main`.
   - `void` indica que no devuelve ningún valor.
   - `String[] args` permite recibir argumentos desde la línea de comandos, aunque en este ejemplo no se utilizan.

3. **Salida en consola (`System.out.println("Hola, mundo!");`):**
   - `System.out` representa la salida estándar del programa.
   - `println` imprime el texto y agrega un salto de línea al final.
   - Las comillas dobles delimitan el texto que se desea imprimir.
   - El punto y coma `;` marca el final de la instrucción.

4. **Comentarios (`//`):**
   - Permiten añadir explicaciones para las personas que leen el código.
   - No se ejecutan ni modifican la salida del programa.

---

## ✅ Actividad de Comprobación

Modifica el mensaje para que el programa muestre tu nombre:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hola, soy Rodrigo y estoy aprendiendo Java.");
    }
}
```

**Salida esperada:**

```text
Hola, soy Rodrigo y estoy aprendiendo Java.
```

Puedes reemplazar `Rodrigo` por tu propio nombre.

---

## 📌 Conclusiones Clave

- Programar consiste en escribir instrucciones para que una computadora realice tareas.
- Java es un lenguaje de programación que se utiliza en diversos tipos de aplicaciones.
- Una clase contiene el método `main`, desde el cual comienza este programa.
- `System.out.println()` permite mostrar mensajes en la consola.
- Con un cambio en el texto podemos personalizar la salida sin modificar la estructura del programa.
