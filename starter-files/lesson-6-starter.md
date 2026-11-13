# Lección 6: Consejos, Código Limpio y Depuración (Starter)

Bienvenido a la práctica de la **Lección 6**. Tu objetivo es tomar este código base —que contiene nombres de variables poco claros, falta de sangría y ausencia de mensajes de depuración— para limpiarlo siguiendo las mejores prácticas vistas en el video.

---

## 🎯 Objetivos de la Práctica
1. Aplicar la convención **`camelCase`** con nombres descriptivos (`nombreJugador`, `puntuacionMaxima`, `nivelActual`).
2. Ordenar la **sangría (tabulación)** y añadir comentarios breves con `//`.
3. Usar el **truco del detective** agregando mensajes `[DEBUG]` con `System.out.println` para verificar el flujo del programa.
4. Practicar la lectura de los 3 errores más frecuentes de Java en **OnlineGDB** (`; expected`, `package system does not exist` y `reached end of file while parsing`).

---

## 💻 Código Inicial (Plantilla para OnlineGDB)

Pega este código en la pestaña **`Main.java`** de **OnlineGDB** (`Language: Java`) y completa los retos:

```java
public class Main {
    public static void main(String[] args) {

        // RETO 1: Cambia estos nombres genéricos por nombres descriptivos usando camelCase
        // (ejemplo del video: nombreJugador, puntuacionMaxima, nivelActual)
        String n = "Alex";
        int p = 100;
        int lvl = 3;

        // RETO 2: Corrige la sangría (tabulación) de estas líneas y agrega comentarios explicativos con //
System.out.println("Jugador: " + n);
System.out.println("Puntaje: " + p);
System.out.println("Nivel actual: " + lvl);

        // RETO 3: Aplica el "truco del detective" agregando mensajes [DEBUG] antes y dentro del if/else
        if (p >= 100) {
            lvl++;
            System.out.println("Has subido al nivel: " + lvl);
        } else {
            System.out.println("Puntaje insuficiente para subir de nivel.");
        }

        // RETO 4: Recorre los recursos recomendados usando .length de forma segura
        String[] recursos = {
            "Documentacion oficial de Oracle Java",
            "Tutoriales interactivos en W3Schools",
            "Plataforma de ejercicios Exercism"
        };

        for (int i = 0; i < recursos.length; i++) {
            System.out.println((i + 1) + ". " + recursos[i]);
        }
    }
}
```

---

## 🛠️ Instrucciones de la Actividad
1. Renombra `n`, `p` y `lvl` a `nombreJugador`, `puntuacionMaxima` y `nivelActual` respetando la regla **camelCase**.
2. Alinea correctamente todas las líneas dentro de `main` usando 4 espacios de sangría.
3. Añade comentarios con `//` y mensajes de rastreo (`[DEBUG]`) para comprobar por consola qué camino toma el condicional `if-else`.
4. **Experimento de errores (opcional):** En OnlineGDB, prueba quitar temporalmente un `;`, escribir `system` en minúscula o borrar una llave `}` de cierre para aprender a identificar los mensajes de error del compilador antes de corregirlo.
5. **Desafío final:** Crea un nuevo proyecto en OnlineGDB eligiendo una de las ideas del video (adivinar número secreto entre 1 y 100, mini trivia con puntaje o ampliar la tienda de mascotas de la Lección 5).
