# Guion de Video - Lección 5: Fundamentos de POO y programas sencillos

* **Duración real del video:** 15:00 minutos (Rango permitido: 5 a 15 minutos).
* **Público objetivo:** Estudiantes de secundaria (12 a 17 años) sin conocimientos previos de programación.
* **Herramienta demostrada:** Editor en línea (OnlineGDB - Java).
* **Enlace del video:** [Ver Lección 5](https://youtu.be/6Sf7poDfdQ8)
* **Regla de estilo:** Cero mención a nombres propios, integrantes o marcas de equipo. Transcripción fiel y estructurada de la explicación paso a paso en pantalla, lenguaje cercano y didáctico, cumpliendo con la terminología formal de ingeniería de software.

---

## Estructura y Cronograma del Video

| Minuto | Sección | Acción visual / En pantalla |
|---|---|---|
| 00:00 - 01:46 | Introducción al proyecto y conceptos de POO | Presentación del objetivo: Sistema de gestión para una tienda de mascotas con 4 archivos (`Mascota.java`, `Cliente.java`, `TiendaMascotas.java`, `Main.java`). |
| 01:46 - 05:13 | Clase `Mascota.java` y encapsulación | Editor OnlineGDB en la pestaña `Mascota.java`: atributos `private`, constructor con `this`, getters, `isDisponible()`, setters con validación, `mostrarInformacion()` y `adoptar()`. |
| 05:13 - 06:38 | Clase `Cliente.java` y separación de responsabilidades | Pestaña `Cliente.java`: atributos privados (`nombre`, `correo`, `edad`), constructor, getters, setters y `mostrarInformacion()`. |
| 06:38 - 10:28 | Clase `TiendaMascotas.java` (arreglos e interacción) | Pestaña `TiendaMascotas.java`: arreglo `Mascota[]` de tamaño `10`, contador `cantidad`, `registrarMascota()`, `mostrarMascotas()` y `registrarAdopcion()` con `equalsIgnoreCase`. |
| 10:28 - 13:08 | Clase `Main.java` (orquestación y prueba) | Pestaña `Main.java`: instanciación de tienda, creación de `Max`, `Michi` y `Luna`, registro, catálogo inicial, cliente `Carlos`, adopción de `Max` y catálogo actualizado. |
| 13:08 - 13:57 | Ejecución y análisis de resultados | Botón **Run** en OnlineGDB: lectura de la consola verificando que `Max` cambia a `Adoptada` mientras `Michi` y `Luna` permanecen `Disponible`. |
| 13:57 - 15:00 | Desafío práctico y conclusión | Reflexión final en pantalla sobre adopciones repetidas, nuevos registros y resumen de pilares de POO aplicados. |

---

## Guion Detallado de Locución

### [00:00 - 01:46] Introducción al Sistema de Tienda de Mascotas y Fundamentos de POO
**[En pantalla: Editor en línea OnlineGDB con lenguaje Java seleccionado y las cuatro pestañas del proyecto: `Main.java`, `Mascota.java`, `Cliente.java` y `TiendaMascotas.java`.]**

**Voz en off:**
> "Hola a todos. En esta lección vamos a desarrollar un pequeño sistema de gestión para una tienda de mascotas utilizando Java y los fundamentos de la programación orientada a objetos.
>
> Nuestro objetivo será construir un programa que permita registrar mascotas, almacenar información del cliente, consultar un catálogo y realizar adopciones. Para conseguirlo vamos a trabajar con tres clases principales: `Mascota`, `Cliente` y `TiendaMascotas`. Finalmente, tendremos una clase `Main` que permitirá ejecutar y probar nuestro programa.
>
> Antes de comenzar debemos comprender cómo se organiza un programa utilizando programación orientada a objetos. Una **clase** es un modelo que define las características y comportamientos de un elemento. Por ejemplo, podemos tener una clase `Mascota` que represente a todos los animales registrados, la cual tendrá un nombre, una especie, una edad y un estado de disponibilidad.
>
> Un **objeto**, por otro lado, es una instancia creada a partir de una clase. Esto significa que podemos crear diferentes mascotas utilizando el mismo modelo, pero asignándoles información distinta. En nuestro proyecto, `Max` será un objeto, `Michi` será otro objeto y `Luna` será un tercer objeto; todos pertenecen a la clase `Mascota`.
>
> También tendremos una clase `Cliente` para representar a las personas que desean adoptar, y una clase `TiendaMascotas` para administrar los registros y las adopciones. De esta manera, cada clase tendrá una responsabilidad específica y nuestro programa estará mejor organizado."

---

### [01:46 - 05:13] Creación de la clase `Mascota.java`
**[Acción en pantalla: Cambio a la pestaña `Mascota.java` en OnlineGDB, recorriendo los atributos privados, constructor, getters, setters y métodos de comportamiento.]**

**Voz en off:**
> "Ahora vamos a comenzar creando nuestra primera clase. Empezamos con el archivo `Mascota.java` y aquí declaramos nuestra clase utilizando la palabra reservada `class` seguida del nombre.
>
> Dentro de ella tenemos cuatro atributos que son `nombre`, `especie`, `edad` y `disponible`. Los dos primeros son de tipo `String` porque almacenan texto. La `edad` es de tipo `int` porque representa un número entero. Y finalmente `disponible` es de tipo `boolean` porque solamente puede tener dos valores: verdadero o falso. Por ejemplo, una mascota puede estar disponible para adopción o puede haber sido adoptada.
>
> Observen que todos los atributos están declarados como `private`. Eso significa que no podemos acceder directamente a ellos desde otras clases. Estamos protegiendo la información de nuestros objetos. A este principio se le conoce como **encapsulación**.
>
> Ahora vamos a observar el **constructor**. El constructor tiene el mismo nombre que la clase y no utiliza un tipo de retorno. Su función es inicializar los atributos cuando creamos una nueva mascota. En este caso recibe tres parámetros: `nombre`, `especie` y `edad`. Luego utilizamos la palabra `this` para asignar cada valor al atributo correspondiente. También establecemos `disponible` en `true`, porque cuando una mascota ingresa por primera vez a nuestra tienda todavía no ha sido adoptada. Por ejemplo, cuando creamos a `Max`, el programa guardará su nombre, su especie y su edad, y automáticamente lo marcará como disponible.
>
> Ahora tenemos los **getters**. Estos métodos nos permiten consultar los valores de nuestros atributos privados. Por ejemplo, `getNombre` devuelve el nombre de la mascota y `getEspecie` devuelve su especie. También tenemos `isDisponible`, que nos permite consultar si la mascota todavía puede ser adoptada. Noten que para los valores booleanos es habitual utilizar el prefijo `is` en lugar de `get`.
>
> Después encontramos los **setters**. Estos métodos permiten modificar determinados atributos de manera controlada. Por ejemplo, `setNombre` permite cambiar el nombre de una mascota. En `setEdad` agregamos una condición para comprobar que la nueva edad sea mayor o igual a cero. Si el valor no cumple esa condición, no se realiza la modificación. Esto es importante porque no queremos almacenar información incorrecta.
>
> Finalmente, tenemos dos métodos adicionales. El primero es `mostrarInformacion`, que muestra en consola los datos de nuestra mascota y su estado de disponibilidad. El segundo es `adoptar`, que cambia la disponibilidad a `false` cuando una mascota es adoptada. Así, nuestra primera clase ya representa un elemento real de nuestro sistema y contiene tanto sus características como sus comportamientos."

---

### [05:13 - 06:38] Creación de la clase `Cliente.java`
**[Acción en pantalla: Cambio a la pestaña `Cliente.java`, mostrando atributos privados, constructor, getters, setters y el método `mostrarInformacion()`.]**

**Voz en off:**
> "Ahora vamos a pasar al segundo archivo llamado `Cliente.java`. ¿Por qué necesitamos una segunda clase? Porque nuestra aplicación no solamente debe administrar animales, también necesita representar a las personas que realizan las adopciones.
>
> Aquí tenemos una clase llamada `Cliente`. Esta clase tiene tres atributos: `nombre`, `correo` y `edad`. Todos son privados porque queremos mantener la información protegida.
>
> Después agregamos el constructor, que recibe los tres datos necesarios para registrar a un cliente. Utilizamos nuevamente `this` para asignar los parámetros a sus respectivos atributos. Por ejemplo, cuando creamos un cliente llamado `Carlos`, podremos almacenar su correo electrónico y su edad.
>
> A continuación, agregamos los getters para consultar la información: tenemos `getNombre`, `getCorreo` y `getEdad`. También agregamos dos setters para modificar el nombre y el correo cuando sea necesario. Finalmente creamos el método `mostrarInformacion`, el cual imprimirá los datos del cliente en la consola.
>
> Observen que estamos siguiendo una estructura parecida a la de la clase `Mascota`. Esto es porque ambas clases representan entidades diferentes, pero utilizan conceptos comunes de programación orientada a objetos. Una ventaja de trabajar de esta manera es que cada clase se encarga únicamente de administrar su propia información. Por ejemplo, la clase `Cliente` no necesita saber cómo funciona el catálogo de mascotas y la clase `Mascota` no necesita administrar los correos de los clientes. Cada una tiene una responsabilidad definida."

---

### [06:38 - 10:28] Creación de la clase `TiendaMascotas.java`
**[Acción en pantalla: Cambio a la pestaña `TiendaMascotas.java`, desplazándose desde el arreglo `Mascota[]` y el constructor hasta `registrarMascota`, `mostrarMascotas` y `registrarAdopcion`.]**

**Voz en off:**
> "Ahora vamos a pasar con nuestra tercera clase llamada `TiendaMascotas.java`. Esta clase será la encargada de administrar el funcionamiento principal de nuestra tienda.
>
> Primero tenemos un atributo llamado `mascotas`, y ese atributo es un arreglo (`array`) de tipo `Mascota`. ¿Qué significa esto? Significa que podemos almacenar varios objetos de nuestra clase `Mascota` dentro de una misma estructura. En nuestro caso, el arreglo tendrá una capacidad máxima de 10 mascotas. También tenemos una variable llamada `cantidad`, que nos permitirá conocer cuántas mascotas hemos registrado realmente.
>
> Después encontraremos el constructor de `TiendaMascotas`. Ese constructor se ejecuta cuando creamos la tienda. Aquí inicializamos el arreglo con 10 posiciones y establecemos la cantidad inicial en cero, porque todavía no hemos registrado ningún animal.
>
> Ahora vamos por el método `registrarMascota`. Este método recibe como parámetro un objeto de tipo `Mascota`. Primero comprueba si todavía tenemos espacio disponible dentro del arreglo: si la `cantidad` de mascotas registradas es menor que la longitud del arreglo, guardamos el objeto en la posición `mascotas[cantidad]`. Después incrementamos la variable `cantidad` en uno y finalmente mostramos un mensaje indicando que el registro fue exitoso. Si ya no tenemos espacio, mostramos un mensaje informando que la tienda está llena. De esta manera, podemos registrar diferentes mascotas sin tener que crear una variable independiente para cada registro dentro de la clase administradora.
>
> Ahora tenemos el método `mostrarMascotas`. Este método nos permitirá visualizar todo el catálogo de nuestra tienda. Primero mostramos un encabezado y después utilizamos un bucle `for`. El bucle comienza desde cero y continúa mientras la variable `i` sea menor que `cantidad`. Eso significa que solamente recorremos las posiciones que realmente contienen mascotas registradas. Dentro del bucle, mostramos el número de mascota y llamamos al método `mostrarInformacion` de cada objeto. También mostramos una línea divisoria para que los resultados sean más fáciles de leer.
>
> Finalmente, tenemos el método `registrarAdopcion`. Este es uno de los métodos más importantes de nuestro proyecto porque conecta las tres clases. Recibe dos parámetros: el nombre de la mascota que queremos adoptar y un objeto de tipo `Cliente`. Primero recorremos el arreglo utilizando otro bucle `for`. En cada posición comparamos el nombre que recibimos con el nombre de la mascota almacenada, y para realizar esa comparación utilizamos `equalsIgnoreCase`. Este método permite comparar textos sin distinguir entre mayúsculas y minúsculas; por ejemplo, `"MAX"` y `"Max"` serán considerados iguales.
>
> Si encontramos la mascota, comprobamos si todavía está disponible utilizando `isDisponible`. Si está disponible, ejecutamos el método `adoptar` para cambiar su estado. Después mostramos un mensaje indicando que la adopción fue exitosa junto con el nombre del cliente y el nombre de la mascota. Si la mascota ya fue adoptada, mostramos un mensaje informativo. Y si terminamos de recorrer el arreglo sin encontrarla, mostramos un mensaje indicando que la mascota no existe en nuestro catálogo.
>
> Como pueden observar, esta clase utiliza objetos de otras clases para administrar las operaciones de la tienda. Esto demuestra cómo podemos organizar diferentes responsabilidades y hacer que nuestras clases trabajen en conjunto."

---

### [10:28 - 13:08] Construcción del programa principal en `Main.java`
**[Acción en pantalla: Cambio a la pestaña `Main.java`, mostrando el método `main` línea por línea.]**

**Voz en off:**
> "Ahora que tenemos nuestras tres clases, vamos a pasar al último archivo: `Main.java`. Este archivo es donde vamos a ejecutar y comprobar el funcionamiento de nuestro sistema.
>
> Primero tenemos el método `main`, que es el punto de entrada de nuestra aplicación Java. Comenzamos creando un objeto llamado `tienda` utilizando la clase `TiendaMascotas`. Para hacerlo utilizamos la palabra `new`, que permite crear una nueva instancia.
>
> Después crearemos tres objetos de tipo `Mascota`. El primero será `Max`, que es un perro de 3 años. El segundo será `Michi`, que es un gato de 2 años. Y el tercero será `Luna`, una coneja de 1 año. Observamos que todos se van creando utilizando el mismo constructor, pero reciben información diferente.
>
> Después utilizamos el objeto `tienda` para llamar al método `registrarMascota` tres veces. Con esto las tres mascotas quedan almacenadas en el arreglo de la tienda. A continuación llamamos al método `mostrarMascotas` para visualizar nuestro catálogo inicial.
>
> Luego creamos un objeto de tipo `Cliente` llamado `Carlos`, le asignamos un correo electrónico como `carlos@gmail.com` y una edad de 20 años. También llamamos a `mostrarInformacion` para mostrar sus datos.
>
> Finalmente, ejecutamos una adopción: utilizamos `registrarAdopcion` y enviamos el nombre `"Max"` junto con el objeto `cliente1`. Esto significa que `Carlos` está realizando la adopción de `Max`. El programa buscará a `Max` dentro del catálogo, comprobará que esté disponible y cambiará su estado a adoptado. Después volvemos a llamar a `mostrarMascotas`; esto es importante porque podremos comprobar que el estado de `Max` ha cambiado mientras que `Michi` y `Luna` continúan disponibles."

---

### [13:08 - 13:57] Ejecución y verificación en consola
**[Acción en pantalla: Clic en el botón `Run` en OnlineGDB y desplazamiento por la consola de salida inferior.]**

**Voz en off:**
> "Vamos a verificarlo en esta ejecución. Como observamos, se registran las tres mascotas correctamente y aparece el catálogo inicial con sus respectivos nombres, especies, edades y estados disponibles.
>
> Lo siguiente que se muestra son los datos del cliente `Carlos`. Luego vemos el mensaje de adopción exitosa donde se indica que `Carlos` ha adoptado a `Max`. Y finalmente se vuelve a mostrar el catálogo. Aquí podemos comprobar algo importante: `Max` ahora aparece como `Adoptada`, mientras que `Michi` y `Luna` siguen `Disponible`. Esto demuestra que nuestro programa no solamente almacena información, sino que también permite modificar el estado de los objetos según las operaciones que realizamos."

---

### [13:57 - 15:00] Desafío propuesto y cierre de la lección
**[En pantalla: Consola final de OnlineGDB y código de `Main.java`.]**

**Voz en off:**
> "Y antes de terminar, les propongo un pequeño desafío: ¿qué sucedería si intentamos adoptar nuevamente a `Max`? El programa debería indicar que esa mascota ya fue adoptada porque su atributo `disponible` ahora tiene el valor `false`, ya que es un booleano. También podemos intentar registrar una nueva mascota, cambiar los datos de un cliente o agregar más animales al catálogo. De esa manera podemos experimentar con el código y comprender mejor cómo se relacionan las diferentes clases.
>
> Y para concluir, en esta lección construimos una aplicación sencilla utilizando programación orientada a objetos. Aprendimos a crear clases, definir atributos y métodos, utilizar constructores, aplicar encapsulación mediante getters y setters, crear objetos y relacionarlos entre sí. También utilizamos arreglos para almacenar varios objetos y bucles para recorrerlos.
>
> Lo más importante es comprender que podemos dividir un programa en diferentes clases, asignar responsabilidades a cada una y conseguir que trabajen juntas para resolver un problema. Muchas gracias por su atención."
