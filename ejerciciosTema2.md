# Ejercicios tema 2

## Ejercicio 1: Hacer un pull request a este proyecto con tests adicionales, si es que faltan (en el momento que se lea este tema)
Ejecutamos el comando `git clone git@github.com:mirismr/tdd-gdg.git` para clonar el repositorio. Y añadimos algunos tests de prueba:
~~~
def testDivision(self):
    self.assertEqual(division(1, 0), -1, "Division correcta")
    self.assertEqual(division(4, 2), 2, "Division correcta")

def testPalindromo(self):
    self.assertEqual(palindromo("hola"), False)
    self.assertEqual(palindromo("aba"), True)
    self.assertEqual(palindromo(1), False)
~~~

Para las funciones:
~~~
def division(a, b):
    if b == 0:
        return -1

    return a/b

def palindromo(cadena):
    if type(cadena) is int or type(cadena) is float:
        return False

    return cadena == cadena[::-1]
~~~

## Ejercicio 2: Para la aplicación que se está haciendo, escribir una serie de aserciones y probar que efectivamente no fallan. Añadir tests para una nueva funcionalidad, probar que falla y escribir el código para que no lo haga (vamos, lo que viene siendo TDD).
Realizado en el ejercicio 1.


## Ejercicio 3:
Yo he usado [Pocha](https://github.com/rlgomes/pocha), una versión de *Mocha* para Python. Podemos seguir la instalación en el link anterior.
Usaré la función *it* para describir los tests.

Así pues, ahora la clase `SoloTest()` que teníamos anteriormente queda de la siguiente forma:

~~~

class SoloTest():
        
    @it('devuelve siempre true')
    def testTrue():
        assert devuelveTrue() == True 

    @it('verifica que los numeros son positivos')
    def testSuma():
    assert sumaPositivos(4,8) == 12
        
    @it('verifica que un numero es multiplo de 3, 5 o 15')
    def testMultiplos():
        assert multiplo3o5o15(3) == 1
        assert multiplo3o5o15(5) == 2
        assert multiplo3o5o15(15) == 3
        assert multiplo3o5o15(7) == 0

    @it('verifica si la division es correcta')
    def testDivision():
        assert division(1, 0) == -1
        assert division(4, 2) == 2

    @it('verifica si una cadena es palindroma')
    def testPalindromo():
        assert palindromo("hola") == False
        assert palindromo("abba") == True
        assert palindromo(1) == False 
~~~

Y al ejecutar el comando `pocha tests.py`, nos saldrá algo similar a la siguiente figura:

![Tests] (img/7.png)