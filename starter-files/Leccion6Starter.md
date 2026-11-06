
*(Esta es la plantilla inicial que se le daría a un estudiante principiante para que él mismo corrija los errores y aplique las buenas prácticas).*
```markdown
# Lección 6: Actividad Práctica - Limpieza y Depuración (Starter)

Bienvenido a la práctica de la Lección 6. Tu objetivo es tomar este código base que contiene malas prácticas y pequeños errores comunes para corregirlo y dejarlo limpio.

```


##  Código Inicial (Plantilla)

Copia este código en tu editor en línea (OnlineGDB, Replit o JDoodle) y sigue los retos:

```java
public class Leccion6Starter {
    public static void main(String[] args) {
        
        // RETO 1: Cambia estos nombres de variables genericos a nombres descriptivos usando camelCase
        String n = "Alex";
        int p = 100;
        int lvl = 3;

        // RETO 2: Ordena la sangria (tabulacion) de estas lineas para que el codigo no este pegado
System.out.println("Estudiante: " + n);
System.out.println("Puntos: " + p);

        // RETO 3: Agrega un mensaje temporal con System.out.println para rastrear si entra al if
        if (p >= 100) {
            lvl++;
            System.out.println("Subiste de nivel a: " + lvl);
        }

        // RETO 4: Asegurate de que el bucle for no exceda el limite del arreglo (cuidado con el <= o <)
        String[] recursos = {"Oracle Java", "W3Schools", "Exercism"};
        
        // TODO: Itera sobre el arreglo de forma segura usando recursos.length
        for (int i = 0; i < recursos.length; i++) {
            System.out.println(recursos[i]);
        }
    }
}

🎯 Instrucciones de la Actividad
Renombra n, p y lvl a nombres significativos (por ejemplo: nombreEstudiante, puntaje, nivelActual).
Aplica sangría correcta dentro del método main.
Ejecuta el código y comprueba que la consola muestre los resultados sin advertencias ni errores en rojo.
Code
```
