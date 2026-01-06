# Excepciones

## "Es mejor pedir perdon qur pedir pesmiso"

En lugar de llenar tu codigo de "ifs" para confirmar ciertos condicionales de error, python te anima a hacer un "try" y a atrapar el error si este ocurre.

Estructura basica de try y except:

```python
try:
    numero=int(input("Intrpduce un numero para dividir a 100: "))
    resultado= 100 / numero
    print(f"El resultado es: {numero}")
except ZeroDivisionError:
    print("X. Debes de introducir un numero, no letras")
```

* **try**: es codigo que podria fallar.

* **except**: el bloque que se ejecuta solo si ocurre un error espesifico.

## El bloque completo.

A veces se necesita mas control,;aqui entra los dos nuevos bloques else y finally.

```python
try:
    archivo= open("datos.txt", "r")
except FielNotFoundError:
    print("El archivo no existe")
else:
    #se ejecuta solo si no hubo errores en el try
    print("archivo leido con exito")
finally:
    #Se ejecuta siempre, haya errro o no 
    #ideal para cerrar archivos o bases de datos
    print("limpiando recursos")
```

## Atrapar el objeto del error.

A veces no sabes que tipo de error atrapar y quieres saber que tipo de mensaje o error va aparecer, o aimplemente atrapatlo de forma sencilla.

```python
try:
    resultado= 100 / 0
except Exception as e:
    print(f"Algo salio mal, el error fue: {e}")
```

**Buenas practicas**: no se recomienda hacer esto, se recomienda siempre *atrapar un error espesifico* para asi el interprete pueda ir con un mejor flujo.

## Lanzar errores propios.

Tu tambien puedes crear tu propio error si algo no cumple con las reglas de lo que dtu creaste em tu programa:

```python
def establecer_edad(edad):
    if edad < 0:
        #forzamos un error manualmente
        raise ValueError("La edad no puede ser negativa")
    print(f"Edad establecida: {edad}")

try:
    establecer_edad(-5)
except ValueError as error:
    print(f"Error detectado: {error}")
```

Eso es todo sobre este tema.
