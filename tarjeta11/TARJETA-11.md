#### ESTRUCTURA 1  
# Manejo de archivos

1. **Describa el por qué y para qué se utiliza.**
   
El manejo de archivos en Kotlin se utiliza para leer, escribir, crear, modificar o eliminar archivos desde un programa, permitiendo así almacenar información de manera persistente. Es útil cuando se desea guardar datos que deben permanecer incluso después de cerrar el programa, como registros, configuraciones o resultados de procesos.

Se puede trabajar con archivos de texto simples (.txt) o incluso archivos más complejos. Kotlin facilita esto mediante sus funciones integradas y la interoperabilidad con Java, utilizando clases como File del paquete java.io.

**Tipos de Variables:**

val: Define una variable inmutable (su valor no puede cambiar después de asignarse).

var: Define una variable mutable (puede cambiar su valor posteriormente).

**Tipos de Datos en Kotlin**

String: Cadenas de texto ("Hola")

Int: Números enteros (1, 20, -10)

Double: Números decimales (3.14, 1.78)

Boolean: Valores lógicos (true, false)

Char: Un solo carácter ('A', 'b')

Float, Long, Short, Byte: Otros tipos numéricos

2. **Genere un ejemplo internamente en el recuadro.**  
   - Utilice un editor de código para lograrlo.  

```kotlin
// EJEMPLO EN CÓDIGO KOTLIN

import java.io.File

fun main() {
    // Crear un archivo y escribir texto
    val archivo = File("datos.txt")
    archivo.writeText("Hola, este es un archivo creado con Kotlin.\n")
    archivo.appendText("Añadimos una segunda línea.")

    // Leer el contenido del archivo
    val contenido = archivo.readText()
    println("Contenido del archivo:\n$contenido")
}


```

---

### CREAR ALGORITMO PROPIO Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](https://github.com/Beltran18/Kotlin/blob/2c7aa2d559b56b7eb53d085b93300b6986bed734/tarjeta11/audio-tarjeta11.ogg)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](https://github.com/Beltran18/Kotlin/blob/ffb30c3882e26553d03d10c806900bbb94de1c31/tarjeta11/img-tarjeta11.jpg)**  

---

### Algoritmo creado y explicación de cómo funciona la estructura  

```kotlin
// EJERCICIO CREADO EN CÓDIGO KOTLIN

import java.io.File

fun main() {
    // Paso 1: Declaramos el nombre del archivo
    val nombreArchivo = "registro_estudiante.txt"

    // Paso 2: Creamos el contenido con los datos del estudiante
    val contenido = """
        Nombre: Ana Torres
        Edad: 22
        Carrera: Ingeniería en Sistemas
        Promedio: 4.3
    """.trimIndent()

    // Paso 3: Escribimos el contenido al archivo
    val archivo = File(nombreArchivo)
    archivo.writeText(contenido)

    // Paso 4: Leemos y mostramos el contenido del archivo
    val resultado = archivo.readText()
    println("Contenido guardado en el archivo:\n$resultado")
}



```
