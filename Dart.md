# **Dart**

###  Conceptos Básicos:
- Dart es un programa desarrollado por Google.
- Fue lanzado en 2013.
- Es orientado a objetos.
- Dart es un lenguaje no nolabo, está protegido para cuando es null no te deje compilar.
- Todo lo que se puede colocar en una variable es un objeto.
- Dart es un lenguaje tipado.
- Un error en tiempo de compilación impide que el Código se ejecute en absoluto.
- Un error en tiempo de ejecución provoca que se haga una excepción mientras el Código se ejecuta.
- Las clases van con la primera letra en mayúscula.
- **Propiedades**: Almacenan información y pueden tener métodos de acceso asociados para obtener y establecer su valor, definen la programación orientada a objetos.
- **Métodos**: Suelen realizar una acción o cálculo y devolver un valor.


### Tipos de Datos:

- El tipo de dato "**int**" solamente puede recibir número enteros.
```dart
void main(List<String> args) {
  int numero = 1;
}
```

- El tipo de dato "**double**" recibe números con decimales.
- ***double numero = 1***; El tipo de dato "**double**" no debe ser representado así, debido a que puede causar problemas, lo mejor es cambiarlo a "**int**".
```dart
void main(List<String> args) {
  double numero = 1.0;
}
```
- ***double numero = 1.0***; Así, si está bien representado.
- El tipo de dato "**String**" son cadenas de caracteres que se pueden poner palabras, espacios en blanco, caracteres, etc.
```dart
void main(List<String> args) {
  String nombre = "Jahir";
}
```
- El tipo de dato "**bol**" define si es verdadero o falso.
```dart
void main(List<String> args) {
bool activado = true;
bool desactivado = false;
}
```
- "**var**" Se utiliza en situaciones donde el tipo es obvio o cuando su uso no afecta la comprensión del código (se utiliza para fijar el tipo de dato de la variable en tiempo de compilación).

```dart
void main(List<String> args) {
  var nombre = "Jahir";
  var numero = 1;
  var numero2 = 1.0;
  var activado = true;
  var desactivado = false;
}
```
- Esta es una forma correcta de utilizar el tipo de dato "var".
```dart
void main(List<String> args) {
var numero = 1;
numero = 2;
print(numero);
}

//salida: 2
```
- Esta es una forma incorrecta de utilizar el tipo de dato "var".
```dart
void main(List<String> args) {
var numero = 1;
numero = "dos";
print(numero);
}

//salida: A value of type 'String' can't be assigned to a variable of type 'int'.
```


- "**dynamic**" es cuando no sabemos qué tipo de dato es (permite que el tipo de variable sea flexible en tiempo de ejecución).
```dart
void main(List<String> args) {
  dynamic nombre = "Jahir";
  dynamic edad = 23;
  dynamic peso = 75.5;
  dynamic casado = false;
}
```
- Esta es la demostración de usar el tipo de dato dynamic.

```dart
void main(List<String> args) {
dynamic numero = 1;
numero = "uno";
}

//salida: uno
```

### Simbología:

- "***?***": significa que esta variable puede ser nula (no se puede multiplicar por algo nulo, a menos que especifiquemos el valor que tiene).



- "***!***": es como que a huevo corra, no importa si es null.



- "***$***": se utiliza para inyectar o insertar variables.



- "***{}***": sirven para obtener el producto de las variables.



- " ": significa propiedad vacia.



- " ***\\*** ": Sirve para poder poner cantidades de dinero o símbolos reservados.



- "***\n***": Se utiliza para imprimir el siguiente mensaje en la siguiente línea.



- "***\t***": Se utiliza para alinear los valores en columnas.



- ***"""(Texto)"""***: Las comillas triples se utilizan para pasar de línea en la terminal.



- "***&&***": Se utiliza como un operador lógico para realizar una operación de "Y" lógico entre dos expresiones booleanas.



### Conceptos Avanzados:

- El ***tipado estático implícito*** Reduce de la cantidad de código que debes escribir y la prevención de errores relacionados con el tipo de datos. Sin embargo, también puede tener algunas desventajas, como la posible pérdida de claridad y documentación explícita del código.

- El ***Implícito o no estático*** es una variable que no tiene un tipo de datos explícito y cuyo tipo se infiere automáticamente por el compilador en tiempo de ejecución.

- "***Código espagueti***" Se refiere a un tipo de código fuente que es muy difícil de entender.

-  "**const**" Es un valor que no puede cambiar durante la ejecución del programa.

- "***args***” Es un parámetro especial que se utiliza en la función *main ()* para recibir argumentos de línea de comandos como una lista de cadenas de caracteres.

