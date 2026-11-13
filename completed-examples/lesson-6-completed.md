# Lección 6: Consejos, Mejores Prácticas y Depuración (Completed)

Este documento contiene la solución completa de la **Lección 6**. Demuestra la aplicación de código limpio (`camelCase`, sangría consistente y comentarios), el "truco del detective" con mensajes `[DEBUG]` y el uso de recursos recomendados para continuar aprendiendo Java.

---

## 💻 Código Completo Resuelto (`Main.java`)

Listo para copiar y ejecutar directamente en **OnlineGDB** (`Language: Java`):

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("=== GUIA DE BUENAS PRACTICAS Y DEPURACION EN JAVA ===\n");

        // 1. Nombres descriptivos en formato camelCase y sangria consistente
        String nombreJugador = "Alex";
        int puntuacionMaxima = 100;
        int nivelActual = 3;

        System.out.println("Jugador: " + nombreJugador);
        System.out.println("Puntaje: " + puntuacionMaxima);
        System.out.println("Nivel actual: " + nivelActual);

        // 2. Truco del detective: mensajes [DEBUG] para rastrear el flujo
        System.out.println("\n[DEBUG] Evaluando condiciones para subir de nivel...");

        if (puntuacionMaxima >= 100) {
            nivelActual++;
            System.out.println("[DEBUG] Condicion cumplida correctamente.");
            System.out.println("¡Excelente! Has subido al nivel " + nivelActual);
        } else {
            System.out.println("[DEBUG] Puntaje insuficiente para subir de nivel.");
        }

        // 3. Recorrido seguro de arreglos evitando salir del limite
        System.out.println("\n--- Recursos recomendados para seguir aprendiendo ---");
        String[] recursos = {
            "Documentacion oficial de Oracle Java",
            "Tutoriales interactivos en W3Schools",
            "Plataforma de ejercicios Exercism"
        };

        for (int i = 0; i < recursos.length; i++) {
            System.out.println((i + 1) + ". " + recursos[i]);
        }

        System.out.println("\n¡Programa finalizado exitosamente!");
    }
}
```

---

## 🖥️ Salida Esperada en Consola

```text
=== GUIA DE BUENAS PRACTICAS Y DEPURACION EN JAVA ===

Jugador: Alex
Puntaje: 100
Nivel actual: 3

[DEBUG] Evaluando condiciones para subir de nivel...
[DEBUG] Condicion cumplida correctamente.
¡Excelente! Has subido al nivel 4

--- Recursos recomendados para seguir aprendiendo ---
1. Documentacion oficial de Oracle Java
2. Tutoriales interactivos en W3Schools
3. Plataforma de ejercicios Exercism

¡Programa finalizado exitosamente!
```

---

## 📖 Explicación Paso a Paso
* **Uso de `camelCase` y nombres claros:** Se reemplazan identificadores genéricos (`n`, `p`, `lvl`) por nombres autoexplicativos como `nombreJugador`, `puntuacionMaxima` y `nivelActual` (coincidiendo con el ejemplo demostrado en el video).
* **Sangría consistente y comentarios `//`:** Cada bloque dentro de `{ }` mantiene 4 espacios de sangría y notas claras para facilitar la lectura por otros estudiantes o programadores.
* **Depuración con `[DEBUG]`:** Los mensajes temporales con `System.out.println` permiten verificar exactamente qué rama del condicional `if-else` se ejecuta cuando no hay errores de sintaxis, pero el resultado lógico genera dudas.
* **Prevención de `ArrayIndexOutOfBoundsException`:** Al usar la condición estricta `i < recursos.length` en el bucle `for`, se garantiza recorrer únicamente posiciones válidas del arreglo.
* **Errores de sintaxis clave repasados en el video:**
  * `';' expected` -> Falta un punto y coma al final de una sentencia.
  * `error: package system does not exist` -> Java distingue mayúsculas de minúsculas (`System` y `String` inician con mayúscula).
  * `reached end of file while parsing` -> Falta una llave `}` de cierre en un bloque o método.
