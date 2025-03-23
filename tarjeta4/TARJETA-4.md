#### ESTRUCTURA 4  
# CONTROL DE FLUJO

1. **Describa el por qué y para qué se utiliza.**

En Kotlin, los controles de flujo son estructuras que permiten tomar decisiones y ejecutar diferentes bloques de código según ciertas condiciones.

**¿Por qué que se usan?:**
Porque permiten que un programa no sea lineal y pueda adaptarse a diferentes situaciones dependiendo de los datos de entrada o el contexto.

**¿Para qué sirven?:**
Para evaluar condiciones y ejecutar acciones específicas según el resultado. 

**Los principales controles de flujo en Kotlin son:**
- if (condicional simple) → Evalúa una condición y ejecuta un bloque si es verdadera.
- if-else (condicional con alternativa) → Si la condición es falsa, ejecuta otro bloque de código.
- if-else if-else (múltiples condiciones) → Permite evaluar varias condiciones en cadena.
- when (alternativa a if-else if-else) → Más estructurado cuando hay muchas opciones posibles.



2. **Genere un ejemplo internamente en el recuadro.**  
   - Utilice un editor de código para lograrlo.  

```kotlin
// EJEMPLO EN CÓDIGO KOTLIN

fun main() {
    // Estudiante 1 - Evaluado con 'if-else'
    val nombre1 = "Carlos Pérez"
    var nota1 = 2.5
    var aprobo1: Boolean

    if (nota1 >= 3.0) {
        aprobo1 = true
    } else {
        aprobo1 = false
    }

    println("\n--- Estudiante 1 ---")
    println("Nombre: $nombre1")
    println("Nota: $nota1")
    println("¿Aprobó? $aprobo1")

    // Estudiante 2 - Evaluado con 'if-else if-else'
    val nombre2 = "Ana Gómez"
    var nota2 = 3.8
    var rendimiento2: String

    if (nota2 >= 4.5) {
        rendimiento2 = "Excelente"
    } else if (nota2 >= 4.0) {
        rendimiento2 = "Muy Bueno"
    } else if (nota2 >= 3.0) {
        rendimiento2 = "Bueno"
    } else if (nota2 >= 2.0) {
        rendimiento2 = "Insuficiente"
    } else {
        rendimiento2 = "Deficiente"
    }

    println("\n--- Estudiante 2 ---")
    println("Nombre: $nombre2")
    println("Nota: $nota2")
    println("Rendimiento: $rendimiento2")

    // Estudiante 3 - Evaluado con 'when'
    val nombre3 = "Luis Rodríguez"
    var nota3 = 4.7

    val rendimiento3 = when {
        nota3 >= 4.5 -> "Excelente"
        nota3 >= 4.0 -> "Muy Bueno"
        nota3 >= 3.0 -> "Bueno"
        nota3 >= 2.0 -> "Insuficiente"
        else -> "Deficiente"
    }

    println("\n--- Estudiante 3 ---")
    println("Nombre: $nombre3")
    println("Nota: $nota3")
    println("Rendimiento: $rendimiento3")
}


```

---

### CREAR ALGORITMO PROPIO Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](https://github.com/Beltran18/Kotlin/blob/34bf201531fbec093f50bffcecaef06e06acf669/tarjeta4/audio-tarjeta4.ogg)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](https://github.com/Beltran18/Kotlin/blob/d0954c207715a25076b790a3bdaa720c2c26c71c/tarjeta4/img-tarjeta4.PNG)**  

---

### Algoritmo creado y explicación de cómo funciona la estructura  

```kotlin
// EJERCICO CREADO EN CÓDIGO KOTLIN

fun main() {
    // Ingresos del usuario
    val ingresos: Double = 4_200_000.0  // Cambia este valor para probar diferentes casos

    // Variable para almacenar el impuesto a pagar (mutable porque cambiará según la condición)
    var impuesto: Double = 0.0  

    // Verificación inicial con 'if-else' para saber si debe pagar impuestos
    if (ingresos < 1_000_000) {
        println("No debe pagar impuestos.")  // Si gana menos de $1,000,000, no paga nada
    } else {
        println("Debe pagar impuestos.")  // Si gana más de $1,000,000, aplicamos las tasas correspondientes
    }

    // Cálculo del impuesto con 'if-else if-else'
    if (ingresos >= 1_000_000 && ingresos <= 3_000_000) {
        impuesto = ingresos * 0.10  // 10% de impuestos
    } else if (ingresos > 3_000_000 && ingresos <= 5_000_000) {
        impuesto = ingresos * 0.15  // 15% de impuestos
    } else if (ingresos > 5_000_000) {
        impuesto = ingresos * 0.20  // 20% de impuestos
    }

    // Mostrar el impuesto calculado
    println("Impuesto a pagar: $$impuesto")

    // Clasificación del nivel de impuestos con 'when'
    val nivelImpuesto = when {
        impuesto == 0.0 -> "No aplica impuestos"
        impuesto <= 300_000 -> "Bajo"
        impuesto <= 750_000 -> "Medio"
        else -> "Alto"
    }

    // Mostrar el nivel de impuestos
    println("Nivel de impuesto: $nivelImpuesto")
}


```

