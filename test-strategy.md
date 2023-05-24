# test-mrwebsite-Geovani
solución del problema
soluciones para los errores encontrados en el archivo 

1. En la línea 2 del archivo js en la parte de "let randomNumber = Math.random() * 10; " está generando un numero aleatorio entre 0 y 10, pero el programa requiere que se genere un numero entre 1 y 100.
Para solucionar este error se cambió  "let randomNumber = Mathc.random() * 10; " por "let randomNumber = Math.random() * 100; " pero si se deja solo así, genera un numero entre 0 y 100 por lo que hay que sustituir el contenido de la línea 2 por lo siguiente "let randomNumber = Math.floor(Math.random() * 100) + 1;" la función "Math.floor" sirve para redondear un numero hacia abajo al entero más cercano, se le suma 1 para que sea entero tal como los parámetros del juego indican.
2. En la línea 6 del archivo js "const lowOrHi = document.querySelector('lowOrHi'); " falta el punto en el selector de clase, tiene que quedar así  "const lowOrHi = document.querySelector('.lowOrHi'); " y que hace ese error? Pues lo que se quiere en principio en seleccionar un elemento del documento HTML que tiene la clase   " lowOrHi" pero debido al punto selector faltante no se logra coincidir con el elemento  y provoca que no se pueda asignar valores o realizar operaciones con dicho elemento
3. En la línea 45 del archivo js" guessSubmit.addeventListener('click', checkGuess); " esta escrita incorrectamente, evento debe de escribirse con la e mayúscula, de esta manera debe de corregirse: " guessSubmit.addEventListener('click', checkGuess); "
4. Lo mismo sucede en la línea 52 del archivo js "resetButton.addeventListener('click', resetGame); " se volvió a cometer el error de Event con la letra minúscula, corrección : "resetButton.addEventListener('click', resetGame); "
5. en la línea 72 del código del archivo js "randomNumber = Math.floor(Math.random()) + 1; " se esta generando mal el numero aleatorio ya que falta el 100 dentro de los paréntesis para que funcione
Errores generales 
El código del archivo js y css esta dentro del HTML lo cual esto provoco que no funcionara el proyecto cuando se subió a los servidores de producción, se debía de crear un archivo llamada script.js con el código js y otro llamado styles.css para el correcto funcionamiento del programa
