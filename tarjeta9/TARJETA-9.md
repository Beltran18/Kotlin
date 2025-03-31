#### ESTRUCTURA 9
# PRUEBAS, TEST Y DEPURACIÓN

1. **Describa el por qué y para qué se utiliza.**
En el desarrollo de software, es fundamental asegurarse de que el código funciona correctamente. En Kotlin, esto se logra a través de pruebas (tests) y depuración (debugging).

**Pruebas y Tests en Kotlin**
Las pruebas permiten verificar que el código se comporta como se espera. Existen varios tipos de pruebas en Kotlin:

- Pruebas Unitarias (Unit Tests)
Se enfocan en probar funciones o métodos individuales de una aplicación sin depender de otros componentes.
  En Kotlin, se usa JUnit y KotlinTest para escribir pruebas unitarias.
  Se ejecutan rápidamente y permiten detectar errores en partes específicas del código.

- Pruebas de Integración (Integration Tests)
Se utilizan para probar la interacción entre varias partes del sistema (ejemplo: una función que accede a una base de datos).

- Pruebas Funcionales
Evalúan el comportamiento del sistema según los requisitos del usuario. Se pueden automatizar con herramientas como Selenium para probar interfaces gráficas.

- Pruebas de UI (User Interface Testing)
Se realizan para verificar que la interfaz gráfica funcione correctamente. En aplicaciones Android escritas en Kotlin, se usan herramientas como Espresso y UI Automator.

**Depuración (Debugging) en Kotlin**
- Depuración con IntelliJ IDEA o Android Studio
Las herramientas de desarrollo como IntelliJ IDEA y Android Studio tienen herramientas avanzadas de depuración:
  Breakpoints: Se colocan en el código para detener la ejecución y analizar variables en un punto específico.
  Step Over, Step Into, Step Out: Permiten avanzar línea por línea en la ejecución del código.
  Inspección de variables: Permite ver el valor de las variables en tiempo de ejecución.

- Mensajes de Depuración con println() y log
En código simple, se pueden usar mensajes en consola con println() para ver el flujo del programa.
Para aplicaciones más avanzadas, se usa Logcat en Android con Log.d("TAG", "Mensaje").

2. **Genere un ejemplo internamente en el recuadro.**  
   - Utilice un editor de código para lograrlo.  

```kotlin
// Definimos la clase Rectangulo con un método para calcular el área
class Rectangulo(val ancho: Double, val alto: Double) {

    fun calcularArea(): Double {
        println("Calculando área para ancho = $ancho y alto = $alto") // Depuración
        return ancho * alto
    }
}

// Función principal que prueba manualmente el código
fun main() {
    val rectangulo = Rectangulo(5.0, 3.0)  // Creamos un rectángulo de 5x3
    val area = rectangulo.calcularArea()
    println("El área calculada es: $area")

    // PRUEBAS AUTOMATIZADAS (simuladas sin JUnit)
    println("Iniciando pruebas...")
    
    // Prueba 1: Rectángulo 5x3 (debe ser 15.0)
    assert(area == 15.0) { "Error: El área debe ser 15.0, pero fue $area" }

    // Prueba 2: Rectángulo con ancho 0 (debe ser 0.0)
    val rectangulo2 = Rectangulo(0.0, 4.0)
    val area2 = rectangulo2.calcularArea()
    assert(area2 == 0.0) { "Error: Si el ancho es 0, el área debe ser 0, pero fue $area2" }

    println("Todas las pruebas pasaron correctamente ✅")
}


```

---

### CREAR ALGORITMO PROPIO Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](https://github.com/Beltran18/Kotlin/blob/main/tarjeta6/tarjeta6.opus)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](https://github.com/Beltran18/Kotlin/blob/f48ee7ac9fb3e43d8c83de9df967d8ac72cf249a/tarjeta6/img-tarjeta6.jpg)**  

---

### Algoritmo creado y explicación de cómo funciona la estructura  

```kotlin
// Definimos la clase Calculadora con cuatro operaciones básicas
class Calculadora {

    fun sumar(a: Double, b: Double): Double {
        println("Sumando $a + $b") // Depuración
        return a + b
    }

    fun restar(a: Double, b: Double): Double {
        println("Restando $a - $b")
        return a - b
    }

    fun multiplicar(a: Double, b: Double): Double {
        println("Multiplicando $a * $b")
        return a * b
    }

    fun dividir(a: Double, b: Double): Double {
        if (b == 0.0) {
            throw IllegalArgumentException("No se puede dividir por cero") // Manejo de error
        }
        println("Dividiendo $a / $b")
        return a / b
    }
}

// Función principal con pruebas manuales y automatizadas
fun main() {
    val calculadora = Calculadora()

    // Prueba manual
    println("Resultado de la suma: ${calculadora.sumar(5.0, 3.0)}")

    // Pruebas automatizadas con assert()
    println("Ejecutando pruebas...")

    assert(calculadora.sumar(5.0, 3.0) == 8.0) { "Error: 5 + 3 debe ser 8.0" }
    assert(calculadora.restar(10.0, 4.0) == 6.0) { "Error: 10 - 4 debe ser 6.0" }
    assert(calculadora.multiplicar(2.0, 3.0) == 6.0) { "Error: 2 * 3 debe ser 6.0" }
    
    try {
        calculadora.dividir(4.0, 0.0) // Esto debería lanzar una excepción
        assert(false) { "Error: No se lanzó una excepción al dividir por cero" }
    } catch (e: IllegalArgumentException) {
        println("Excepción capturada correctamente: ${e.message}") // Manejo de error esperado
    }

    println("Todas las pruebas pasaron correctamente ✅")
}



```
