# Clase 4 - Métodos, Entrada/Salida e Introducción a la POO (Starter)

Este documento sirve como guía práctica y contiene la plantilla de código inicial que los estudiantes utilizarán durante la clase 4.

---

## Objetivo de la Lección
1. **Métodos:** Comprender cómo dividir un programa en bloques de código reutilizables con parámetros y valores de retorno.
2. **Entrada y Salida estándar:** Aprender a solicitar y leer datos ingresados por el usuario desde la consola utilizando la clase `Scanner` de la biblioteca estándar de Java.
3. **Introducción a la Programación Orientada a Objetos (POO):** Comprender los conceptos fundamentales de **clase** (molde o plantilla), **objeto** (instancia en la vida real), **atributos** (características) y **métodos** (comportamientos).

---

## Conceptos Clave

### 1. ¿Qué es un Método?
Un método es un bloque de instrucciones que realiza una tarea específica y se ejecuta únicamente cuando es llamado (invocado). Nos ayuda a evitar escribir el mismo código muchas veces (principio de reutilización).

```java
// Método que recibe un parámetro y devuelve un resultado
public static int sumar(int a, int b) {
    return a + b;
}
```

### 2. Entrada de Datos con `Scanner`
Para que un programa sea interactivo y reciba datos desde el teclado, importamos la clase `Scanner` desde la biblioteca estándar de Java (`java.util.Scanner`):

```java
import java.util.Scanner;

Scanner scanner = new Scanner(System.in);
System.out.print("Escribe tu nombre: ");
String nombre = scanner.nextLine(); // Lee texto escrito por el usuario
```

### 3. Clases y Objetos
* **Clase:** Es el molde o plano arquitectónico (por ejemplo, el diseño general de una `Mascota`).
* **Objeto:** Es el ejemplar real creado a partir de ese molde (por ejemplo, tu perro "Pixel" o tu gato "Michi").
* **Atributos:** Son las variables que describen las características del objeto (`nombre`, `especie`, `energia`).
* **Instanciación:** Crear un objeto en memoria usando la palabra clave `new`.

---

## Código Inicial (Starter)

Copia y pega la siguiente plantilla en tu editor en línea (**OnlineGDB**, **Replit** o **JDoodle**):

```java
import java.util.Scanner;

// =============================================================================
// PARTE 3: DEFINICIÓN DE LA CLASE MASCOTA (EL MOLDE)
// =============================================================================
class Mascota {
    // Atributos (características de cualquier mascota)
    String nombre;
    String especie;
    int energia;

    // TODO 3: Completa el constructor de la clase Mascota
    public Mascota(String nombre, String especie, int energia) {
        // Asigna los valores recibidos a los atributos usando 'this'
        // this.nombre = nombre;
        // this.especie = especie;
        // this.energia = energia;
    }

    // Método de comportamiento: muestra los datos de la mascota
    public void mostrarEstado() {
        System.out.println("\n--- FICHA DE LA MASCOTA ---");
        System.out.println("Nombre: " + nombre);
        System.out.println("Especie: " + especie);
        System.out.println("Energia: " + energia + "/100");
    }

    // TODO 4: Completa el método jugar para simular gasto de energía
    public void jugar(int minutos) {
        // Muestra un mensaje indicando cuántos minutos juega la mascota
        // Resta energía (por ejemplo: energia -= (minutos * 2))
        // Asegúrate de que la energía no baje de cero
    }
}

// =============================================================================
// CLASE PRINCIPAL
// =============================================================================
public class Leccion4Starter {

    // TODO 1: Crea un método estático llamado 'saludar' que reciba un String (nombreUsuario)
    // y muestre: "¡Hola, " + nombreUsuario + "! Bienvenido al Creador de Mascotas."
    public static void saludar(String nombreUsuario) {
        // Escribe aquí tu código
    }

    // TODO 2: Crea un método estático llamado 'calcularEdadMascota' que reciba un int (edadHumanos)
    // y devuelva (return) los años equivalentes multiplicados por 7.
    public static int calcularEdadMascota(int edadHumanos) {
        // Reemplaza este valor por la fórmula
        return 0;
    }

    public static void main(String[] args) {
        System.out.println("=== LECCIÓN 4: MÉTODOS, ENTRADA DE DATOS Y POO ===");

        // --- Probando métodos ---
        saludar("Explorador");
        int edad = calcularEdadMascota(2);
        System.out.println("2 años humanos equivalen a unos " + edad + " años mascota.\n");

        // --- Entrada de datos con Scanner ---
        Scanner scanner = new Scanner(System.in);

        System.out.println("--- REGISTRO DE TU MASCOTA VIRTUAL ---");
        System.out.print("Escribe el nombre de tu mascota: ");
        String nombre = scanner.nextLine();

        System.out.print("Escribe la especie (ej. Perro, Gato, Robot): ");
        String especie = scanner.nextLine();

        // TODO 5: Instancia un nuevo objeto de la clase Mascota usando la palabra 'new'
        // Mascota miMascota = new Mascota(nombre, especie, 100);

        // TODO 6: Invoca los métodos mostrarEstado() y jugar(15) sobre tu objeto


        scanner.close();
    }
}
```

---

## Retos para el Estudiante
1. Agrega un método nuevo a la clase `Mascota` llamado `alimentar(int comida)` que recupere puntos de energía sin superar 100.
2. Agrega una validación con `if` para que la mascota no pueda jugar si su energía está en 0.
3. Crea un segundo objeto `Mascota` (por ejemplo, la mascota de un amigo) con valores distintos para comprobar que cada objeto tiene sus propios datos independientes.
