# Lección 2 - Variables y Tipos de Datos (Starter)

## 1. Objetivo de la actividad

En esta actividad aprenderás a utilizar variables en Java para guardar diferentes tipos de información.

Al finalizar, podrás:

- Comprender qué es una variable.
- Identificar los tipos de datos `int`, `double`, `String` y `boolean`.
- Crear variables y asignarles valores.
- Mostrar información utilizando `System.out.println()`.
- Crear un pequeño programa con tus datos personales.

## 2. Guía de práctica

### ¿Qué es una variable?

Imagina que tienes diferentes cajas donde puedes guardar cosas. Una caja puede guardar tu nombre, otra tu edad y otra tu color favorito.

En programación, estas cajas se llaman **variables**.

Una variable es un espacio en la memoria de la computadora donde podemos guardar información para utilizarla después.

Por ejemplo:

```java
int edad = 10;
```

En este ejemplo, creamos una variable llamada `edad` y guardamos el número `10`.

### 3. Conoce los tipos de datos

En Java existen diferentes tipos de datos. En esta actividad utilizaremos cuatro de los más importantes:

| Tipo de dato | ¿Qué almacena? | Ejemplo |
|---|---|---|
| `int` | Números enteros | `10` |
| `double` | Números decimales | `1.50` |
| `String` | Textos y palabras | `"Sofia"` |
| `boolean` | Verdadero o falso | `true` |

**Recuerda:**

- `int`: se utiliza para números sin decimales.
- `double`: permite guardar números con decimales.
- `String`: permite guardar nombres, palabras y frases. Su primera letra es mayúscula.
- `boolean`: solamente puede almacenar `true` o `false`.

## 4. Actividad inicial

Vamos a crear un programa que almacene información de una persona.

Completa los siguientes pasos:

1. Guarda un nombre utilizando `String`.
2. Guarda una edad utilizando `int`.
3. Guarda una altura utilizando `double`.
4. Indica si a la persona le gusta jugar utilizando `boolean`.
5. Muestra todos los valores en la consola.

## 5. Código base (Starter)

Completa los espacios indicados en el siguiente programa:

```java
public class Main {
    public static void main(String[] args) {

        // 1. Guarda un nombre utilizando String.
        String nombre = "";

        // 2. Guarda una edad utilizando int.
        int edad = 0;

        // 3. Guarda una altura utilizando double.
        double altura = 0.0;

        // 4. Indica si le gusta jugar utilizando boolean.
        boolean leGustaJugar = false;

        // 5. Muestra el nombre en la consola.
        System.out.println("Nombre: " + nombre);

        // TODO: Muestra la edad.

        // TODO: Muestra la altura.

        // TODO: Muestra si le gusta jugar.
    }
}
```

## 6. Tu reto: ¡Crea un programa sobre ti!

Ahora que conoces los cuatro tipos de datos, es momento de crear tu propio programa.

Imagina que quieres mostrar información sobre ti mismo.

Tu programa debe guardar:

- Tu nombre.
- Tu edad.
- Tu color favorito.

### Instrucciones

1. Crea una variable `String` para tu nombre.
2. Crea una variable `int` para tu edad.
3. Crea una variable `String` para tu color favorito.
4. Utiliza `System.out.println()` para mostrar toda tu información.

### Ejemplo de referencia

```java
String nombre = "Sofia";
int edad = 9;
String colorFavorito = "Verde";
```

**¡Importante!** Cambia los valores del ejemplo por tus propios datos.

## 7. Conceptos clave

- **Variable:** espacio donde guardamos información.
- **Tipo de dato:** indica qué clase de información podemos guardar.
- **Asignación:** consiste en guardar un valor dentro de una variable.
- **System.out.println():** permite mostrar información en la consola.

## 8. Comprueba lo aprendido

Antes de terminar, responde estas preguntas:

1. ¿Qué es una variable?
2. ¿Qué tipo de dato utilizarías para guardar tu edad?
3. ¿Qué tipo de dato permite guardar números decimales?
4. ¿Qué valores puede almacenar un boolean?
5. ¿Para qué sirve `System.out.println()`?

¡Excelente trabajo! Ahora estás listo para utilizar variables en Java.