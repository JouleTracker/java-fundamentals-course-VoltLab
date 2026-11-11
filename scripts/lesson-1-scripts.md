# Guion de Video - Lección 1: ¿Qué es Java y la Programación?

* **Duración estimada:** 5 minutos (3 minutos de teoría y 2 minutos de demostración práctica).
* **Público objetivo:** Estudiantes de secundaria (12 a 17 años) sin conocimientos previos de programación.
* **Herramienta demostrada:** Editor en línea **OnlineGDB**, desde el navegador.
* **Regla de estilo:** No mencionar nombres propios de integrantes ni marcas de equipo. Utilizar explicaciones sencillas, ejemplos cotidianos y terminología correcta de programación. La primera parte se apoya en tres diapositivas; la segunda muestra el código en pantalla.

---

## Estructura y Cronograma del Video

| Minuto | Sección | Acción visual / En pantalla |
|---|---|---|
| 00:00 - 01:00 | ¿Qué es la programación? | Diapositiva 1: definición, instrucciones y ejemplos cotidianos. |
| 01:00 - 02:00 | ¿Qué es Java? | Diapositiva 2: origen, orientación a objetos y JVM. |
| 02:00 - 03:00 | ¿Para qué se utiliza Java? | Diapositiva 3: sistemas empresariales, backend, aplicaciones y videojuegos. |
| 03:00 - 03:20 | Presentación del ejemplo | Abrir OnlineGDB y mostrar el programa «Hola, mundo». |
| 03:20 - 03:45 | Clase `Main` | Señalar la declaración de clase y sus llaves. |
| 03:45 - 04:15 | Método `main` | Señalar el punto de entrada del programa. |
| 04:15 - 04:40 | `System.out.println` | Explicar la impresión de texto en consola. |
| 04:40 - 05:00 | Ejecutar y cerrar | Pulsar **Run**, mostrar la salida y resumir. |

---

## Guion Detallado de Locución

### [00:00 - 01:00] Diapositiva 1: ¿Qué es la programación?

**[En pantalla: Primera diapositiva. Señalar la definición y los ejemplos de aplicaciones.]**

**Voz en off:**
> «¡Hola a todos! Bienvenidos a esta primera lección, en la que aprenderemos qué es la programación y conoceremos un lenguaje muy utilizado: Java.
>
> Para comenzar, programar significa escribir instrucciones que una computadora ejecuta para realizar tareas.
>
> Por ejemplo, cuando usamos una aplicación de mensajes, una página web o un videojuego, detrás existen programas que indican qué debe ocurrir cuando presionamos un botón o escribimos algo.
>
> Podemos compararlo con una receta de cocina: primero seguimos un paso, después otro y, al final, obtenemos un resultado. En programación, también necesitamos instrucciones claras y organizadas.
>
> Ahora veremos con qué lenguaje podemos escribir esas instrucciones».

---

### [01:00 - 02:00] Diapositiva 2: ¿Qué es Java?

**[En pantalla: Segunda diapositiva. Resaltar «1995», «orientado a objetos» y «multiplataforma».]**

**Voz en off:**
> «Java es un lenguaje de programación creado en 1995 por Sun Microsystems.
>
> Una de sus características es que está orientado a objetos. Esto quiere decir que podemos organizar un programa mediante clases y objetos. Más adelante aprenderemos a trabajar con ellos.
>
> Otra característica importante es que Java es multiplataforma. Un programa Java puede funcionar en distintos sistemas operativos, siempre que tenga el entorno adecuado para ejecutarlo.
>
> Esto es posible gracias a la máquina virtual de Java, conocida como JVM, que permite ejecutar el código compilado.
>
> Por estas razones, Java es una buena opción para aprender conceptos fundamentales de programación».

---

### [02:00 - 03:00] Diapositiva 3: ¿Para qué se utiliza Java?

**[En pantalla: Tercera diapositiva. Mostrar ejemplos de banca, desarrollo web y aplicaciones.]**

