# Guion de Video - Lección 6: Consejos y próximos pasos

* **Duración real del video:** 10:25 minutos (Rango permitido: 5 a 15 minutos).
* **Público objetivo:** Estudiantes de secundaria (12 a 17 años) sin conocimientos previos de programación.
* **Herramienta demostrada:** Editor en línea (OnlineGDB - Java).
* **Enlace del video:** [Ver Lección 6](https://youtu.be/gHEnulUZS9Q)
* **Regla de estilo:** Cero mención a nombres propios, integrantes o marcas de equipo. Transcripción fiel y estructurada de la explicación paso a paso en pantalla, lenguaje cercano y didáctico, cumpliendo con la terminología formal de ingeniería de software.

---

## Estructura y Cronograma del Video

| Minuto | Sección | Acción visual / En pantalla |
|---|---|---|
| 00:00 - 00:48 | Introducción y cierre del curso | Bienvenida a la sexta y última lección; repaso de pilares aprendidos (variables, condicionales, bucles, métodos y POO). |
| 00:48 - 02:44 | Editores en línea vs. entornos locales (IDE) | Editor OnlineGDB con `Main.java` (`Language: Java`), explicación del compilador al presionar **Run** (`F9`), consola de salida y mención a IntelliJ IDEA / Visual Studio Code. |
| 02:44 - 04:31 | Reglas de oro para escribir código limpio | Demostración en `Main.java`: nombres descriptivos con `camelCase` (`nombreJugador`, `puntuacionMaxima`), sangría / tabulación y comentarios con `//`. |
| 04:31 - 06:50 | Errores comunes en consola y depuración | Simulación en vivo en OnlineGDB de 3 errores (`; expected`, `package system does not exist` por mayúsculas/minúsculas y `reached end of file while parsing` por llave sin cerrar) y el "truco del detective" con `System.out.println`. |
| 06:50 - 07:54 | Dónde continuar aprendiendo Java | Recomendación de documentación oficial de Oracle Java (métodos de `String`), W3Schools, Exercism y minijuegos de consola. |
| 07:54 - 09:33 | Actitud y estrategia ante errores | Tres consejos clave: dividir el problema en pasos pequeños, buscar mensajes de error en Stack Overflow y aplicar la regla del descanso. |
| 09:33 - 10:25 | Reto final y despedida | Propuesta de miniproyectos en OnlineGDB (adivinar número secreto, mini trivia o ampliar clases POO) y cierre del curso. |

---

## Guion Detallado de Locución

### [00:00 - 00:48] Introducción a la última lección del curso
**[En pantalla: Entorno OnlineGDB con Java listo para trabajar.]**

**Voz en off:**
> "Hola a todos y bienvenidos a la sexta y última lección de este curso de fundamentos de Java para principiantes.
>
> Primero que nada, muchas felicidades por llegar hasta aquí. A lo largo de las lecciones anteriores aprendieron los pilares de la programación: variables, condicionales, bucles, métodos y conceptos básicos de la programación orientada a objetos.
>
> En esta lección final no vamos a complicarnos con conceptos nuevos y pesados. Voy a ser su guía para darles los mejores consejos que usan los programadores profesionales: cómo escribir código limpio, cómo entender los errores que salen en la pantalla sin frustrarse, dónde seguir aprendiendo por su cuenta y cómo consolidar su proyecto final. Empecemos."

---

### [00:48 - 02:44] Editores en línea vs. Entornos de Desarrollo (IDE)
**[Acción en pantalla: OnlineGDB con el archivo `Main.java`, el ejemplo `nombreJugador = "Alex"` y `puntuacionMaxima = 100`, ejecutando con el botón verde `Run` y mostrando la salida en consola inferior.]**

**Voz en off:**
> "Antes de entrar directamente a modificar código, es clave entender dónde estamos parados y qué herramientas necesitamos. A lo largo de este curso estuvimos utilizando editores en línea como OnlineGDB.
>
> La gran ventaja para quienes recién empiezan en secundaria es que no necesitan configurar variables de entorno, ni instalar el JDK, ni preocuparse por qué sistema operativo tienen. Abren la pestaña en su navegador y tienen un compilador de Java funcionando al instante.
>
> Básicamente, presionamos `F9` o hacemos clic en **Run** y el código empieza a compilar. Fíjense en dos partes principales de la pantalla: arriba tenemos nuestro editor, donde escribimos las instrucciones para la computadora; y al presionar **Run**, entra en acción el compilador de Java. El compilador revisa que no tenga ninguna falta de ortografía o de sintaxis, traduce nuestro código a lenguaje de máquina y nos muestra el resultado final aquí abajo, en la consola de salida.
>
> Cuando más adelante decidan dar el paso hacia proyectos más grandes y profesionales, usarán entornos de desarrollo más completos en su computadora, conocidos como IDE, por ejemplo IntelliJ IDEA o Visual Studio Code. Pero las reglas básicas de cómo funciona Java son exactamente las mismas que estamos viendo aquí."

---

### [02:44 - 04:31] Tres reglas de oro para escribir código limpio
**[Acción en pantalla: Resaltado en el editor de `String nombreJugador = "Alex";`, `int puntuacionMaxima = 100;`, sangría dentro de `main` y comentario `// Lección 6: Buenas prácticas`.]**

**Voz en off:**
> "Teniendo en claro cómo funciona nuestro entorno de trabajo, pasemos ahora sí a las reglas de oro para escribir un código impecable.
>
> Un consejo fundamental para todo programador es escribir código limpio. Cuando empezamos, creemos que que el programa funcione es suficiente; pero la realidad es que el código se lee muchas más veces de las que se escribe.
>
> Veamos el **primer punto: los nombres de las variables**. Miren este ejemplo en pantalla: `String nombreJugador = "Alex";`. Si yo le hubiera puesto simplemente `x` o `n`, cuando el programa tenga 200 líneas nadie sabrá qué guarda esa variable. Usen nombres descriptivos. Además, en Java usamos la convención llamada **camelCase**: la primera palabra empieza con minúscula y cada palabra que sigue empieza con mayúscula, como `nombreJugador` o `puntuacionMaxima`.
>
> El **segundo punto es la sangría o tabulación**. Fíjense cómo dentro de la clase y del método `main`, las líneas de código tienen un espacio hacia la derecha. Si todo estuviera pegado al margen izquierdo, sería muy difícil saber dónde empieza y dónde termina cada bloque. La tabulación es el orden de tu código.
>
> Y el **tercer punto son los comentarios**. Usando la doble barra inclinada (`//`), podemos dejar notas breves para recordar por qué escribimos cierta lógica, ayudándonos a nosotros mismos en el futuro o a otros compañeros que lean nuestro proyecto."

---

### [04:31 - 06:50] Errores comunes en consola y cómo depurar
**[Acción en pantalla: En `Main.java`, eliminación intencional del `;`, cambio de `System` a `system` minúscula para provocar errores rojos en consola, eliminación de una llave `}` de cierre y corrección paso a paso.]**

**Voz en off:**
> "Ahora hablemos de lo que más inquieta a los principiantes: los errores en consola. Cuando ven letras rojas en la pantalla, muchos piensan: 'esto no es para mí' o 'hice todo mal'. Pero un error no significa que seas mal programador; los programadores profesionales ven errores todo el día. El truco es aprender a leerlos.
>
> Veamos el **error número uno: olvidar el punto y coma (`;`)** al final de una instrucción. Miren la consola: Java nos dice exactamente el error (`';' expected`) y nos indica la línea donde falta. Ponemos el punto y coma de nuevo, ejecutamos y ya funciona.
>
> El **segundo error común: mayúsculas y minúsculas**. Java es un lenguaje que distingue estrictamente entre mayúsculas y minúsculas. Si escribo `system.out.println` con `s` minúscula o `string` con `s` minúscula, nos va a salir un error en consola (`error: package system does not exist`). Recuerden que las clases como `String` y `System` siempre inician con letra mayúscula. Lo corregimos y vuelve a funcionar.
>
> El **tercer error: llaves abiertas o sin cerrar**. Si quitamos esta llave de cierre y ejecutamos, aparece otro error (`reached end of file while parsing`). El truco aquí es hacer clic junto a una llave en el editor para ver cuál es su pareja; así detectamos rápidamente dónde falta cerrar la llave, la colocamos y vuelve a compilar.
>
> ¿Y cómo depurar cuando el código **no** muestra errores de sintaxis, pero tampoco hace lo que queremos? Aplicamos el **truco del detective**: coloquen mensajes en pantalla con `System.out.println` (por ejemplo, 'Paso por aquí' o '[DEBUG]') para comprobar en la consola si el programa realmente está entrando a un `if` o a un bucle."

---

### [06:50 - 07:54] Recursos para seguir aprendiendo por tu cuenta
**[En pantalla: Editor OnlineGDB como referencia mientras se mencionan plataformas y documentación.]**

**Voz en off:**
> "Una vez terminado este curso introductorio, la gran pregunta es: ¿dónde continúo?
>
> Lo primero que deben conocer es la **documentación oficial de Oracle Java**. Esta página es como la enciclopedia oficial del lenguaje. Aquí no tienen que memorizar nada: si quieren saber qué funciones tiene el texto en Java, buscan la clase `String` y verán sus métodos, como `length`, `toUpperCase` o `contains`, con explicaciones de cómo utilizarlos.
>
> Además de la documentación oficial, existen sitios interactivos y gratuitos como **W3Schools** de Java o **Exercism**, donde pueden practicar resolviendo pequeños acertijos de código. Mi recomendación personal es que intenten crear minijuegos por consola: un juego de adivinar números secretos con `Scanner` y bucles, o un juego de preguntas y respuestas; es una forma muy divertida de dominar la programación."

---

### [07:54 - 09:33] Mentalidad del programador frente a la frustración
**[En pantalla: Código Java limpio en OnlineGDB.]**

**Voz en off:**
> "Antes de despedirnos, quiero dejarles un último grupo de consejos muy importante que no tiene que ver con la sintaxis del código, sino con la actitud de un programador para no frustrarse cuando algo no sale:
>
> **Primero, divide los problemas en pedazos pequeños.** Si quieres crear un videojuego, no intentes hacer todo de golpe. Empieza logrando que imprima un mensaje; cuando eso funcione, agrégale una variable; cuando esa variable funcione, ponle un `if`; y paso a paso irás construyendo cualquier programa que desees.
>
> **Segundo, aprende a buscar ayuda.** Cuando te salga un error raro que no entiendas, no te quedes bloqueado durante horas. Copia el mensaje de error de la consola y búscalo en internet o en foros como **Stack Overflow**. El 99 % de las veces a otro programador ya le ocurrió exactamente el mismo problema y dejó una solución explicada.
>
> **Y tercero, la regla del descanso.** Si llevas 20 minutos mirando la pantalla y no encuentras cómo resolver una falla, aléjate del teclado, toma un vaso de agua y camina 5 minutos. La mayoría de las veces, cuando regreses, tu mente estará fresca y verás la solución casi al instante. Recuerda que programar es como aprender a tocar un instrumento o practicar un deporte: se mejora con la práctica diaria."

---

### [09:33 - 10:25] Reto final y cierre del curso
**[En pantalla: Editor en línea `onlinegdb.com` con el programa ejecutado correctamente.]**

**Voz en off:**
> "Como reto final para ustedes, les recomiendo intentar crear pequeños proyectos por su cuenta aquí mismo en el editor en línea **OnlineGDB**:
> - Un juego para adivinar un número secreto entre el `1` y el `100` usando la consola y condicionales.
> - Una mini trivia de preguntas y respuestas con puntaje.
> - O expandir el proyecto de clases y objetos que vieron en las lecciones anteriores agregándole nuevos métodos y atributos.
>
> La mejor forma de afianzar lo que aprendieron es practicando y probando cosas nuevas. No tengan miedo de equivocarse, porque cada error resuelto es una lección aprendida. Muchísimas gracias por haber seguido nuestro curso de fundamentos de Java. ¡Muchos éxitos en sus futuros proyectos!"
