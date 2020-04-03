# JaqueTest
Propuesta de solución para los ejercicios solicitados, elaborada por Fernando Arreola.

Para la solución del examen, fueron utilizadas las siguientes herramientas:

* JavaScript y HTML como lenguajes de programación
* Consola de JavaScript del navegador Safari para depuración de código
* Navegador safari para pruebas de código
* Atom como editor de texto
* GitHub como repositorio de archivos

A continuación se menciona una breve descripción de mi análisis para resolver los ejercicios:

__Ejercicio uno__

Para resolver este ejercicio, hice uso de dos arreglos y de dos variables contadoras para tener el control de aquellos elementos que son mayores que el anterior. El arreglo a analizar se ingresa direcamente en el código.

Con apoyo de un ciclo for, se recorre el arreglo, y por medio de un if, validamos si el elemento actual del arreglo, es mayor que el elemento anterior:

* Si es mayor, sacamos el último elemento de un arreglo temporal (Para evitar elementos duplicados)
* Ingresamos el elemento anterior del arreglo que estamos analizando al arreglo temporal
* Ingresamos el elemento actual del arreglo que estamos analizando al arreglo temporal

Si el elemento actual, no es mayor que el elemento anterior ajustamos los valores de los contadores, almacenamos los elementos que cumplen la condición hasta este momento en un arreglo donde almacenaremos el resultado y limpiamos el arreglo temporal. Finalmente, al salir del ciclo for, se vuelven a validar los valores de los contadores, ya que puede darse el caso de que los últimos elementos del arreglo cumplen la condición de interés, y se muestra tanto el arreglo origina como el máximo subarreglo.

La complejidad del algoritmo es O(n), ya que se hace uso de un ciclo for y dentro de el, se encuentran operaciones de tiempo constante.

__Ejercicio dos__

El ejercicio recibe dos números por medio de un textbox, para componer la serie. Primero ser verifica que se ingresen dos valores y que ambos sean positivos. Si es así, se convierten los números a enteros y se verifica que m sea mayor que n. Posteriormente se verifica si son iguales y en caso de que no, se comienza a calcular la serie por medio de un ciclo while que itera hasta que la suma de m + i sea menor que el valor de m, donde i es un iterador para componer la forma de la serie que es calculada por medio de una variable acumuladora . Una vez que se rompe el ciclo, se agregan los terminos m y n a la serie y se muestra el resultado.

La complejidad del algoritmo es O(n), ya que no hay algún otro bucle anidado y las operaciones contenidas son de tiempo constante.

__Ejercicio tres__

El ejercicio recibe un arreglo que introduce el usuario, aunque con un tamaño máximo predeterminado. El valor de k-ésimo elemento a buscar, tabién es introducido por el usuario. Primero se valida que la k introducida esté entre el valor del tamaño del arreglo. Si es así, continua la ejecución, por medio de la función sort ordenamos ascendentemente el arreglo y finalmente, restamos a la longitud del arreglo el valor de k, y como el arreglo está ordenado, obtendremos como resultado el valor del k-ésimo elemento más grande. Se imprime el arreglo original y el valor del elemento en la posición k.

La complejidad de la solución propuesta puede caer en un caso de O(n<sup>2</sup>), debido a la parte del algoritmo que implmente el método sort.

__Ejercicio cuatro__

El ejercicio recibe un arreglo que introduce el usuario, aunque con un tamaño máximo predeterminado. El ejercicio consite en eliminar elementos repetidos, para ello aplicamos el metodo forEach al arreglo para iterar y aplicar una función a cada uno de sus elementos, verificando si el elemento actual ya está o no está alamacenado en un arreglo temporal; si no está, se agrega, si ya está, se omite, quedándonos así sólo con los valores no repetidos. Finalmente guardamos los índices en una nueva variable, que contendrá los elementos no duplicados y los mostramos.

Se tienen dos ciclos iterativos, con complejidad O(n), pero al no estar anidados, podemos concluir que la complejidad de la solución será O(n).

__Ejercicio cinco__

El ejercicio tiene un arreglo de símbolos que están definidos dentro de la función. Se define una variable "pila", que funcionara como una pila de datos para meter, sacar información y llegar a una conclusión. Por medio de un ciclo for, iteramos a lo largo del arreglo de símbolos, primero verificamos que el elemento actual del arreglo se trate "(" o "\[", si es así, metemos ese valor a la pila. En caso de que no sea un símbolo de apertura, se realiza lo siguiente:

* Primero valida que la pila no esté vacía
* Si no esta vacía, validamos de qué expresión de cierre se trata; ya sea que se trate de "\]" o ")", se verifica que al hacer un pop a la pila, la expresión obtenida haga match con la de cierre. Si esto se cumple, continuamos iterando sobre el arreglo de símbolos, si no, termina la función.
* En caso de que no se presente algún problema dentro del ciclo for, se verifica que la pila este vacía para asegurarnos de que no haya símbolos apertura de sobra y presentar el resultado final, sea afirmativo o negativo.

La complejidad de la solución es O(n), ya que estamos empelando operaciones de pila que son constantes pero tenemos un ciclo iterativo con operaciones constantes en su interior.

__Ejercicio seis__

Este ejercicio no se implmentó por falta de tiempo, pero la idea es tener dos arreglos: Uno para horas de inicio de clase, otro para horas de salida. La idea es iterar sobre ambos arreglos de la siguiente manera:
* Comenzar en el segundo elemento del arreglo de hora de inicio. Por medio de un contador llevaremos el conteo de salones, que por defecto, vale siempre 1.
* Con un arreglo anidado, que va a iterar sobre el arreglo de horas de salida, comparamos el inicio de la segunda clase con todos los horarios de salida de clases: Si hora de inicio no es mayor que la hora de fin, aumentamos el valor del conteo de salones.
* El paso anterior lo repetimos a todos los elementos del arreglo del horas de inicio, partiendo de la segunda.
* Obtenemos el valor minimo, que estará registrado en el contadores

Restaría imprimir el resultado. La complejidad de la solución propuesta sería O(n<sup>2</sup>), ya que tenemos ciclos anidados, en los que realizamos operaciones constantes.

__Ejercicio siete__

Para pruebas unitarias, principalmente se empleo la instrucción _console.log()_, para que por medio de la consola de JavaScript del navegador safari, depurar errores y observar resultados intermedios.
Con apoyo de html se hacen visibles los resultados finales en una interfaz sencilla, una muestra de ellos se encuentra en la carpeta Evidencias del presente repositorio.
