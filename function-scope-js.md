## Identificacion de funciones

#### Objetivo

Identificar las funciones globales, locales, funciones de callback, expresions, statement, closure, scope, contextos de ejecucion, funciones que forman parte de la pila de ejecucion (stack execution) y funciones que forman parte de la cola de eventos (event queue) en el ejercicio mostrado.


**Funciones globales**
Funciones que no estan dentro de otra funcion

```Javascript
$(document).ready(function() {});
```
**Funciones locales**
Funciones que se esncuetran dentro de otras funciones

- function activeButton()
- function desactiveButton()
- function longitud(input)
- function soloNumeros(input)
- function isValidCreditCard(numberCard)

**Funciones de callback**
Funciones que son pasadas como argumento

- funcion anonima relacionada al evento input (linea 14)
- funcion longitud usada como argumento para la funcion soloNumeros

**Function expresion**
Funcion asignada a una variable, puede ser invocada posterior a su declaracion (recomendable)

```Javascript
var creditCardNumber = soloNumeros(longitud(numberCard));
```

**Function statements**
Funncion creada de forma directa, puede ser invocada desde cualquier parte del código (no recomendable)

- function activeButton()
- function desactiveButton()
- function longitud(input)
- function soloNumeros(input)
- function isValidCreditCard(numberCard)

**Closure**
Es la capacidad de las funciones para recordar el entorno en el que fueron creadas

- function activeButton()
- function desactiveButton()

Estas 2 funciones recuerdan a la variable $buttonNext que fue declarada en su entorno de creacion.

**Execution Stack**
Funciones que se posicionan en la pila de ejecucion

- $(document).ready(function()
- console.log('Probar con el numero valido 4544164785372342');  

**Event Queue**
Son aquellas funciones que forman parte de la cola de eventos

 - funcion anonima relacionada al evento input
 - function isValidCreditCard()
 - soloNumeros() --> (isValidCreditCard())
 - longitud()--> (isValidCreditCard())
 - activeButton() --> (isValidCreditCard())
 - desactiveButton() --> (isValidCreditCard())
