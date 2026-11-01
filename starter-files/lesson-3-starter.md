# Clase 3 - Estructuras de Control: Decisiones y Bucles (Starter)

Este documento sirve como guía para la lección práctica y contiene la plantilla de código inicial que los estudiantes utilizarán durante la clase 3.

---

##  Objetivo de la Lección
Aprender a controlar el flujo de ejecución de un programa en Java mediante:
1. **Toma de decisiones:** Sentencias condicionales `if`, `else if` y `else`.
2. **Repetición de tareas:** Bucles determinados con `for` y bucles condicionales con `while`.

---

##  Conceptos Clave

### 1. Estructuras Condicionales (`if-else`)
Permiten que el programa tome caminos distintos según si una condición lógica es verdadera (`true`) o falsa (`false`).

```java
if (condicion) {
    // Código que se ejecuta si la condición es verdadera
} else {
    // Código que se ejecuta si la condición es falsa
}
```

### 2. Operadores de Comparación
* `==` : Igual a
* `!=` : Diferente de
* `>` : Mayor que
* `<` : Menor que
* `>=` : Mayor o igual que
* `<=` : Menor o igual que

### 3. Bucles (`for` y `while`)
* **Bucle `for`:** Se utiliza cuando conocemos de antemano cuántas veces queremos repetir un bloque de código (por ejemplo, contar del 1 al 5).
* **Bucle `while`:** Se repite continuamente **mientras** una condición siga siendo verdadera.

---

## Código Inicial (Starter)

Copia y pega el siguiente código en tu editor en línea (**JDoodle**, **Replit** o **OnlineGDB**):

```java
public class Leccion3Starter {
    public static void main(String[] args) {
        System.out.println("=== BIENVENIDO AL PARQUE DE AVENTURAS ===");

        // PARTE 1: DECISIONES CON IF-ELSE
        // Situación: Para subir a la montaña rusa espacial, la estatura mínima es 140 cm.
        int estaturaEstudiante = 145; // Puedes cambiar este valor para probar

        System.out.println("Verificando acceso a la atraccion...");

        // TODO 1: Escribe una estructura if-else para verificar si estaturaEstudiante >= 140.
        // Si cumple, muestra: "¡Acceso concedido! Disfruta la atraccion."
        // Si no cumple, muestra: "Acceso denegado: debes medir al menos 140 cm."



        System.out.println("\n=== ZONA DE ENTRENAMIENTO: BUCLES ===");

        // PARTE 2: BUCLE FOR
        // Situación: Cuenta regresiva para el lanzamiento de un cohete (del 5 al 1) y luego ¡Despegue!
        System.out.println("Iniciando cuenta regresiva:");

        // TODO 2: Completa el bucle for para contar de 5 hacia 1.
        /*
        for (int i = 5; i >= 1; i--) {
            System.out.println(i + "...");
        }
        System.out.println("¡Despegue!");
        */



        // PARTE 3: BUCLE WHILE
        // Situación: Cargar la bateria de un robot explorador hasta llegar a 100%.
        int bateria = 70;
        System.out.println("\nCargando bateria del robot...");

        // TODO 3: Usa un bucle while para incrementar la bateria de 10 en 10 mientras sea menor que 100.
        /*
        while (bateria < 100) {
            bateria += 10;
            System.out.println("Bateria actual: " + bateria + "%");
        }
        System.out.println("¡Carga completa!");
        */
    }
}
```

---

##  Retos para el Estudiante
1. Cambia el valor de `estaturaEstudiante` a `130` y comprueba que se ejecute la rama alternativa (`else`).
2. Agrega una condición adicional con `else if` para permitir el acceso con acompañante adulto si la estatura está entre `120` y `139` cm.
3. Modifica la cuenta regresiva del bucle `for` para que cuente del `1` al `10` en orden ascendente.
