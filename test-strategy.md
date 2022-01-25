# Estrategia de testing  de software
**El objetivo general** de esta estrategia es verificar la funcionalidad del proyecto ***Testing de prueba 1*** describiendo las diferentes pruebas que se realizarán. El proyecto se compone de los archivos:

 1. index.html
 2. Readme.md
## Estrategia de testing de software

 1. Tiempo Límite: 8 horas
 2. Realizar pruebas 10 unitarias de caja negra
 3. Realizar las pruebas de caja blanca sobre el flujo normal del proyecto
 4. Solucionar los errores encontrados o proponer soluciones viables
 5. Se tiene a una persona experta en QA y Testing de software

## Errores de caja Negra
**Validación de valores vacios**

**Descripción**

> Ingresar espacios en textbox adivinar numero

**Funcionamiento esperado**

> No tomar ninguna acción

**Validación ingreso espacios seguido de numero**

**Descripción**

> Ingresar espacios y luego número en textbox adivinar numero

**Funcionamiento esperado**

> Tomar número ingresado después de los espacios

**Resultado**

> Tomar valor ingresado

~~**Validación ingreso texto - Error**~~

**Descripción**

> Ingresar letras en textbox adivinar numero

**Funcionamiento esperado**

> Validar que no es un numero y mostrar un error

**Resultado**

> Error

~~**Validación ingreso texto seguido de numero**~~

**Descripción**

> Ingresar letras seguido de numero en textbox adivinar numero

**Funcionamiento esperado**

> Validar que no es un número y mostrar un error

**Resultado**

Error

~~**Validación ingreso de numero decimal**~~

**Descripción**

> Ingresar numero decimal en textbox adivinar numero

**Funcionamiento esperado**

> Validar que no es un número entero y mostrar un error

**Resultado**

Error

**Validación ingreso vacío**

**Descripción**

> No ingresar nada

**Funcionamiento esperado**

> Mostar error de ingresar un numero

**Resultado**

> Toma resultado un valor 0

~~**Validación ingreso símbolos**~~

**Descripción**

> Ingresar símbolo en textbox adivinar numero

**Funcionamiento esperado**

> Validar que no es un número entero y mostrar un error

**Resultado**

Error

**Validación ingreso número mayor**

**Descripción**

> Ingresar numero mayor al rango de 1-100

**Funcionamiento esperado**
> Validar que no es un número entre el rango y mostrar un error

**Resultado**

> Ingresa numero fuera de rango

**Validación ingreso número negativo**

**Descripción**

> Ingresar número negativo

**Funcionamiento esperado**
> Validar que no es un número entre el rango y mostrar un error

**Resultado**

> Ingresa número fuera de rango

**Validación ingreso número 4.444444444444445e+28**

**Descripción**

> Ingreso número decimal seguido de una letra y sumando un segundo

**Funcionamiento esperado**
> Validar que no es un número entre el rango y mostrar un error

**Resultado**

> Ingresa número fuera de rango

##   Errores de caja Blanca
####  Descripción
Verificar los mensajes dentro de un flujo normal del proyecto en caso de que la partida se pierda.
#### Solución

    else if (guessCount === 10) {
    lastResult.textContent = '!!!Pérdistes!!!';
    lowOrHi.textContent = '';
    setGameOver();
    
### 1.  Error en mensaje en caso de ganar la partida
#### Descripciòn

Mostrar mensaje correcto al ganar.

#### Solución
Cambiar lo que imprime y cambiar el color.

    if (userGuess === randomNumber) {
    lastResult.textContent = 'Felicitaciones! adivinaste el número!';
    lastResult.style.backgroundColor = 'green';
    lowOrHi.textContent = '';

### 2. Error en validación de número entero

#### Descripciòn

Validar numero entero

#### Soluciòn

Validar numero entero o decimal.

    if ( Number.isInteger(userGuess))


### 3. Validación de número de intentos de la partida

#### Descripciòn

Numero de intetos 5, el correcto es 10

#### Soluciòn

eliminar la constante y en la condicion eliminar la constante y colocar el numero de intentos la cual es 10

    else if (guessCount === 10)


### 4. Validación de números aleatorios dentro del rango especificado

Descripción

Numero random se encuentra en 10 y tiene que ser en 100

Se debe de cambiar para 100 numeros.

    let randomNumber = Math.floor(Math.random() * 100) + 1;





          

