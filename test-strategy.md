Error 1
Descripciòn
Mostrar mensaje correcto.
Soluciòn
else if (guessCount === 10) {
          lastResult.textContent = '!!!Pérdistes!!!';
          lowOrHi.textContent = '';
          setGameOver();
          

Error 2
Descripciòn
Mostrar mensaje correcto al ganar.
Soluciòn
Cambiar lo que imprime y cambiar el color.
if (userGuess === randomNumber) {
          lastResult.textContent = 'Felicitaciones! adivinaste el número!';
          lastResult.style.backgroundColor = 'green';
          lowOrHi.textContent = '';
Error 3
Descripciòn
Validar numero entero 
Soluciòn
Validar numero entero o decimal.
if ( Number.isInteger(userGuess))

Error 4
Descripciòn
Numero de intetos 5, el correcto es 10
Soluciòn
eliminar la constante y en la condicion eliminar la constante y colocar el numero de intentos la cual es 10
else if (guessCount === 10)


Error 5
Descripciòn
Numero random se encuentra en 10 y tiene que ser en 100
Se debe de cambiar para 100 numeros.
let randomNumber = Math.floor(Math.random() * 100) + 1;





          

