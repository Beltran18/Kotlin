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
    // Bucle 'for': Recorre un rango de 1 a 5
    println("Bucle 'for':")
    for (i in 1..5) {
        println(i)
    }

    println("\nBucle 'while':")
    var j = 1
    while (j <= 5) {
        println(j)
        j++ // Incremento para evitar bucle infinito
    }

    println("\nBucle 'do-while':")
    var k = 1
    do {
        println(k)
        k++ // Incremento para evitar bucle infinito
    } while (k <= 5)
}


```

---

### CREAR ALGORITMO PROPIO Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](https://github.com/Beltran18/Kotlin/blob/7ecd1a11544349e04f222de187eab3ab6a4be5f0/tarjeta7/audio-tarjeta7.ogg)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](https://github.com/Beltran18/Kotlin/blob/3fc875cb40dcf84f3f4e122151e654aa71877232/tarjeta7/img-tarjeta7.PNG)**  

---

### Algoritmo creado y explicación de cómo funciona la estructura  

```kotlin
// EJERCICO CREADO EN CÓDIGO KOTLIN

fun main() {
    // -------------------------
    // Bucle 'for': Sumar los números del 1 al 5
    // -------------------------
    var suma = 0 // Variable para almacenar la suma
    for (i in 1..5) { // Iteramos del 1 al 5
        suma += i // Sumamos el valor de i a la variable suma
    }
    println("Suma de los números del 1 al 5: $suma")

    // -------------------------
    // Bucle 'while': Contar números impares del 1 al 10
    // -------------------------
    var contador = 1 // Empezamos en 1
    var impares = 0 // Contador de números impares
    while (contador <= 10) { // Mientras el número sea menor o igual a 10
        if (contador % 2 != 0) { // Verificamos si es impar
            impares++ // Aumentamos el contador de impares
        }
        contador++ // Incrementamos el número
    }
    println("Cantidad de números impares entre 1 y 10: $impares")

    // -------------------------
    // Bucle 'do-while': Multiplicar los números del 1 al 5
    // -------------------------
    var producto = 1 // Variable para almacenar la multiplicación
    var num = 1 // Empezamos en 1
    do {
        producto *= num // Multiplicamos el número actual por el producto
        num++ // Incrementamos el número
    } while (num <= 5) // Se repite mientras num sea menor o igual a 5
    println("Multiplicación de los números del 1 al 5: $producto")
}


```
