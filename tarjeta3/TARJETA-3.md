#### ESTRUCTURA 3
# FUNCIONES DE STRINGS Y PRINTING

1. **Describa el por qué y para qué se utiliza.**
Las funciones de strings y printing en Kotlin son esenciales para manejar y mostrar texto de manera eficiente en aplicaciones. Las funciones de strings permiten manipular, transformar y analizar texto, lo que resulta útil en situaciones como validar correos electrónicos, extraer información de mensajes o formatear datos antes de mostrarlos. Por otro lado, las funciones de impresión (print, println, printf) se utilizan para mostrar información en la consola, lo cual es clave para depurar programas, generar reportes o interactuar con el usuario en aplicaciones de línea de comandos. Por ejemplo, al desarrollar una aplicación de chat, se pueden usar funciones de string para procesar los mensajes y funciones de impresión para mostrar conversaciones en la pantalla. También, en un sistema de reportes financieros, se pueden formatear números y textos antes de imprimirlos en pantalla o en archivos de salida.

**Tipos de Funciones de String:**
- Funciones de transformación:
convierte texto a otro formato.
Ejemplo: Convertir un texto a mayúsculas o minúsculas.
Ejemplos: toUpperCase(), toLowerCase(), capitalize(), decapitalize()

- Funciones de manipulación
Modifican el contenido del string.
Ejemplo: Eliminar espacios en blanco o reemplazar palabras en una frase.
Ejemplos: trim(), replace(), removePrefix(), removeSuffix(), padStart(), padEnd()

- Funciones de búsqueda y comparación
Permiten encontrar y comparar texto dentro de un string.
Ejemplo: Buscar si una palabra está dentro de un mensaje o comparar nombres de usuarios.
Ejemplos: contains(), startsWith(), endsWith(), indexOf(), lastIndexOf(), equals(), compareTo()

- Funciones de extracción y división
Extraen o dividen texto en partes.
Ejemplo: Obtener el dominio de un correo electrónico o dividir una oración en palabras.
Ejemplos: substring(), split(), chunked(), slice()

- Funciones de validación y análisis
Determinan el tipo de contenido en un string.
Ejemplo: Verificar si un input de usuario es un número o una letra.
Ejemplos: isEmpty(), isNotEmpty(), isBlank(), isNotBlank(), matches()

**Tipos de Funciones de Printing:**
- Impresión básica
Muestra texto en la consola sin formato especial.
Ejemplos: print(), println()

- Impresión formateada
Permite personalizar la salida con valores dinámicos.
Ejemplos: printf() (similar a printf en C), format()

- Interpolación de Strings (String Templates)
Inserta valores dentro de un texto usando $ o ${}.
Ejemplos: "Hola, $nombre!", "El resultado es ${a + b}"


2. **Genere un ejemplo internamente en el recuadro.**  
   - Utilice un editor de código para lograrlo.  

```kotlin
// EJEMPLO EN CÓDIGO KOTLIN

fun main() {
    print("Ingrese su nombre");
    val nombre = readln() ?: ""

    val nombreMa: String = nombre.uppercase();
    val longitudN: Int = nombre.length

    println("-----\nTu nombre en mayusculas es: $nombreMa");
    println("-----\nTu nombre tiene: $longitudN caracteres");
}


```

---

### CREAR ALGORITMO PROPIO Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](https://github.com/Beltran18/Kotlin/blob/beb2dc12fb0ebcc7ef5fa44f7ba7ed77a11bd0b3/tarjeta1/audio-tarjeta1.ogg)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](https://github.com/Beltran18/Kotlin/blob/4786c503181391eb065b9ea962e2a517275d4359/tarjeta1/img-tarjeta3.jpg)**  

---

### Algoritmo creado y explicación de cómo funciona la estructura  

```kotlin
// EJERCICO CREADO EN CÓDIGO KOTLIN

fun main() {
    fun main() {
    // Solicitar al usuario que ingrese una palabra
    print("Ingresa una palabra: ")  // print() para que el cursor quede en la misma línea
    val palabra = readLine() ?: ""  // Captura la entrada del usuario

    // Reemplazar la vocal 'a' por '@'
    val palabraModificada = palabra.replace('a', '@')

    // Mostrar los resultados con println
    println("\nPalabra modificada: $palabraModificada")
}
}


```
