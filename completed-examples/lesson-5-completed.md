# Clase 5 - Fundamentos de POO y programas sencillos (Completed)

Este documento contiene la solución completa, verificada y comentada de la **Lección 5**, correspondiente al proyecto **Sistema de Gestión para una Tienda de Mascotas** demostrado en el video.

---

## 🎯 Código Completo Resuelto

En el video se trabaja en **OnlineGDB** (`Language: Java`) con cuatro archivos organizados por responsabilidad: `Mascota.java`, `Cliente.java`, `TiendaMascotas.java` y `Main.java`.

### 1. `Mascota.java`

```java
public class Mascota {
    // Atributos privados (encapsulación)
    private String nombre;
    private String especie;
    private int edad;
    private boolean disponible;

    // Constructor
    public Mascota(String nombre, String especie, int edad) {
        this.nombre = nombre;
        this.especie = especie;
        this.edad = edad;
        this.disponible = true;
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
        if (edad >= 0) {
            this.edad = edad;
        }
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

    // Cambiar disponibilidad
    public void adoptar() {
        disponible = false;
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
        this.nombre = nombre;
        this.correo = correo;
        this.edad = edad;
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

    // Mostrar información del cliente
    public void mostrarInformacion() {
        System.out.println("Nombre del cliente: " + nombre);
        System.out.println("Correo: " + correo);
        System.out.println("Edad: " + edad);
    }
}
```

### 3. `TiendaMascotas.java`

```java
public class TiendaMascotas {
    // Arreglo de objetos y contador de registros
    private Mascota[] mascotas;
    private int cantidad;

    // Constructor
    public TiendaMascotas() {
        mascotas = new Mascota[10];
        cantidad = 0;
    }

    // Registrar una mascota
    public void registrarMascota(Mascota mascota) {
        if (cantidad < mascotas.length) {
            mascotas[cantidad] = mascota;
            cantidad++;
            System.out.println("Mascota registrada correctamente.");
        } else {
            System.out.println("La tienda está llena.");
        }
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
            if (mascotas[i].getNombre().equalsIgnoreCase(nombre)) {
                if (mascotas[i].isDisponible()) {
                    mascotas[i].adoptar();
                    System.out.println("\n¡Adopcion exitosa!");
                    System.out.println("Cliente: " + cliente.getNombre());
                    System.out.println("Mascota: " + mascotas[i].getNombre());
                } else {
                    System.out.println("Esta mascota ya fue adoptada.");
                }
                return;
            }
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
        Mascota mascota3 = new Mascota("Luna", "Conejo", 1);

        // Registrar mascotas
        tienda.registrarMascota(mascota1);
        tienda.registrarMascota(mascota2);
        tienda.registrarMascota(mascota3);

        // Mostrar catálogo
        tienda.mostrarMascotas();

        // Crear un cliente
        Cliente cliente1 = new Cliente(
            "Carlos",
            "carlos@gmail.com",
            20
        );

        // Mostrar información del cliente
        System.out.println("\n===== DATOS DEL CLIENTE =====");
        cliente1.mostrarInformacion();

        // Registrar una adopción
        tienda.registrarAdopcion("Max", cliente1);

        // Mostrar catálogo actualizado
        tienda.mostrarMascotas();
    }
}
```

---

## 🔍 Explicación Paso a Paso de la Solución

1. **Encapsulación en `Mascota` y `Cliente`:**
   * Todos los atributos se declaran con `private`, evitando modificaciones directas externas.
   * Los métodos **getters** (`getNombre()`, `isDisponible()`, etc.) exponen lectura segura, y los **setters** (`setEdad(int edad)`) permiten validar reglas antes de cambiar un dato (por ejemplo, impedir edades negativas).
   * En los constructores se utiliza `this` para distinguir los atributos de la clase de los parámetros recibidos.
2. **Composición y administración en `TiendaMascotas`:**
   * Usa un arreglo de objetos `Mascota[]` con capacidad fija de `10` elementos y una variable entera `cantidad` para rastrear las posiciones ocupadas.
   * `registrarMascota(Mascota mascota)` verifica `cantidad < mascotas.length` antes de insertar el objeto en el arreglo e incrementar el contador.
   * `registrarAdopcion(String nombre, Cliente cliente)` recorre las mascotas registradas, compara nombres ignorando mayúsculas/minúsculas con `equalsIgnoreCase`, verifica `isDisponible()`, cambia el estado llamando a `adoptar()` e imprime la confirmación con el cliente.
3. **Orquestación en `Main`:**
   * Instancia `TiendaMascotas`, tres objetos `Mascota` (`Max`, `Michi`, `Luna`) y un objeto `Cliente` (`Carlos`).
   * Ejecuta el flujo completo: registro, impresión del catálogo inicial, visualización del cliente, adopción de `Max` y consulta del catálogo actualizado.

---

## 💻 Salida Esperada en Consola

```text
Mascota registrada correctamente.
Mascota registrada correctamente.
Mascota registrada correctamente.

===== CATALOGO DE MASCOTAS =====

Mascota 1
Nombre: Max
Especie: Perro
Edad: 3 años
Estado: Disponible
----------------------

Mascota 2
Nombre: Michi
Especie: Gato
Edad: 2 años
Estado: Disponible
----------------------

Mascota 3
Nombre: Luna
Especie: Conejo
Edad: 1 años
Estado: Disponible
----------------------

===== DATOS DEL CLIENTE =====
Nombre del cliente: Carlos
Correo: carlos@gmail.com
Edad: 20

¡Adopcion exitosa!
Cliente: Carlos
Mascota: Max

===== CATALOGO DE MASCOTAS =====

Mascota 1
Nombre: Max
Especie: Perro
Edad: 3 años
Estado: Adoptada
----------------------

Mascota 2
Nombre: Michi
Especie: Gato
Edad: 2 años
Estado: Disponible
----------------------

Mascota 3
Nombre: Luna
Especie: Conejo
Edad: 1 años
Estado: Disponible
----------------------
```
