# Ejercicios-JS-abril-16

1. Mostrar por consola la tabla de multiplicar del 5 utilizando la sentencia for de la siguiente manera:
```javascript
console.log("Tabla de multiplicar del 5:");
for (var i = 0; i <= 10; i++) {
    var resultado = 5 * i;
    console.log("5 x " + i + " = " + resultado);
}
```

2. Modificar el programa anterior y mostrar las 10 tablas de multiplicar.

```javascript
console.log("Tabla de multiplicar del 5:");
for (var i = 0; i <= 10; i++) {
    var resultado = 10 * i;
    console.log("10 x " + i + " = " + resultado);
}
```

3. Pedir por pantalla a través de prompt un texto y mostrar en un alert si el texto introducido es un valor numérico o es una cadena.






4. Pedir dos textos por pantalla a través de prompt y mostrar en un alert las dos cadena concatenadas.
```Javascript
// Pedir al usuario que introduzca dos textos mediante prompt
var texto1 = prompt("Introduce el primer texto:");
var texto2 = prompt("Introduce el segundo texto:");

// Concatenar los dos textos
var textoConcatenado = texto1 + " " + texto2;

// Mostrar un alert con el resultado de la concatenación
alert("Los dos textos concatenados son: " + textoConcatenado);
```

5. Pedir dos números por pantalla con prompt y mostrar la suma de ambos.  Se debe validar que los números introducidos sean números.
```javascript
<
       
function esNumero(valor) {
    return !isNaN(valor) && isFinite(valor);
}


var numero1 = prompt("Introduce el primer número:");
var numero2 = prompt("Introduce el segundo número:");


if (esNumero(numero1) && esNumero(numero2)) {

    numero1 = parseFloat(numero1);
    numero2 = parseFloat(numero2);

    var suma = numero1 + numero2;

   
    alert("La suma de los dos números es: " + suma);
} else {
    
    alert("Por favor, introduce dos números válidos.");
}
```

6. Pedir dos números por pantalla y una operación (+, -, *, /) y mostrar en un alert el resultado de la operación.  Si la operación no es ninguna de las anteriores, se debe mostrar el mensaje "Operación incorrecta".  Se debe validar que los valores introducidos sean números.
```Javascript
function esNumero(valor) {
    return !isNaN(valor) && isFinite(valor);
}


var numero1 = prompt("Introduce el primer número:");
var numero2 = prompt("Introduce el segundo número:");
var operacion = prompt("Introduce la operación a realizar (+, -, *, /):");


if (esNumero(numero1) && esNumero(numero2)) {
   
    numero1 = parseFloat(numero1);
    numero2 = parseFloat(numero2);

    
    switch (operacion) {
        case "+":
            alert("El resultado de la suma es: " + (numero1 + numero2));
            break;
        case "-":
            alert("El resultado de la resta es: " + (numero1 - numero2));
            break;
        case "*":
            alert("El resultado de la multiplicación es: " + (numero1 * numero2));
            break;
        case "/":
            alert("El resultado de la división es: " + (numero1 / numero2));
            break;
        default:
            alert("Operación incorrecta");
            break;
    }
} else {
    
    alert("Por favor, introduce dos números válidos.");
}
```

7. Leer tres notas de los estudiantes y calcular la media.  Tiene que indicar si está reprobado (nota < 3) o aprobado, junto con la nota media.  Si alguna nota no es un número, no dejar de pedirlas hasta que sea correcta.
```Javascript
// Función para validar si un valor es un número
function esNumero(valor) {
    return !isNaN(valor) && isFinite(valor);
}

// Función para calcular la media de las notas
function calcularMedia(notas) {
    var suma = 0;
    for (var i = 0; i < notas.length; i++) {
        suma += notas[i];
    }
    return suma / notas.length;
}

// Función para determinar si un estudiante está aprobado o reprobado
function verificarAprobacion(media) {
    if (media >= 3) {
        return "Aprobado";
    } else {
        return "Reprobado";
    }
}

// Array para almacenar las notas
var notas = [];

// Solicitar al usuario que introduzca tres notas y validarlas
for (var i = 0; i < 3; i++) {
    var nota;
    do {
        nota = prompt("Introduce la nota " + (i + 1) + ":");
    } while (!esNumero(nota));
    notas.push(parseFloat(nota));
}

// Calcular la media de las notas
var media = calcularMedia(notas);

// Determinar si el estudiante está aprobado o reprobado
var estado = verificarAprobacion(media);

// Mostrar el resultado
alert("La nota media es: " + media.toFixed(2) + ". El estudiante está " + estado + ".");


```

8. Introducir dos números e indicar cuál es el mayor o si son iguales.
```Javascript
var numero1 = prompt("Introduce el primer número:");
var numero2 = prompt("Introduce el segundo número:");

numero1 = parseFloat(numero1);
numero2 = parseFloat(numero2);

if (numero1 === numero2) {
    alert("Los dos números son iguales.");
} else if (numero1 > numero2) {
    alert("El primer número es mayor que el segundo.");
} else {
    alert("El segundo número es mayor que el primero.");
}
```
9. Pintar un cuadrado de asteriscos de 5 por cada lado.
```Javascript
var tamaño = 5;


for (var i = 0; i < tamaño; i++) {
    var linea = "";
    for (var j = 0; j < tamaño; j++) {
        if (i === 0 || i === tamaño - 1 || j === 0 || j === tamaño - 1) {
            linea += "*";
        } else {
            linea += " ";
        }
    }
    console.log(linea);
}
```

10. Cree esta figura por pantalla con JS
```Javascript
// Definir la altura de la figura
var altura = 5;
// Dibujar la parte superior de la figura
for (var i = 1; i <= altura; i++) {
    var linea = "";
    // Imprimir espacios en blanco
    for (var j = 1; j <= altura - i; j++) {
        linea += " ";
    }
    // Imprimir asteriscos
    for (var k = 1; k <= 2 * i - 1; k++) {
        linea += "*";
    }
    console.log(linea);
}
// Dibujar la parte inferior de la figura
for (var i = altura - 1; i >= 1; i--) {
    var linea = "";
    // Imprimir espacios en blanco
    for (var j = 1; j <= altura - i; j++) {
        linea += " ";
    }
    // Imprimir asteriscos
    for (var k = 1; k <= 2 * i - 1; k++) {
        linea += "*";
    }
    console.log(linea);
}
```