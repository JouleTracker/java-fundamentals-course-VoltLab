# Clase 5 - Fundamentos de POO y programas sencillos (Starter)

Este documento sirve como guía práctica y contiene la plantilla de código inicial que los estudiantes utilizarán durante la **Lección 5**, enfocada en construir un **Sistema de Gestión para una Tienda de Mascotas** aplicando Programación Orientada a Objetos (POO).

---

## Objetivos de la Lección
1. **Encapsulación:** Proteger los atributos de una clase con el modificador `private` y controlar el acceso mediante métodos **getters** y **setters** (incluyendo validaciones).
2. **Constructores con `this`:** Inicializar objetos con estado inicial consistente al momento de crearlos con `new`.
3. **Interacción entre múltiples clases:** Organizar un programa por responsabilidades usando las clases `Mascota`, `Cliente`, `TiendaMascotas` y `Main`.
4. **Arreglos de objetos:** Almacenar y recorrer múltiples instancias (`Mascota[]`) mediante bucles `for` y comparaciones de texto con `equalsIgnoreCase`.

---

## Conceptos Clave

### 1. Encapsulación, Getters y Setters
Declarar atributos como `private` impide que otras clases los modifiquen sin control:

```java
private int edad;

public int getEdad() {
    return edad;
}

public void setEdad(int edad) {
    if (edad >= 0) {
        this.edad = edad;
    }
}
```
> **Nota:** Para atributos de tipo `boolean`, por convención el método de consulta inicia con `is` (por ejemplo, `isDisponible()`).

### 2. Separación de Responsabilidades
En lugar de concentrar toda la lógica en `Main`, dividimos el sistema:
* `Mascota`: Representa cada animal, sus datos y su cambio de estado al ser adoptado.
* `Cliente`: Representa a la persona que adopta.
* `TiendaMascotas`: Administra el catálogo (`Mascota[]`), el registro de nuevas mascotas y el proceso de adopción.
* `Main`: Crea los objetos iniciales y ejecuta la demostración del sistema.

---

##  Plantilla de Código Inicial (Para el Estudiante)

Crea cuatro pestañas/archivos en tu editor en línea (**OnlineGDB** con lenguaje **Java**): `Mascota.java`, `Cliente.java`, `TiendaMascotas.java` y `Main.java`, y completa las secciones marcadas con `// TODO:`.

### 1. `Mascota.java`

```java
public class Mascota {
    // Atributos privados
    private String nombre;
    private String especie;
    private int edad;
    private boolean disponible;

    // Constructor
    public Mascota(String nombre, String especie, int edad) {
        this.nombre = nombre;
        this.especie = especie;
        this.edad = edad;
        // TODO 1: Inicializa 'disponible' en true, ya que una mascota recién ingresada aún no ha sido adoptada
    }

    // Getters
    public String getNombre() {
        return nombre;
    }

    public String getEspecie() {
        return especie;
    }

    public int getEdad() {
        return edad;
    }

    public boolean isDisponible() {
        return disponible;
    }

    // Setters
    public void setNombre(String nombre) {
        this.nombre = nombre;
    }

    public void setEdad(int edad) {
        // TODO 2: Agrega una condición para asignar 'this.edad = edad' solo si 'edad >= 0'
    }

    // Mostrar información
    public void mostrarInformacion() {
        System.out.println("Nombre: " + nombre);
        System.out.println("Especie: " + especie);
        System.out.println("Edad: " + edad + " años");

        if (disponible) {
            System.out.println("Estado: Disponible");
        } else {
            System.out.println("Estado: Adoptada");
        }
    }

    // TODO 3: Completa el método 'adoptar()' para cambiar 'disponible' a false
    public void adoptar() {
        // Escribe aquí tu código
    }
}
```

### 2. `Cliente.java`

