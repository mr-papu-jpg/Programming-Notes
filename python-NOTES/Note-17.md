# Expreciones Regulares en Python

Las expreciones regulares no son;solo mativas de python, si no de muchoa lenguajes, uno de sus usos es validar textos y emails de webs, muchas veces pasa que queremos valedar cuentas, contrasenias, ect, es la mejor forma de validar textos de forma rapida y segura.

## 1. Modulo "re" y sus funcines principales:

Lo lrimero es hace un `import re`, aqui tienes las funciones comunes de uso:

|**Funcion**|**Que hace?**|
|:--|:--|
|re.match()|Busca el patron al principio de la cadena, si no empieza con eso, devuelve None|
|re.search()|Busca el patron en todo el texto, y devuelve la primera coincidencia que encuentre|
|re.findall()|Busca todas las coincidencias y las devuelve en una lista de strings|
|re.split()|Divide una cadena en partes cada vez que encuentra el patron|
|re.sub()|Sustituye una o mas coincidencias por un texto nuevo (substitulle)|

### Tabla para armar patrones (Metacaracteres)

Esta tabla muestra las sintaxis de patrones para contruir una busqueda o algo similar:

|**Simbolo**|*Descripcion*|*Ejemplo*|
|:--:|:---|:---|
|.|Cualquier caracter, ecepto salto de linea.|"h." coincide con "hola", "hula"|
|^|Indica con que deberia empezar el texto|^Hola|
|$|Indica con que deberia terminar el texto|adios$|
|*|Indica si hay 0 o mas repeticiones|"lo*" coincide con "l", "lo" y "loooooo"|
|+|Una o mas repeticione|"lo+" coincide con "l", "lo" y "loooooo"|
|?|0 o una repeticion (opcional)|"colou?r" coincide con "color" y "colour"|
|{n}|Exactamente n repeticiones|[0-9]{3} indica 3 numeros segidos en este rago definido|

### clases de caracteres (abreviaturas).

|**Simbolo**|Equivale|*Descripcion*|
|:--:|:--|:--|
|\d|[0-9]|Cualquier digito de numero|
|\D|[^0-9]|Cualquier cosa que no sea un numero|
|\w|[a-zA-Z0-9_]|Cualquier caracter alfanumerico (letras, numeros, guion bajo...)|
|\W||Cualquier caracter que no sea alfanumerico.|
|\s|[ \t\n\r\f\v]|Espaciosen blanco, pestanias o saltos de linea|

## 3. Ejemplos basico en Python.

```python
import re 

texto= "mi numero es 123-456 y el de mi amigo es 987-654"

#Buscar el primer telefono
busqueda= re.search(r"\d{3}-\d{3}", texto)
if busqueda:
    print(f"Encontrado: {busqueda.group()}") #group() extrae el texto

#buscar todos loa telefonos
todos= re.findall(r"\d{3}-\d{3}", texto)
print(f"Lista completa: {todos}")
```

Ejemplo de **sub** sustitucion:

```python
texto= "El usuario admin tiene acceso total."

#Cambiamos admin por censurado

nuevo_texto= re.sub(r"admin", "CENSURADO", texto)
print(nuevo_texto)
```

## Tips importantes:

* 1. *Cadenas crudas*: simpre usa la letra "r" antes de las comillas del patron, esto le dice a python que ignore los caracteres de escape.

* 2. *Validacion*: Regex es el rey para validar emails o contrasenias fuertes, siempre usar esta practica para estas tareas o otras similares.
