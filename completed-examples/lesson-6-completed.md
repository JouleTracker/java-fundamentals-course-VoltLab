# Lección 6: Consejos, Mejores Prácticas y Depuración (Completed)

Este documento contiene la solución completa de la Lección 6. Muestra la aplicación de buenas prácticas de nombrado, indentación y técnicas de depuración en consola para Java.

---

## 💻 Código Completo Resuelto

```java
public class Leccion6Completed {
    public static void main(String[] args) {
        System.out.println("=== GUIA DE BUENAS PRACTICAS Y DEPURACION EN JAVA ===\n");

        // 1. Nombres descriptivos en formato camelCase
        String nombreEstudiante = "Alex";
        int puntuacionMaxima = 100;
        int nivelActual = 3;

        System.out.println("Estudiante: " + nombreEstudiante);
        System.out.println("Puntaje acumulado: " + puntuacionMaxima);
        System.out.println("Nivel actual: " + nivelActual);

        // 2. Tecnica de rastreo (mensajes de depuracion en consola)
        System.out.println("\n[DEBUG] Evaluando condiciones para subir de nivel...");

        if (puntuacionMaxima >= 100) {
            nivelActual++;
            System.out.println("[DEBUG] Condicion cumplida correctamente.");
            System.out.println("¡Felicitaciones! Has subido al nivel " + nivelActual);
        } else {
            System.out.println("[DEBUG] Puntuacion insuficiente.");
        }

        // 3. Recorrido seguro de colecciones evitando errores de limite
        System.out.println("\n--- Recursos recomendados ---");
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

🖥 Salida Esperada en Consola
Text
=== GUIA DE BUENAS PRACTICAS Y DEPURACION EN JAVA ===

Estudiante: Alex
Puntaje acumulado: 100
Nivel actual: 3

[DEBUG] Evaluando condiciones para subir de nivel...
[DEBUG] Condicion cumplida correctamente.
¡Felicitaciones! Has subido al nivel 4

--- Recursos recomendados ---
1. Documentacion oficial de Oracle Java
2. Tutoriales interactivos en W3Schools
3. Plataforma de ejercicios Exercism

¡Programa finalizado exitosamente!
📖 Explicación Paso a Paso
Uso de camelCase y nombres claros: Se evita el uso de variables de una sola letra (como x o y), empleando identificadores claros como nombreEstudiante o puntuacionMaxima.
Indentación consistente: Todo bloque de código dentro de las llaves { } cuenta con 4 espacios de sangría para hacer evidente la estructura del programa.
Depuración con [DEBUG]: Permite verificar paso a paso en qué punto entra el flujo de ejecución cuando se evalúa una condición if-else.
Prevención de ArrayIndexOutOfBoundsException: Se utiliza la propiedad .length en el bucle para asegurar que nunca se solicite un índice inexistente del arreglo.
Code