**Voz en off:**
> «Ahora que sabemos qué es Java, veamos dónde se utiliza.
>
> Java está presente en sistemas empresariales y bancarios, donde se necesita procesar información y ejecutar operaciones de forma confiable.
>
> También se utiliza en el desarrollo de aplicaciones web, especialmente en el backend, que es la parte que procesa datos y responde a las solicitudes de los usuarios.
>
> Además, Java se ha utilizado en aplicaciones Android y videojuegos, como Minecraft.
>
> En resumen, Java nos permite convertir instrucciones en soluciones útiles. Y para comprender cómo funciona, vamos a crear un ejemplo sencillo que mostrará un mensaje en la consola».

---

### [03:00 - 03:20] Demostración: Presentación del programa

**[En pantalla: Abrir la práctica en [OnlineGDB](https://onlinegdb.com/hOQLbUZNL). Mostrar el archivo `Main.java` y aumentar el tamaño de fuente si es necesario.]**

**Voz en off:**
> «Ahora vamos a pasar a la parte práctica. Este es nuestro primer programa en Java. Su objetivo es mostrar el mensaje “Hola, mundo” en la consola.
>
> Aunque el código es corto, contiene elementos fundamentales que encontraremos en otros programas».

**[Código en pantalla:]**

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hola, mundo!");
    }
}
```

---

### [03:20 - 03:45] Primera línea: `public class Main`

**[En pantalla: Señalar `public class Main` y las llaves que delimitan su contenido.]**

**Voz en off:**
> «La primera línea dice `public class Main`. Aquí definimos una clase llamada `Main`.
>
> Las clases nos permiten organizar el código de Java. En este ejemplo, la clase contiene las instrucciones de nuestro programa. Las llaves indican dónde empieza y termina su contenido».

---

### [03:45 - 04:15] Segunda línea: `public static void main(String[] args)`

**[En pantalla: Señalar el encabezado del método `main` y sus llaves.]**

**Voz en off:**
> «Después encontramos `public static void main(String[] args)`.
>
> Este es el método principal del programa: cuando ejecutamos esta aplicación, Java comienza por aquí.
>
> Aunque la instrucción parezca larga, por ahora lo importante es recordar que `main` marca el punto de entrada y que dentro de sus llaves colocamos las instrucciones que queremos ejecutar».

---

### [04:15 - 04:40] Tercera línea: `System.out.println`

**[En pantalla: Resaltar `System.out.println("Hola, mundo!");` y luego el texto entre comillas.]**

**Voz en off:**
> «Por último, tenemos `System.out.println("Hola, mundo!");`.
>
> Esta instrucción imprime un mensaje en la consola. El texto que aparece entre comillas es exactamente el que queremos mostrar.
>
> Si cambiamos ese texto, el resultado también cambiará. El punto y coma indica el final de la instrucción».

---

### [04:40 - 05:00] Ejecución y cierre

**[En pantalla: Pulsar **Run**. Mostrar la salida y mantenerla visible durante el cierre.]**

**Salida esperada:**

```text
Hola, mundo!
```

**Voz en off:**
> «Vamos a ejecutar el programa. Como podemos observar, la consola muestra “Hola, mundo”.
>
> Con este ejemplo aprendimos la estructura básica de una clase, el método principal y cómo imprimir mensajes.
>
> ¡Eso es todo por esta primera lección! En la siguiente aprenderemos a guardar información mediante variables».

---

## 📌 Recomendaciones de Grabación

1. Utilizar las **tres diapositivas teóricas** únicamente durante los primeros tres minutos.
2. Mostrar el editor y señalar cada línea con el cursor durante los dos minutos finales.
3. Ejecutar el programa al terminar la explicación y comprobar que aparezca `Hola, mundo!`.
4. Evitar leer el código carácter por carácter: explicar la función general de cada instrucción.
5. Ensayar el texto y ajustar las pausas para mantener una duración cercana a los cinco minutos.

## 🔗 Recursos de la Lección

- **Video:** https://youtu.be/e-CJTcVVT5Y
- **Práctica en OnlineGDB:** https://onlinegdb.com/hOQLbUZNL
- **Solución documentada:** [`../completed-examples/Leccion1Completed.md`](../completed-examples/Leccion1Completed.md)
