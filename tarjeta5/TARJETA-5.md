#### ESTRUCTURA 5  
# ESTRUCTURAS DE DECISIÓN, CONTROL Y MANEJO DE ERRORES
1. **Describa el por qué y para qué se utiliza.**

En Kotlin, las estructuras de decisión y control permiten modificar el flujo de ejecución de un programa según condiciones o iteraciones.

**Tipos de Control de Flujo:**
- Estructuras de Decisión:
  - if, else if, else: Evalúan condiciones y ejecutan bloques de código según el resultado.
  - when: Alternativa más potente que if-else if-else, ideal para múltiples condiciones.

- Estructuras de Control de Ciclos:
  - for: Recorre rangos, listas, matrices o cualquier colección iterable.
  - while: Ejecuta un bloque de código mientras se cumpla una condición.
  - do-while: Similar a while, pero garantiza al menos una ejecución.

- Manejo de Errores:
  - try-catch-finally: Permite capturar excepciones para evitar que el programa falle inesperadamente.
  - throw: Permite lanzar excepciones de manera explícita.

2. **Genere un ejemplo internamente en el recuadro.**  
   - Utilice un editor de código para lograrlo.  

```kotlin
// EJEMPLO EN CÓDIGO KOTLIN

fun main() {
    // Estructura de decisión con 'if-else'
    val numero = 10
    if (numero > 0) {
        println("El número es positivo")
    } else {
        println("El número es negativo o cero")
    }

    // Estructura de decisión con 'when'
    val dia = 3
    val nombreDia = when(dia) {
        1 -> "Lunes"
        2 -> "Martes"
        3 -> "Miércoles"
        4 -> "Jueves"
        5 -> "Viernes"
        6 -> "Sábado"
        7 -> "Domingo"
        else -> "Día inválido"
    }
    println("Día seleccionado: $nombreDia")

    // Control de ciclo con 'for'
    for (i in 1..5) {
        println("Iteración: $i")
    }

    // Manejo de errores con 'try-catch'
    try {
        val resultado = 10 / 0
        println("Resultado: $resultado")
    } catch (e: ArithmeticException) {
        println("Error: División por cero")
    } finally {
        println("Bloque 'finally' ejecutado")
    }
}


```

---

### CREAR ALGORITMO PROPIO Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](https://github.com/Beltran18/Kotlin/blob/beb2dc12fb0ebcc7ef5fa44f7ba7ed77a11bd0b3/tarjeta1/audio-tarjeta1.ogg)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](https://github.com/Beltran18/Kotlin/blob/c8a2b17e95d069e22a0259a270ce53790f7ea2bd/tarjeta5/imagen-tarjeta5.jpg)**  

---

### Algoritmo creado y explicación de cómo funciona la estructura  

```kotlin
// EJERCICO CREADO EN CÓDIGO KOTLIN

fun main() {
    // Declaración de una variable entera
    val edad = 20
    
    // Verificación de la mayoría de edad usando una estructura de decisión 'if-else'
    if (edad >= 18) {
        println("Eres mayor de edad")  // Imprime si la condición se cumple
    } else {
        println("Eres menor de edad")  // Imprime si la condición no se cumple
    }

    // Manejo de errores con 'try-catch'
    try {
        val resultado = 10 / 2  // Realiza una división válida
        println("Resultado de la división: $resultado")
    } catch (e: ArithmeticException) {
        println("Error: División inválida")  // Se ejecuta si ocurre un error
    }
}


```
