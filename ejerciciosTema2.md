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