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

6. Pedir dos números por pantalla y una operación (+, -, *, /) y mostrar en un alert el resultado de la operación.  Si la operación no es ninguna de las anteriores, se debe mostrar el mensaje "Operación incorrecta".  Se debe validar que los valores introducidos sean números.

7. Leer tres notas de los estudiantes y calcular la media.  Tiene que indicar si está reprobado (nota < 3) o aprobado, junto con la nota media.  Si alguna nota no es un número, no dejar de pedirlas hasta que sea correcta.


8. Introducir dos números e indicar cuál es el mayor o si son iguales.


9. Pintar un cuadrado de asteriscos de 5 por cada lado.


10. Cree esta figura por pantalla con JS
