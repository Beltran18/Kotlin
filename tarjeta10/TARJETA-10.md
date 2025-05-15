#### ESTRUCTURA 10
# PROGRAMACIÓN ORIENTADA A OBJETOS

1. **Programación orientada a objetos (POO).**
La Programación Orientada a Objetos (POO) en Kotlin se usa para organizar, estructurar y reutilizar el código de forma eficiente y mantenible, especialmente en aplicaciones grandes o complejas, como las de Android. 

**Modularidad y organización del código:**
- Permite dividir el código en clases y objetos, lo cual facilita su comprensión, mantenimiento y reutilización.

**Reutilización del código:**
- A través de la herencia y la composición, puedes reutilizar estructuras existentes sin tener que escribir todo desde cero

**Abstracción:**
- Oculta los detalles internos de una clase y expone solo lo necesario, haciendo que el código sea más limpio y fácil de usar.

**Encapsulamiento:**
- Protege los datos internos de una clase, permitiendo el acceso controlado a través de funciones (getters y setters).

**Polimorfismo:**
- Permite usar una misma interfaz para diferentes tipos de datos u objetos, facilitando el diseño flexible y extensible del software.

2. **Genere un ejemplo internamente en el recuadro.**  
   - Utilice un editor de código para lograrlo.  

```kotlin
// EJEMPLO EN CÓDIGO KOTLIN

open class Animal(val nombre: String) {
    fun hacerSonido() {
        println("$nombre hace un sonido")
    }
}

class Perro(nombre: String) : Animal(nombre) {
    fun ladrar() {
        println("$nombre está ladrando")
    }
}

fun main() {
    val miPerro = Perro("Firulais")
    miPerro.hacerSonido()
    miPerro.ladrar()
}



```

---

### CREAR ALGORITMO PROPIO Y EXPLÍQUELO PASO A PASO  
- Genere el link del audio y el link de GitHub.  

🔗 **[LINK DEL AUDIO](https://github.com/Beltran18/Kotlin/blob/beb2dc12fb0ebcc7ef5fa44f7ba7ed77a11bd0b3/tarjeta1/audio-tarjeta1.ogg)**  
🔗 **[LINK CÓDIGO PROBADO POR US Y GUARDADO EN GITHUB](https://github.com/Beltran18/Kotlin/blob/4786c503181391eb065b9ea962e2a517275d4359/tarjeta1/img-tarjeta10.jpg)**  

---

### Algoritmo creado y explicación de cómo funciona la estructura  

```kotlin
// EJERCICO CREADO EN CÓDIGO KOTLIN

// Definimos una clase base llamada Vehiculo con una propiedad 'marca'
open class Vehiculo(val marca: String) {
    
    // Método que imprime información genérica del vehículo
    fun encender() {
        println("$marca está encendido") // Muestra que el vehículo se ha encendido
    }
}

// Definimos una clase Coche que hereda de Vehiculo usando ": Vehiculo()"
class Coche(marca: String, val modelo: String) : Vehiculo(marca) {
    
    // Método específico del Coche que imprime el modelo
    fun mostrarModelo() {
        println("El modelo del coche es $modelo") // Muestra el modelo del coche
    }
}

// Función principal, punto de entrada del programa
fun main() {
    
    // Creamos una instancia (objeto) de la clase Coche
    val miCoche = Coche("Toyota", "Corolla")
    
    // Llamamos al método encender heredado de la clase Vehiculo
    miCoche.encender() // Resultado: Toyota está encendido
    
    // Llamamos al método mostrarModelo definido en la clase Coche
    miCoche.mostrarModelo() // Resultado: El modelo del coche es Corolla
}



```

