# Intro

Todo el mundo conoce lo que es ["Hello, World!"](http://en.wikipedia.org/wiki/%22Hello,_world!%22_program), cierto?

Bueno, en caso que no lo recuerden, es el primer paso en cualquier lenguaje de programación (o scripting en este caso). Y para ejecutarlo en PowerShell, la manera es la siguiente:

```powershell
Write-Host "Hello, world!"
```

## Variables
Existe la posibilidad de declarar **variables** de diferentes **tipos** posibles, como números, texto, u objetos más complejos. Cada uno de estos tipos tiene una sintaxis particular para la creación y la modificación de cada variable.

Por ejemplo, si queremos declarar una varible que contenga texto, el tipo de variable requerido va a ser un String (cadena de caracteres). Para ello, se puede ejecutar lo siguiente:

```powershell
$text = "Una cadena de caracteres" 
```
En caso contrario, para declarar una variable que contenga números:

```powershell
$number = 5
$number_decimal = 3.7
```

Adicional a esto, estos *objetos* son llamados variables porque tienen la particularidad de que pueden ser *modificados*

```powershell
$number = 5
Write-Host $number
$number = 6+3           #Suma
Write-Host $number
$number = 6-3           #Resta
Write-Host $number
$number = 30/2          #División
Write-Host $number
$number = 4*6           #Multiplicación
Write-Host $number
```

Los símbolos `+`, `/`, `*` son los llamados **operadores** y básicamente se utilizan al igual que en matemática (para operaciones más complejas existen otros métodos).

Pero... ¿qué es eso que figura detrás del "`#`"? Eso se llama **comentario**. Un comentario es una sección de código legible que es ignorado por la línea de comandos.

Para modificar las variables existen varios caminos y uno de ellos es llamando a los **métodos** del objeto. Para el caso de los *strings* (variables que contienen texto), existen métodos para modificar *in-place* el contenido. Por ejemplo, podríamos obtener en mayúscula el texto de una variable de la siguiente manera:

```powershell
$title = "texto a modificar"
$title.ToUpper()                # retorna en la consola: TEXTO A MODIFICAR
```

Es posible **concatenar** Strings de una manera bien simple:

```powershell
$name = "Victor"
$name += " Silva"
$name                           #retorna en la consola: Victor Silva
```
Donde esencialmente, se están combinando 2 Strings en una. Otro ejemplo utilizando un operador:

```powershell
$language = "PowerShell"
$language * 2                   # retorna en la consola: PowerShellPowerShell
```