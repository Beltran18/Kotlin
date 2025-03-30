#### ESTRUCTURA 7  
# LOOPERS, BUCLES

1. **Describa el por qué y para qué se utiliza.**

En Kotlin, un bucle es una estructura de control que permite ejecutar un bloque de código varias veces, dependiendo de una condición. En lugar de escribir el mismo código repetidamente, los bucles nos permiten automatizar tareas repetitivas de manera eficiente.

**Kotlin nos ofrece tres tipos principales de bucles:**
- for → Se usa cuando sabemos cuántas veces queremos repetir una acción, como recorrer una lista o un rango de números.
- while → Se ejecuta mientras se cumpla una condición específica. No sabemos exactamente cuántas veces se repetirá, solo que continuará hasta que la condición sea falsa.
- do-while → Es similar a while, pero con una diferencia clave: el bloque de código se ejecuta al menos una vez, incluso si la condición es falsa desde el principio.

**¿Para qué se usan los bucles?:**
Los bucles son esenciales en la programación porque nos ayudan a:
- Recorrer elementos en listas, arreglos o rangos de números.
- Ejecutar tareas repetitivas como cálculos, validaciones o simulaciones.
- Esperar una condición específica antes de continuar (por ejemplo, pedir datos hasta que sean correctos).
- Optimizar código, evitando la repetición manual de instrucciones.

Cada tipo de bucle es útil en diferentes escenarios, y la elección depende de la situación que queremos resolver.



2. **Genere un ejemplo internamente en el recuadro.**  
   - Utilice un editor de código para lograrlo.  

```kotlin
// EJEMPLO EN CÓDIGO KOTLIN

fun main() {
    // Ejemplo de uso de val y var
    val nombre = "Samuel"  // No se puede cambiar
    var edad = 17          // Se puede modificar

    println("Nombre: $nombre")
    println("Edad: $edad")

    edad = 18  // Se puede cambiar porque es 'var'
    println("Nueva edad: $edad")

    // Ejemplo con diferentes tipos de datos
    val altura: Double = 1.78
    val esEstudiante: Boolean = false
    val inicial: Char = 'S'

    println("Altura: $altura metros")
    println("¿Es estudiante? $esEstudiante")
    println("Inicial del nombre: $inicial")
}


```

---

### CREAR ALGORITMO PROPIO Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](https://github.com/Beltran18/Kotlin/blob/beb2dc12fb0ebcc7ef5fa44f7ba7ed77a11bd0b3/tarjeta1/audio-tarjeta1.ogg)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](https://github.com/Beltran18/Kotlin/blob/4786c503181391eb065b9ea962e2a517275d4359/tarjeta1/img-tarjeta1.png)**  

---

### Algoritmo creado y explicación de cómo funciona la estructura  

```kotlin
// EJERCICO CREADO EN CÓDIGO KOTLIN

fun main() {
    // Declaración de variables inmutables (val) porque su valor no cambia
    val nombre: String = "Juan Pérez"  // Nombre del estudiante (inmutable)
    val edad: Int = 20                 // Edad del estudiante (inmutable)
    val estatura: Double = 1.75         // Estatura del estudiante en metros (inmutable)

    // Declaración de variables mutables (var) porque su valor puede cambiar
    var nota: Double = 2.0      // Nota inicial del estudiante (mutable)
    var aprobo: Boolean = false // Estado inicial de aprobación (mutable)

    // Mostrar los datos iniciales del estudiante
    println("Nombre: $nombre")         // Se imprime el nombre del estudiante
    println("Edad: $edad años")        // Se imprime la edad del estudiante
    println("Estatura: $estatura m")   // Se imprime la estatura del estudiante
    println("Nota inicial: $nota")     // Se imprime la nota inicial del estudiante
    println("¿Aprobó? $aprobo")        // Se imprime si el estudiante aprobó o no

    // Cambio de valores en las variables mutables
    nota = 4.0    // Se actualiza la nota del estudiante
    aprobo = true // Se actualiza el estado de aprobación

    // Mostrar los datos después del cambio de nota
    println("\n--- Actualización de datos ---")
    println("Nueva nota: $nota")     // Se imprime la nueva nota
    println("¿Aprobó ahora? $aprobo") // Se imprime si ahora aprobó
}


```
