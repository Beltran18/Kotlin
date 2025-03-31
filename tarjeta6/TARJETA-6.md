#### ESTRUCTURA 6
# COLLECTIONS, JSON Y MANEJO DE DATOS EN KOTLIN

1. **Describa el por qué y para qué se utiliza.**
En Kotlin, Collections, JSON y el manejo de datos son fundamentales para trabajar con información de manera estructurada y eficiente. Cada uno tiene un propósito específico en el desarrollo de aplicaciones.

**Collections en Kotlin**
- ¿Por qué se utilizan?
Permiten almacenar, organizar y manipular datos de manera estructurada.
Facilitan el acceso a grandes volúmenes de datos sin necesidad de variables individuales.
Optimizan el rendimiento y reducen la complejidad del código.

- ¿Para qué se utilizan?
Listas (List): Para manejar datos ordenados, como nombres de usuarios en un sistema.
Conjuntos (Set): Para evitar duplicados, como una lista de categorías únicas en una tienda en línea.
Mapas (Map): Para asociar claves y valores, como un diccionario de precios de productos.

**JSON en Kotlin**
- ¿Por qué se utiliza?
Es el formato estándar para intercambiar datos entre aplicaciones web, móviles y APIs.
Es ligero, fácil de leer y escribir.
Kotlin permite manejar JSON de forma sencilla con librerías como kotlinx.serialization, Gson y Moshi.

- ¿Para qué se utiliza?
Comunicación con APIs REST para enviar y recibir datos estructurados.
Almacenamiento de configuraciones en archivos JSON.
Intercambio de datos entre aplicaciones o sistemas.

**Manejo de Datos en Kotlin**
- ¿Por qué se utiliza?
Permite guardar, recuperar y modificar datos de forma persistente.
Facilita la gestión de información en archivos o bases de datos.
Es clave para el desarrollo de aplicaciones que necesitan almacenamiento a largo plazo.

- ¿Para qué se utiliza?
Lectura y escritura de archivos, como logs o reportes en txt o csv.
Bases de datos SQLite o SQL Server, por ejemplo, con Room o Exposed.
Gestión de usuarios y configuraciones, guardando datos en archivos locales o en la nube.

2. **Genere un ejemplo internamente en el recuadro.**  
   - Utilice un editor de código para lograrlo.  

```kotlin
// EJEMPLO EN CÓDIGO KOTLIN
import kotlinx.serialization.*
import kotlinx.serialization.json.*

@Serializable
data class Usuario(val id: Int, val nombre: String, val correo: String)

fun main() {
    val usuarios = mutableListOf<Usuario>()

    // Agregar usuarios a la lista
    usuarios.add(Usuario(1, "Juan Pérez", "juan@example.com"))
    usuarios.add(Usuario(2, "María López", "maria@example.com"))

    // Convertir la lista a JSON
    val jsonUsuarios = Json.encodeToString(usuarios)
    println("Usuarios en formato JSON:\n$jsonUsuarios")

    // Buscar un usuario por ID
    val usuarioEncontrado = usuarios.find { it.id == 2 }
    println("\nUsuario encontrado: $usuarioEncontrado")

    // Convertir JSON a lista de objetos
    val nuevaListaUsuarios = Json.decodeFromString<List<Usuario>>(jsonUsuarios)
    println("\nLista recuperada desde JSON:")
    nuevaListaUsuarios.forEach { println(it) }
}


```

---

### CREAR ALGORITMO PROPIO Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](https://github.com/Beltran18/Kotlin/blob/beb2dc12fb0ebcc7ef5fa44f7ba7ed77a11bd0b3/tarjeta6/tarjeta6.opus)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](https://github.com/Beltran18/Kotlin/blob/f48ee7ac9fb3e43d8c83de9df967d8ac72cf249a/tarjeta6/img-tarjeta6.jpg)**  

---

### Algoritmo creado y explicación de cómo funciona la estructura  

```kotlin
// EJERCICO CREADO EN CÓDIGO KOTLIN
// Importamos las librerías necesarias
import kotlinx.serialization.*
import kotlinx.serialization.json.*

/**
 * Definimos un modelo de datos para representar una tarea
 */
@Serializable  // Permite que la clase se pueda convertir a JSON
data class Tarea(
    val nombre: String,         // Nombre de la tarea
    val descripcion: String,    // Descripción breve
    val completada: Boolean     // Estado de la tarea (true = completada, false = pendiente)
)

fun main() {
    // Creamos una lista mutable de tareas
    val listaTareas = mutableListOf(
        Tarea("Comprar leche", "Ir al supermercado y comprar leche", false),
        Tarea("Hacer ejercicio", "Correr 30 minutos en el parque", true),
        Tarea("Estudiar Kotlin", "Repasar programación en Kotlin", false)
    )

    // Convertimos la lista de tareas a JSON usando kotlinx.serialization
    val json = Json.encodeToString(listaTareas)
    
    // Mostramos el JSON generado
    println("Lista de tareas en JSON:")
    println(json)

    // Simulamos recuperar los datos desde JSON y convertirlos nuevamente a objetos Kotlin
    val tareasRecuperadas: List<Tarea> = Json.decodeFromString(json)

    // Mostramos las tareas recuperadas
    println("\nTareas recuperadas desde JSON:")
    tareasRecuperadas.forEach { tarea ->
        println("Nombre: ${tarea.nombre}, Descripción: ${tarea.descripcion}, Completada: ${tarea.completada}")
    }
}



```
