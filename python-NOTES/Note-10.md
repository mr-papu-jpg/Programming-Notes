# Modulos / importaciones

Cualquier archivo python es un modulo por defecto.

**herramienta.py**:

```python
def saludar_nombre(nombre):
    return f"Hola, {nombre}"

PI=3.142593 #no se como era exactamente
```

**Uso** en main.py:

```python
import herramienta

print(herramienta.saludar_nombre("Ang11"))
print(herramienta.PI)
```

## Formas de importar un modulo

* *import modulo* es la forma de traer todo lo del modulo, pero sus variables, objetos, funcione, ect, se traen como: *modulo.funcion*.

* *from modulo import funcion* es la forma para traer solo una funcion especifuca de un modulo.

* *import modulo as alias* le cambia el nombre para escribir menks texto, ej: import pandas as pd.

* *form modulo import ** esto trae todo lo del modulo, pero no es recomendado por ser muy pesado.

## Que es *if __name__=="__main__":*,

Esto sirve por lo que entiendo para poner codigo de prueba dentro de esta funcion, aunque debo de investigar esto mejor mas a fondo:

```python
#En herramienta.py 
def sumar(a, b):
    return a+b

if __name__=="__main__":
    #esto solo ejecuta si corres herramienta.py directamente
    print("Probamdo la suma 'sumar':", sumar(4, 5))
```

## Paquetese estruturados en carpetas.

Un paquete simplemente es una carpeta con varios modulos, para que python lo reconosca como paquete, y por buenas practicas (aunque no es necesario), antes se requeriq un archivo vacio llamado __init__.py, actualmente ya no es obligatorio.

**Estructura**:

```text
mi-proyecto/
 |
 |--main.py 
 |
 |--utilidades/
    |
    |--__init__.py 
    |
    |--calculos.py 
    |
    |--red.py 
```

* para importar la carpeta: from utilidades.calculos import sumar_puntos.

## Las 3 fuentes de modulos.

* 1. Standar library: modulo que ya viene con python por defecto.

* 2. Modulos de terceros: instalados con pip.

* 3. Modulos propios: archivos que tu creas.

Eso es todo. :3
