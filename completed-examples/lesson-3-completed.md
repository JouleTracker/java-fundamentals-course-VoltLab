# Clase 3 - Estructuras de Control: Decisiones y Bucles (Completed)

Este documento contiene la solución completa y explicada de la lección 3.

---

##  Código Completo Resuelto

A continuación se presenta el código final listo para ejecutarse en cualquier editor en línea o terminal:

```java
public class Leccion3Completed {
    public static void main(String[] args) {
        System.out.println("=== BIENVENIDO AL PARQUE DE AVENTURAS ===");

        // ---------------------------------------------------------------------
        // PARTE 1: DECISIONES CON IF, ELSE IF Y ELSE
        // ---------------------------------------------------------------------
        // Evaluamos la estatura en centimetros de un estudiante para ingresar a la atraccion.
        int estaturaEstudiante = 135; // Probamos con 135 cm
        boolean vieneConAdulto = true; // Variable booleana para acceso acompanado

        System.out.println("Estatura registrada: " + estaturaEstudiante + " cm.");
        System.out.println("Verificando acceso a la montaña rusa...");

        if (estaturaEstudiante >= 140) {
            System.out.println("Resultado: ¡Acceso concedido! Disfruta la atraccion.");
        } else if (estaturaEstudiante >= 120 && vieneConAdulto) {
            System.out.println("Resultado: ¡Acceso concedido con acompanante adulto!");
        } else {
            System.out.println("Resultado: Acceso denegado. Se requiere una estatura minima de 140 cm (o 120 cm con adulto).");
        }

        // ---------------------------------------------------------------------
        // PARTE 2: BUCLE DETERMINADO CON FOR
        // ---------------------------------------------------------------------
        // Realizamos una cuenta regresiva del 5 al 1 para el lanzamiento del cohete.
        System.out.println("\n=== ZONA DE ENTRENAMIENTO: BUCLES ===");
        System.out.println("Iniciando cuenta regresiva:");

        for (int i = 5; i >= 1; i--) {
            System.out.println(i + "...");
        }
        System.out.println("¡Despegue con exito!");

        // ---------------------------------------------------------------------
        // PARTE 3: BUCLE CONDICIONAL CON WHILE
        // ---------------------------------------------------------------------
        // Simulamos la recarga de bateria de un robot explorador hasta el 100%.
        int bateria = 70;
        System.out.println("\nCargando bateria del robot...");
        System.out.println("Nivel inicial: " + bateria + "%");

        while (bateria < 100) {
            bateria += 10; // Incrementamos la bateria de 10 en 10
            System.out.println("Cargando... Bateria al " + bateria + "%");
        }

        System.out.println("¡Bateria completamente cargada al 100%!");
    }
}
```

---

## 🖥 Salida Esperada en Consola

Al ejecutar el programa anterior, se obtiene la siguiente salida:

```text
=== BIENVENIDO AL PARQUE DE AVENTURAS ===
Estatura registrada: 135 cm.
Verificando acceso a la montaña rusa...
Resultado: ¡Acceso concedido con acompanante adulto!

=== ZONA DE ENTRENAMIENTO: BUCLES ===
Iniciando cuenta regresiva:
5...
4...
3...
2...
1...
¡Despegue con exito!

Cargando bateria del robot...
Nivel inicial: 70%
Cargando... Bateria al 80%
Cargando... Bateria al 90%
Cargando... Bateria al 100%
¡Bateria completamente cargada al 100%!
```

---

##  Explicación Paso a Paso

1. **Evaluación de condiciones (`if-else if-else`):**
   * Primero se evalúa si `estaturaEstudiante >= 140`. Si es falso, pasa a la siguiente condición.
   * En el `else if`, se verifica con el operador lógico `&&` (Y) que la estatura sea al menos 120 cm y que la variable `vieneConAdulto` sea `true`.
   * Si ninguna condición se cumple, se ejecuta el bloque `else`.

2. **Cuenta regresiva con `for`:**
   * `int i = 5`: Inicia el contador en 5.
   * `i >= 1`: Condición de parada (continúa mientras `i` sea mayor o igual a 1).
   * `i--`: En cada iteración disminuye el valor de `i` en 1.

3. **Recarga con `while`:**
   * La condición `bateria < 100` se comprueba antes de entrar al ciclo.
   * Dentro del bucle, la instrucción `bateria += 10` asegura que en algún momento la condición se vuelva falsa, evitando que el programa se quede atrapado en un ciclo infinito.
