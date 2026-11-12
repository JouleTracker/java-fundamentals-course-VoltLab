# Guion de Video - Lección 4: Métodos, Entrada/Salida e Introducción a la POO

* **Duración estimada:** ~10 a 12 minutos (Rango permitido: 5 a 15 minutos).
* **Público objetivo:** Estudiantes de secundaria (12 a 17 años) sin conocimientos previos de programación.
* **Herramienta demostrada:** Editor en línea (OnlineGDB / Replit).
* **Regla de estilo:** Cero mención a nombres propios, integrantes o marcas de equipo. Demostración práctica fluida en pantalla, paso a paso, lenguaje cercano y dinámico, cumpliendo con la terminología formal de ingeniería de software.

---

## Estructura y Cronograma del Video

| Minuto | Sección | Acción visual / En pantalla |
|---|---|---|
| 00:00 - 01:15 | Introducción a la lección | Diapositiva introductoria: ¿Por qué necesitamos organizar el código y crear objetos? |
| 01:15 - 04:00 | Métodos reutilizables y parámetros | Editor en línea: creación del método `saludar` (`void`) y `calcularEdadMascota` (`return`). |
| 04:00 - 06:30 | Entrada de datos interactiva con `Scanner` | Demostración de importación de `java.util.Scanner` desde la biblioteca estándar y lectura en consola. |
| 06:30 - 09:45 | Introducción a la POO: Clases y Objetos | Creación de la clase `Mascota`, constructor, atributos y métodos de comportamiento (`mostrarEstado`, `jugar`). |
| 09:45 - 11:30 | Instanciación con `new` y prueba completa | Creación del objeto `miMascota`, interacción por consola y ejecución en vivo de los comportamientos. |
| 11:30 - 12:15 | Resumen, buenas prácticas y cierre | Panel visual recapitulativo y transición hacia la siguiente lección. |

---

## Guion Detallado de Locución

### [00:00 - 01:15] Introducción: De programas simples a programas organizados
**[En pantalla: Diapositiva conceptual ilustrando una receta de cocina y un plano de construcción de casas].**

**Voz en off:**
> "¡Hola a todos! Bienvenidos a la lección número 4 de nuestro curso de Java para principiantes.
>
> Hasta ahora hemos escrito todo nuestro código dentro de una sola sección principal llamada `main`. Pero a medida que nuestros programas crecen, escribir cientos de líneas en un solo lugar puede volverse desordenado y difícil de entender.
>
> Hoy daremos dos de los saltos más importantes en la vida de un programador:
> Primero, aprenderemos a crear **métodos**, que son como pequeñas recetas o funciones reutilizables que podemos llamar cuando las necesitemos.
> Segundo, descubriremos cómo hacer que nuestro programa sea interactivo pidiéndole datos al usuario a través del teclado con la herramienta **Scanner**.
> Y finalmente, entraremos al fascinante mundo de la **Programación Orientada a Objetos**, aprendiendo qué son las clases y cómo crear nuestros propios objetos en Java. ¡Acompáñame al editor de código!"

---

### [01:15 - 04:00] Parte 1: Métodos con parámetros y retorno
**[En pantalla: Se abre el navegador web en el editor OnlineGDB mostrando la plantilla básica con letra amplia y clara].**

**Voz en off:**
> "Un **método** es un bloque de código diseñado para realizar una tarea específica. Piensa en el botón de encendido de un control remoto: presionas el botón y adentro se ejecuta toda la acción sin que tengas que volver a construir los cables cada vez.
>
> Vamos a escribir nuestro primer método justo fuera del `main`:"

**[Acción en pantalla: Escribir el método saludar]:**
```java
public static void saludar(String nombreUsuario) {
    System.out.println("¡Hola, " + nombreUsuario + "! Bienvenido al Creador de Mascotas.");
}
```

**Voz en off:**
> "Analicemos las partes de esta línea:
> `void` significa que el método solo ejecuta una acción y no devuelve ningún dato de vuelta.
> Dentro de los paréntesis tenemos un **parámetro**: `String nombreUsuario`. Esto es como una variable que recibe el dato que le enviemos desde donde lo llamemos.
>
> Ahora creemos un método que sí devuelva un resultado utilizando la palabra clave `return`:"

**[Acción en pantalla: Escribir el método calcularEdadMascota]:**
```java
public static int calcularEdadMascota(int edadHumanos) {
    return edadHumanos * 7;
}
```

**Voz en off:**
> "Observa que aquí reemplazamos `void` por `int`, porque este método se compromete a devolvernos un número entero.
>
> Si en el método principal `main` llamamos a `saludar("Explorador")` y luego a `calcularEdadMascota(2)`, Java ejecuta esas instrucciones y nos entrega el resultado calculado de manera limpia y ordenada."

---

### [04:00 - 06:30] Parte 2: Entrada de datos interactiva con `Scanner`
**[En pantalla: Se agrega la línea de importación al inicio del archivo].**

**Voz en off:**
> "Hasta ahora, todos los valores en nuestras variables estaban fijos en el código. Pero en una aplicación real, queremos que el usuario escriba su información en la pantalla.
>
> Para lograrlo, Java nos brinda una herramienta llamada `Scanner`, que forma parte de la biblioteca estándar del lenguaje.
>
> Para usarla, primero agregamos en la primera línea de nuestro archivo la instrucción de importación:"

