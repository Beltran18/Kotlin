#### ESTRUCTURA 2
# OPERADORES MATH LOGICOS 

1. **Describa el por qué y para qué se utiliza.**
En Kotlin, los operadores matemáticos y lógicos son herramientas fundamentales que permiten realizar cálculos y tomar decisiones dentro de un programa.
Los operadores matemáticos se utilizan para realizar operaciones aritméticas sobre valores numéricos, como suma, resta, multiplicación y división. Estos operadores son esenciales en cálculos financieros, algoritmos matemáticos, procesamiento de datos y muchas otras aplicaciones.

**Tipos de operadores matemáticos en Kotlin:**

-Suma (+) → Permite sumar dos valores numéricos.

-Resta (-) → Resta un valor de otro.

-Multiplicación (*) → Multiplica dos valores.

-División (/) → Divide un número entre otro.

-Módulo (%) → Devuelve el residuo de una división.

**Tipos de operadores lógicos en Kotlin** 

-AND lógico (&&) → Devuelve true solo si ambas condiciones son verdaderas.

-OR lógico (||) → Devuelve true si al menos una condición es verdadera.

-NOT lógico (!) → Invierte el valor de una condición (true a false y viceversa).

2. **Genere un ejemplo internamente en el recuadro.**  
   - Utilice un editor de código para lograrlo.

```kotlin
// EJEMPLO EN CÓDIGO KOTLIN
fun main() {
    val numero1: Int = 20
    val numero2: Int = 10
    val suma = numero1 + numero2
    val resta = numero1 - numero2
    val multiplicacion = numero1 * numero2
    val division = numero1 / numero2
    val modulo = numero1 % numero2
    
    println("Suma: $suma")
    println("Resta: $resta")
    println("Multiplicación: $multiplicacion")
    println("División: $division")
    println("Módulo: $modulo")
    
    val esMayor = numero1 > numero2
    val esMenor = numero1 < numero2
    val sonIguales = numero1 == numero2
    
    println("Número 1 es mayor que Número 2: $esMayor")
    println("Número 1 es menor que Número 2: $esMenor")
    println("Número 1 es igual a Número 2: $sonIguales")
    
    val resultado = (numero1 + numero2) > 25 && (numero1 - numero2) < 15
    println("¿La suma es mayor a 25 y la resta menor a 15? $resultado")
}

```

---

### CREAR ALGORITMO PROPIO Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](https://github.com/Beltran18/Kotlin/blob/beb2dc12fb0ebcc7ef5fa44f7ba7ed77a11bd0b3/tarjeta1/audio-tarjeta1.ogg)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB]https://github.com/Beltran18/Kotlin/blob/main/tarjeta2/imagen-tarjeta2.jpg?raw=true**  

---

### Algoritmo creado y explicación de cómo funciona la estructura  

```kotlin
// EJERCICO CREADO EN CÓDIGO KOTLIN
fun main() {
    val a = 8  // Variable entera con valor 8
    val b = 4  // Variable entera con valor 4
    
    val suma = a + b  // Suma de a y b
    println("Suma: $suma")
    
    val esMayor = a > b  // Comprueba si a es mayor que b
    println("¿A es mayor que B?: $esMayor")
    
    val condicion = (suma > 10) && esMayor  // Verifica si la suma es mayor que 10 y si a es mayor que b
    println("¿La suma es mayor a 10 y A es mayor que B?: $condicion")
}
```