```dart
// Escribir un programa que imprima su nombre completo escrito desde la terminal.

void main(List<String> args) {
  print("Hola ${args[0]} ${args[1]} ${args[2]} ¿Cómo estas?"); // Escribir lo que quieras poner en la terminal.
}
```

- "***Casting***" Es el proceso de convertir un valor de un tipo de dato a otro tipo de dato.

```dart
void main(List<String> args){
double numeroDouble = 3.14;
int numeroEntero = numeroDouble.toInt();
print(numeroEntero); 
}

//salida: 3.
```

- "***Estructuras Repetitivas***" Las estructuras repetitivas son aquellas que permiten ejecutar una o varias instrucciones varias veces en función de una condición.

- "***For***" Se utiliza para iterar sobre una secuencia de números enteros en orden ascendente o descendente.

```dart
for (int i = inicio; i <= fin; i++) {
  // Instrucciones a repetir.
}
```
- *Ejemplo*:

```dart
// Hacer un ciclo for que imprima los numeros del 1 al 10 y explique su funcionamiento.

void main(List<String> args){ 
  for (int i = 1; i <= 10; i++) { //Se utiliza para iterar sobre una secuencia de números enteros en orden ascendente o descendente.
    print(i); //Imprime los numeros del 1 al 10.
  }
}

///salida: 1,2,3,4,5,6,7,8,9,10.
```


- "***For Each***" Se utiliza para iterar sobre una colección de elementos, como un array o una lista.

```dart
for (var elemento in coleccion) {
  // Instrucciones a repetir
}
```
- *Ejemplo*:

```dart
// Hacer un ciclo for each que imprima los números del 1 al 10

void main(List<String> args){
  var lista = [1,2,3,4,5,6,7,8,9,10]; //lista de numeros
  for (var i in lista) { //ciclo for each que funciona con listas y arrays que recorre la lista y la imprime 
    print(i); //imprime la lista 
  }
}

//salida: 1,2,3,4,5,6,7,8,9,10.
```

- "***For In***" Se utiliza para iterar sobre los elementos de un objeto iterable, como un "map" o un "set".

```dart
for (var entrada in objetoIterable) {
  // Instrucciones a repetir
}
```
- *Ejemplo*: 

```dart
// Hacer un ciclo for in que recorra una lista de 10 elementos e imprima cada uno de ellos.

void main(List<String> args){ //
  var lista = [1,2,3,4,5,6,7,8,9,10]; //creamos una lista de 10 elementos y la guardamos en la variable lista. 
  for (var entrada in lista) { //creamos un ciclo for in, donde la variable entrada va a tomar el valor de cada elemento de la lista hasta que se termine de recorrer la lista.
    print(entrada); //imprimimos el valor de la variable entrada.
  }
}

///salida: 1,2,3,4,5,6,7,8,9,10.
```

- "***While***" Se utiliza para repetir un conjunto de instrucciones mientras se cumpla una condición específica.

```dart
while (condición) {
  // conjunto de instrucciones a repetir
}
```
- *Ejemplo*:

```dart
// Hacer un ciclo while que imprima los números del 1 al 10.

void main(List<String> args){ 
  int i = 1; //inicializamos la variable i en 1.
  while (i <= 10) { //mientras i sea menor o igual a 10 se ejecutara el ciclo.
    print(i); //imprimimos el valor de i en cada iteracion del ciclo.
    i++; // Cada vez que se ejecute el ciclo while se le sumara 1 a la variable i hasta que i sea mayor a 10.
  }
}

///salida: 1,2,3,4,5,6,7,8,9,10.
```

- "***Do While***" Se utiliza para repetir un conjunto de instrucciones al menos una vez, y luego repetir el conjunto de instrucciones mientras se cumpla una condición específica.

```dart
do {
  // conjunto de instrucciones a repetir
} while (condición);
```

- *Ejemplo*: 

```dart
// Haz un ciclo Do while que imprima los números del 1 al 10.

void main(List<String> args){ 
  int i = 1; // Inicializamos la variable i en 1.
  do { // Hacemos un ciclo do while que imprima los números del 1 al 10.
    print(i); // Imprimimos el valor de i hasta que i sea igual a 10.
    i++; // Incrementamos el valor de i en 1.
  } while (i <= 10); // Mientras i sea menor o igual a 10 se repetirá el ciclo.
}

// salida: 1,2,3,4,5,6,7,8,9,10.
```

- *"**switch case**"* se utiliza para ejecutar un bloque de código diferente dependiendo del valor de una expresión determinada (como una variable o una constante) y de los valores de las diferentes cláusulas case.

