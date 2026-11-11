# Clase 1 - ¿Qué es Java y la Programación? (Starter)

Este documento sirve como guía práctica y contiene la plantilla de código inicial que los estudiantes utilizarán durante la clase 1. El objetivo es escribir y ejecutar su primer programa en Java, sin necesidad de instalar herramientas.

---

## 🎯 Objetivo de la Lección

1. **Programación:** Comprender que un programa es un conjunto ordenado de instrucciones que una computadora ejecuta para realizar tareas.
2. **Introducción a Java:** Reconocer que Java es un lenguaje de programación orientado a objetos y multiplataforma.
3. **Estructura básica:** Identificar la clase `Main`, el método `main` y la instrucción `System.out.println()`.
4. **Primera ejecución:** Completar y ejecutar el programa "Hola, mundo" en un editor en línea.

---

## Conceptos Clave

### 1. ¿Qué es la programación?

Programar significa escribir instrucciones claras para que una computadora realice una tarea. Por ejemplo, mostrar un mensaje, hacer un cálculo o responder a una acción del usuario.

### 2. ¿Qué es Java?

Java es un lenguaje de programación creado en 1995. Se utiliza para desarrollar aplicaciones, sistemas empresariales y servicios web, entre otros proyectos. Gracias a la **Máquina Virtual de Java (JVM)**, muchos programas Java pueden ejecutarse en distintos sistemas operativos.

### 3. ¿Cómo se organiza un programa básico en Java?

- **`public class Main`:** Define la clase principal del ejemplo.
- **`public static void main(String[] args)`:** Es el punto de entrada desde el que empieza la ejecución del programa.
- **`System.out.println(...)`:** Muestra un mensaje en la consola y agrega un salto de línea.
- **`{ }`:** Agrupan las instrucciones de una clase o un método.
- **`;`:** Indica el final de una instrucción, como la llamada a `println`.

---

## 💻 Código Inicial (Starter)

Copia la siguiente plantilla en **[OnlineGDB](https://onlinegdb.com/hOQLbUZNL)**, Replit o JDoodle. Completa los espacios marcados como **TODO** antes de ejecutarla.

> En OnlineGDB, asegúrate de seleccionar el lenguaje **Java**. Si trabajas con un archivo local, utiliza el nombre `Main.java`.

```java
// =============================================================================
// LECCIÓN 1: MI PRIMER PROGRAMA EN JAVA
// =============================================================================

// TODO 1: Completa el nombre de la clase principal (Main)
public class ______ {

    // TODO 2: Completa el nombre del método principal (main)
    public static void ______(String[] args) {

        // TODO 3: Usa System.out.println para mostrar "Hola, mundo!"
        // Escribe tu instrucción aquí:

    }
}
```

**Pista:** La instrucción para mostrar texto empieza con `System.out.println(`. Recuerda usar comillas dobles para el mensaje y terminar la instrucción con punto y coma.

---

## 🖥️ Salida Esperada

Cuando completes correctamente los tres TODO y presiones **Run / Ejecutar**, la consola deberá mostrar:

```text
Hola, mundo!
```

Si aparece un error de compilación, revisa que hayas escrito bien los nombres de la clase y del método, que el texto esté entre comillas y que la instrucción finalice con `;`.

---

## 🧩 Actividad Guiada Paso a Paso

1. **Completa el nombre de la clase** con `Main`.
2. **Completa el nombre del método de entrada** con `main`.
3. **Escribe la instrucción** necesaria para imprimir `Hola, mundo!`.
4. **Ejecuta el programa** y verifica que la salida coincida con el resultado esperado.
5. **Modifica el mensaje** para mostrar tu nombre y vuelve a ejecutar.

Puedes comparar tu resultado con el archivo **`Leccion1Completed.md`** de la carpeta `completed-examples` después de intentar resolver la actividad.

---

## 🚀 Retos para el Estudiante

1. Cambia el mensaje inicial por `Hola, soy [tu nombre]`.
2. Agrega una segunda instrucción que muestre `Estoy aprendiendo Java` en otra línea.
3. Experimenta con `System.out.print()` en lugar de `System.out.println()` e identifica la diferencia en la salida.

---

## 📚 Recursos de la Lección

- **Video:** [Lección 1 - ¿Qué es Java y la Programación?](https://youtu.be/e-CJTcVVT5Y)
- **Práctica en línea:** [OnlineGDB - Hola, mundo](https://onlinegdb.com/hOQLbUZNL)
- **Solución explicada:** `completed-examples/Leccion1Completed.md`

**Recuerda:** Esta es la versión *Starter*, por lo que el código está incompleto intencionalmente. La solución final se encuentra en la versión *Completed*.