```java
public class Cliente {
    // Atributos privados
    private String nombre;
    private String correo;
    private int edad;

    // Constructor
    public Cliente(String nombre, String correo, int edad) {
        // TODO 4: Asigna los parámetros 'nombre', 'correo' y 'edad' a los atributos usando 'this'
    }

    // Getters
    public String getNombre() {
        return nombre;
    }

    public String getCorreo() {
        return correo;
    }

    public int getEdad() {
        return edad;
    }

    // Setters
    public void setNombre(String nombre) {
        this.nombre = nombre;
    }

    public void setCorreo(String correo) {
        this.correo = correo;
    }

    // TODO 5: Completa el método 'mostrarInformacion()' para imprimir nombre, correo y edad del cliente
    public void mostrarInformacion() {
        System.out.println("Nombre del cliente: " + nombre);
        // Imprime también Correo y Edad
    }
}
```

### 3. `TiendaMascotas.java`

```java
public class TiendaMascotas {
    // Arreglo de objetos
    private Mascota[] mascotas;
    private int cantidad;

    // Constructor
    public TiendaMascotas() {
        mascotas = new Mascota[10];
        cantidad = 0;
    }

    // Registrar una mascota
    public void registrarMascota(Mascota mascota) {
        // TODO 6: Verifica si 'cantidad < mascotas.length'. Si hay espacio, guarda la mascota en 'mascotas[cantidad]', incrementa 'cantidad' e imprime "Mascota registrada correctamente.". Si no, imprime "La tienda está llena."
    }

    // Mostrar todas las mascotas
    public void mostrarMascotas() {
        System.out.println("\n===== CATALOGO DE MASCOTAS =====");
        for (int i = 0; i < cantidad; i++) {
            System.out.println("\nMascota " + (i + 1));
            mascotas[i].mostrarInformacion();
            System.out.println("----------------------");
        }
    }

    // Buscar y adoptar una mascota
    public void registrarAdopcion(String nombre, Cliente cliente) {
        for (int i = 0; i < cantidad; i++) {
            // TODO 7: Compara 'mascotas[i].getNombre().equalsIgnoreCase(nombre)'. Si coincide y 'isDisponible()' es verdadero, llama a 'adoptar()' e imprime el éxito con cliente y mascota; si no está disponible, imprime "Esta mascota ya fue adoptada.". Luego usa 'return;'
        }
        System.out.println("La mascota no existe en el catalogo.");
    }
}
```

### 4. `Main.java`

```java
public class Main {
    public static void main(String[] args) {
        // Crear la tienda
        TiendaMascotas tienda = new TiendaMascotas();

        // Crear mascotas
        Mascota mascota1 = new Mascota("Max", "Perro", 3);
        Mascota mascota2 = new Mascota("Michi", "Gato", 2);
        // TODO 8: Crea 'mascota3' ("Luna", "Conejo", 1)

        // Registrar mascotas
        tienda.registrarMascota(mascota1);
        tienda.registrarMascota(mascota2);
        // TODO 9: Registra a 'mascota3' y muestra el catálogo con 'tienda.mostrarMascotas()'

        // Crear un cliente
        Cliente cliente1 = new Cliente("Carlos", "carlos@gmail.com", 20);

        // Mostrar información del cliente
        System.out.println("\n===== DATOS DEL CLIENTE =====");
        cliente1.mostrarInformacion();

        // TODO 10: Registra la adopción de "Max" por 'cliente1' y vuelve a mostrar el catálogo para comprobar el cambio de estado
    }
}
```

---

## Desafíos Adicionales (Para Explorar)
1. **Doble adopción:** Intenta llamar a `tienda.registrarAdopcion("Max", cliente1);` una segunda vez después de que `Max` fue adoptado y verifica que aparezca el mensaje `"Esta mascota ya fue adoptada."`.
2. **Mascota inexistente:** Prueba buscar un nombre que no esté en el catálogo (por ejemplo, `"Bobby"`) para observar la respuesta del sistema.
3. **Actualización con setters:** Cambia el correo de `Carlos` usando `cliente1.setCorreo(...)` o intenta asignar una edad negativa a una mascota con `setEdad(-2)` y comprueba si la validación la bloquea.