```dart
switch (expresion) {
  case valor1:
    - // bloque de código si la expresión es igual a valor1
    break;
  case valor2:
    - // bloque de código si la expresión es igual a valor2
    break;
  - // ...
  default:
   -  // bloque de código si la expresión no coincide con ningún valor
}
```


- *Ejmeplo*: 

```dart
// Hacer un ciclo case que imprima un número del 1 al 5.

void main(List<String> args){ 
  int numero = 1; // asignamos el valor 1 a la variable numero.
  switch (numero) { // evaluamos la variable numero.
    case 1: // si el valor de la variable numero es 1 entonces:
      print("1"); // imprimimos el valor de la variable numero que es 1 en este caso.
      break; // salimos del switch case para evitar que se ejecuten los demas casos del switch case si es que los hay y el programa termine.
    case 2: // asi sucesivamente evaluamos el valor de la variable numero para cada caso.
      print("2"); 
      break;
    case 3:
      print("3");
      break;
    case 4:
      print("4");
      break;
    case 5:
      print("5");
      break;
    default: // si el valor de la variable numero no es ninguno de los anteriores entonces:
      print("No es un numero del 1 al 5"); // imprimimos que el valor de la variable numero no es un numero del 1 al 5.
  }
}

// salida: 1.
```

- "***Listas***" las listas son indexadas, puede acceder a los elementos del array.

```dart
void main(List<String> args){
  List<int> nums = [1,2,3,4,5,6,7,8,9]; // Lista de numeros enteros y se le asigna un valor.
  // Imperativa
  for (var i = 0; i < nums.length; i++) { // "i" funciona como un contador y nums.length es el tamaño de la lista.
    print(nums[i]); // Imprime la lista de numeros.
  }
  // Declarativo
  for (var num in nums) { // "num" es una variable que va a recorrer la lista de numeros y nums es la lista de numeros que se va a recorrer con la variable "num".
    print(num + num); // Imprime la lista de numeros y los suma.
  }
  // Coleccion 
  nums.forEach((num) { // "num" es una variable que va a recorrer la lista de numeros y nums es la lista de numeros que se va a recorrer con la variable "num" y el forEach es un metodo que recorre la lista de numeros.
    print(num * num * num); // Imprime la lista de numeros y los multiplica.
  });
}
```
### Métodos

- *Los metodos empiezan con un punto ("**.**"*).

- "***.isNotEmpty***": Se puede realizar una comprobación rápida de si una cadena de texto o una lista tiene algún elemento antes de intentar realizar alguna operación con ella.



- "***.endsWith***": Es un método que se utiliza para verificar si una cadena de texto termina con un determinado sufijo o cadena de caracteres.



- "***.runtimeType***": Es un método que se utiliza para obtener el tipo en tiempo de ejecución (runtime) de un objeto.



- "***.toString***": Se utiliza para convertir un objeto en una cadena de texto.



- "***.toInt***": Se utiliza en un número decimal o de punto flotante, se devuelve una versión entera de ese número, truncando cualquier parte decimal.



- "***.contains***":  Se utiliza para verificar si una colección (como una lista, un conjunto o un mapa) contiene un elemento determinado.



- "***.leght***":  Se utiliza para obtener la cantidad de elementos que hay en una colección (como una lista, un conjunto o una cadena de caracteres).



- "***.add***": Se utiliza en Dart para agregar un elemento al final de una lista.



- "***.toSet***": Cuando se desea obtener una colección de elementos únicos a partir de una colección con elementos repetidos, o para eliminar elementos duplicados de una colección.



- "***.firstWhere***": Es una herramienta útil para buscar elementos específicos en una lista o iterador.



- ***.removeWhere***: Es una herramienta útil para eliminar elementos específicos de una lista o iterador que cumplan con una determinada condición.



- "***int.parse***": Toma una cadena como argumento y devuelve un número entero si la cadena se puede convertir correctamente, o lanza una excepción si la cadena no es válida.



- "***double.parse***": Toma una cadena como argumento y devuelve un número de punto flotante si la cadena se puede convertir correctamente, o lanza una excepción si no es válida.



- "***args.lenght***": Se utiliza para obtener el número de argumentos que se pasan a un programa en línea de comandos.



- "***stdout.write***": Se utiliza para escribir una cadena de texto en la salida estándar del programa, que por lo general es la consola en la que se está ejecutando.



- "***stdin.readByteSync***": Se usa para leer datos desde la entrada, aunque bloquea la ejecución del programa hasta que se ingresa un byte en la entrada estándar.



- "***stdin.readLineSync***": Una línea de entrada de texto desde la consola (Hasta que se haya ingresado una línea de texto y se haya presionado la tecla "Enter").




