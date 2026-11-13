# Clase 4 - Métodos, Entrada/Salida e Introducción a la POO (Completed)

Este documento contiene la solución completa, explicada y comentada paso a paso de la lección 4.

---

##  Código Completo Resuelto

A continuación se presenta el código final listo para ejecutarse en cualquier editor en línea (**OnlineGDB**, **Replit**, **JDoodle**) o entorno local:

```java
import java.util.Scanner;

// =============================================================================
// PARTE 3: DEFINICIÓN DE LA CLASE MASCOTA (EL MOLDE O PLANTILLA DE POO)
// =============================================================================
class Mascota {
    // Atributos: representan las características o estado de cada mascota
    String nombre;
    String especie;
    int energia;

    // Constructor: método especial que inicializa el objeto cuando se crea con 'new'
    public Mascota(String nombre, String especie, int energia) {
        this.nombre = nombre;
        this.especie = especie;
        this.energia = energia;
    }

    // Método de comportamiento: muestra en consola la ficha actual de la mascota
    public void mostrarEstado() {
        System.out.println("\n--- FICHA DE LA MASCOTA ---");
        System.out.println("Nombre: " + this.nombre);
        System.out.println("Especie: " + this.especie);
        System.out.println("Energia: " + this.energia + "/100");
    }

    // Método con parámetro: simula la acción de jugar y reduce la energía
    public void jugar(int minutos) {
        System.out.println("\n" + this.nombre + " esta jugando intensamente por " + minutos + " minutos...");
        this.energia -= (minutos * 2);

        // Validación para evitar que la energía sea un valor negativo
        if (this.energia < 0) {
            this.energia = 0;
        }

        System.out.println("Energia restante tras jugar: " + this.energia + "/100");
    }
}

// =============================================================================
// CLASE PRINCIPAL DEL PROGRAMA
// =============================================================================
public class Leccion4Completed {

    // PARTE 1: MÉTODOS REUTILIZABLES
    // Método que recibe un parámetro y no devuelve valor (void)
    public static void saludar(String nombreUsuario) {
        System.out.println("¡Hola, " + nombreUsuario + "! Bienvenido al Creador de Mascotas.");
    }

    // Método con parámetro que calcula y RETORNA un valor entero (int)
    public static int calcularEdadMascota(int edadHumanos) {
        return edadHumanos * 7; // Regla de aproximación para años de mascota
    }

    public static void main(String[] args) {
        System.out.println("=== LECCIÓN 4: MÉTODOS, ENTRADA DE DATOS Y POO ===");

        // --- Demostración de métodos auxiliares ---
        saludar("Explorador");
        int edadEquivalente = calcularEdadMascota(2);
        System.out.println("Una mascota de 2 anos humanos equivale a unos " + edadEquivalente + " anos mascota.\n");

        // --- PARTE 2: ENTRADA DE DATOS CON SCANNER ---
        // Se crea el lector a partir de System.in (teclado/consola)
        Scanner scanner = new Scanner(System.in);

        System.out.println("--- REGISTRO DE TU MASCOTA VIRTUAL ---");
        System.out.print("Escribe el nombre de tu mascota: ");
        String nombre = scanner.nextLine();

        System.out.print("Escribe la especie (ej. Perro, Gato, Robot): ");
        String especie = scanner.nextLine();

        // --- PARTE 3: CREACIÓN Y USO DEL OBJETO (INSTANCIACIÓN) ---
        // Se usa la palabra clave 'new' para reservar memoria y construir el objeto
        Mascota miMascota = new Mascota(nombre, especie, 100);

        // Invocación de comportamientos (métodos del objeto)
        miMascota.mostrarEstado();
        miMascota.jugar(15);

        // Cierre del recurso Scanner
        scanner.close();
    }
}
```

---

## Demostración y Salida en Consola

Al ejecutar el programa anterior e interactuar con la consola (ingresando `Pixel` como nombre y `Perro Robot` como especie), se obtiene la siguiente salida:

```text
=== LECCIÓN 4: MÉTODOS, ENTRADA DE DATOS Y POO ===
¡Hola, Explorador! Bienvenido al Creador de Mascotas.
Una mascota de 2 anos humanos equivale a unos 14 anos mascota.

--- REGISTRO DE TU MASCOTA VIRTUAL ---
Escribe el nombre de tu mascota: Pixel
Escribe la especie (ej. Perro, Gato, Robot): Perro Robot

--- FICHA DE LA MASCOTA ---
Nombre: Pixel
Especie: Perro Robot
Energia: 100/100

Pixel esta jugando intensamente por 15 minutos...
Energia restante tras jugar: 70/100
```

---

##  Explicación Técnica Paso a Paso

1. **Métodos (`saludar` y `calcularEdadMascota`):**
   * El método `saludar` tiene modificador `void` porque solo realiza una acción (imprimir en consola) sin retornar ningún valor numérico o textual.
   * El método `calcularEdadMascota` define un tipo de retorno `int` y usa la sentencia `return` para devolver el resultado del cálculo a la línea donde fue llamado.
2. **Entrada con `Scanner`:**
   * Proviene del paquete `java.util`, perteneciente a la biblioteca estándar de Java.
   * El método `nextLine()` captura la línea de texto completa escrita por el usuario hasta que presiona la tecla Enter.
3. **Clases y Objetos en POO:**
   * `class Mascota`: Define el plano o estructura general.
   * `this.nombre`: La palabra clave `this` permite diferenciar el atributo de la clase del parámetro recibido con el mismo nombre en el constructor.
   * `new Mascota(...)`: Operador de instanciación que crea un ejemplar independiente en la memoria de Java con sus propios datos.