**[Acción en pantalla: Escribir import java.util.Scanner; y crear el objeto Scanner en main]:**
```java
import java.util.Scanner;

// Dentro de main:
Scanner scanner = new Scanner(System.in);

System.out.print("Escribe el nombre de tu mascota: ");
String nombre = scanner.nextLine();

System.out.print("Escribe la especie (ej. Perro, Gato, Robot): ");
String especie = scanner.nextLine();
```

**Voz en off:**
> "`System.in` le indica a Java que queremos capturar lo que el usuario escriba en la consola a través del teclado.
> Y con `scanner.nextLine()`, el programa se detiene amablemente a esperar que el usuario escriba un texto y presione la tecla Enter. ¡Ahora nuestro programa es totalmente interactivo!"

---

### [06:30 - 09:45] Parte 3: Introducción a la POO: Clases y Objetos
**[En pantalla: Se ilustra la analogía: Molde de galletas (Clase) vs. Galletas horneadas (Objetos)].**

**Voz en off:**
> "Ahora llegamos al corazón del desarrollo de software moderno: la **Programación Orientada a Objetos**, conocida como **POO**.
>
> En el mundo real, todo lo que nos rodea son objetos: un auto, una guitarra, un teléfono o una mascota. Cada objeto tiene **características** (como su color, tamaño o nombre) y **comportamientos** (lo que puede hacer: avanzar, sonar, jugar o dormir).
>
> En Java:
> Una **Clase** es el plano o molde de galletas.
> Un **Objeto** es la galleta horneada concreta que creamos con ese molde.
>
> Vamos a definir la clase `Mascota`:"

**[Acción en pantalla: Escribir la clase Mascota]:**
```java
class Mascota {
    String nombre;
    String especie;
    int energia;

    public Mascota(String nombre, String especie, int energia) {
        this.nombre = nombre;
        this.especie = especie;
        this.energia = energia;
    }

    public void mostrarEstado() {
        System.out.println("\n--- FICHA DE LA MASCOTA ---");
        System.out.println("Nombre: " + this.nombre);
        System.out.println("Especie: " + this.especie);
        System.out.println("Energia: " + this.energia + "/100");
    }

    public void jugar(int minutos) {
        System.out.println("\n" + this.nombre + " esta jugando por " + minutos + " minutos...");
        this.energia -= (minutos * 2);
        if (this.energia < 0) {
            this.energia = 0;
        }
        System.out.println("Energia restante: " + this.energia + "/100");
    }
}
```

**Voz en off:**
> "Fíjate en esta estructura:
> `nombre`, `especie` y `energia` son los **atributos**.
> El método que se llama exactamente igual que la clase, `public Mascota(...)`, es el **constructor**: su misión es darle vida inicial a la mascota con los datos que le pasemos. Usamos la palabra clave `this` para indicarle a Java que nos referimos al atributo propio de esta mascota en particular.
> Y luego definimos dos métodos: `mostrarEstado()` para ver su ficha y `jugar()` para interactuar y gastar energía."

---

### [09:45 - 11:30] Parte 4: Instanciación con `new` y Ejecución en Vivo
**[En pantalla: Dentro de main, se unen todas las piezas creadas y se presiona Ejecutar].**

**Voz en off:**
> "Ahora conectemos todo en el método principal `main`.
>
> Con los datos que el usuario ingresó por consola mediante `Scanner`, creamos un nuevo objeto en memoria utilizando la palabra clave `new`:"

**[Acción en pantalla: Escribir en main]:**
```java
Mascota miMascota = new Mascota(nombre, especie, 100);

miMascota.mostrarEstado();
miMascota.jugar(15);

scanner.close();
```

**Voz en off:**
> "Presionamos el botón verde de 'Ejecutar'.
>
> En la consola nos pide: 'Escribe el nombre de tu mascota:'. Escribimos: *Pixel*.
> Luego nos solicita la especie: escribimos *Perro Robot*.
> Presionamos Enter y... ¡observa la magia!
> Se crea el objeto en memoria, se imprime su ficha completa con 100 de energía y luego, al llamar a `miMascota.jugar(15)`, vemos cómo juega por 15 minutos y su energía disminuye a 70.
>
> Lo más fascinante es que podríamos crear dos, tres o cien mascotas distintas usando el mismo molde, y cada una tendrá sus propios datos independientes."

---

### [11:30 - 12:15] Resumen y Cierre
**[En pantalla: Panel con las 3 conclusiones clave de la lección].**

**Voz en off:**
> "Hagamos un repaso rápido de lo aprendido hoy:
> 1. Los **métodos** nos permiten escribir código reutilizable y ordenado, aceptando parámetros y devolviendo resultados con `return`.
> 2. Con la clase `Scanner` de la biblioteca estándar de Java podemos interactuar con el usuario a través de la consola.
> 3. En la **Programación Orientada a Objetos**, una clase define la estructura general con atributos y métodos, y usamos `new` para crear objetos reales e independientes.
>
> En el repositorio del curso encontrarás tanto la plantilla con ejercicios para practicar como el código resuelto completo.
>
> En la próxima lección profundizaremos en el encapsulamiento con getters y setters y construiremos un proyecto completo basado en POO.
>
> ¡Muchas gracias por acompañarnos y nos vemos en la siguiente lección!"
