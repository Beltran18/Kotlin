#### ESTRUCTURA 8 
# PROGRAMACION FUNCIONAL Y EXPRESIONES LAMBDA

1. **Describa el por qué y para qué se utiliza.**
La programación funcional en Kotlin permite tratar funciones como ciudadanos de primera clase, lo que significa que se pueden almacenar en variables, pasarlas como argumentos o devolverlas desde otras funciones. Kotlin proporciona soporte completo para funciones de orden superior y expresiones lambda, lo cual permite escribir código más conciso, reutilizable y fácil de mantener.

**Funciones de Orden Superior:** Son funciones que reciben funciones como parámetros o retornan funciones.

**Expresiones Lambda:** Una lambda es una función anónima que se puede definir de manera concisa y se utiliza especialmente en funciones que reciben otras funciones como parámetros. Permiten escribir código más expresivo y limpio.

**Ventajas:**
- Facilita la programación orientada a funciones.
- Reduce el código boilerplate.
- Mejora la legibilidad y reutilización del código.

**Tipos de Variables:**
- val (constante): No se puede modificar después de asignarle un valor.
- var (variable): Puede cambiar su valor en cualquier momento.

**Tipos de Datos en Kotlin:**
- Funciones Lambda: Funciones anónimas que se definen sin un nombre explícito.
- Funciones de Orden Superior: Funciones que reciben o retornan otras funciones.
- Colecciones (List, Set, Map): Se pueden manipular mediante lambdas y funciones estándar como `filter`, `map`, `reduce`, etc.



2. **Genere un ejemplo internamente en el recuadro.**  
   - Utilice un editor de código para lograrlo.  

```kotlin
// EJEMPLO EN CÓDIGO KOTLIN

fun main() {
    // Ejemplo de expresión lambda para sumar dos números
    val suma: (Int, Int) -> Int = { a, b -> a + b }
    val resultado = suma(5, 3)
    println("El resultado de la suma es: $resultado")

    // Uso de función de orden superior con lambda
    val lista = listOf(1, 2, 3, 4, 5)
    val listaFiltrada = lista.filter { it > 2 }
    println("Números mayores que 2: $listaFiltrada")

    // Mapeo de elementos con lambda
    val listaMapeada = lista.map { it * 2 }
    println("Elementos multiplicados por 2: $listaMapeada")

    // Uso de lambdas con funciones de orden superior personalizadas
    fun operar(a: Int, b: Int, operacion: (Int, Int) -> Int): Int {
        return operacion(a, b)
    }

    val multiplicacion = operar(4, 5) { x, y -> x * y }
    println("El resultado de la multiplicación es: $multiplicacion")
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
    // Declaración de un mapa de productos con su precio.
    val productos = mapOf("Manzana" to 1.0, "Banana" to 0.5, "Naranja" to 0.8)

    // Uso de la función 'forEach' para iterar sobre cada elemento del mapa.
    productos.forEach { (producto, precio) ->
        println("Producto: $producto - Precio: $precio")
    }

    // Declaración de una lista de precios.
    val precios = listOf(10.0, 20.0, 30.0, 40.0)

    // Uso de 'map' con una lambda para aplicar un descuento del 10% a cada precio.
    val preciosConDescuento = precios.map { it * 0.9 }

    // Imprime la lista de precios con descuento.
    println("Precios con descuento: $preciosConDescuento")

    // Uso de 'filter' para obtener solo los precios mayores a 25.
    val preciosFiltrados = precios.filter { it > 25 }

    // Imprime los precios filtrados.
    println("Precios mayores a 25: $preciosFiltrados")

    // Declaración de una función de orden superior que recibe una lista y una operación sobre ella.
    fun <T> aplicarOperacion(lista: List<T>, operacion: (T) -> Unit) {
        lista.forEach { operacion(it) }
    }

    // Uso de la función de orden superior para imprimir cada precio con formato especial.
    aplicarOperacion(precios) { println("Precio: $$it") }

    // Declaración de una lambda que calcula el precio total sumando todos los elementos de la lista.
    val calcularTotal: (List<Double>) -> Double = { it.sum() }

    // Uso de la lambda para calcular el total de precios.
    val total = calcularTotal(precios)

    // Imprime el total calculado.
    println("El precio total es: $$total")
}

```

