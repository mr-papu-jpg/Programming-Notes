# Lambdas.

## Como crear un Lambda?

La sintaxis es muy minimalista, no usas ni return, ni parentesis para los argumentos.

**Estructura**: lambda argumentos : exprecion

### Comparativa:

| **Tipo de funcion** | **codigo** |
|:---:|:---:|
| Normal (def) | `def sumar(a, b): return a+b` |
| Lambda | `sumar= lambda x, y: x+y` |

## Usar Lambdas dentro de funciones.

La verdadera magia ocurre cuando creas funciones dentro de funcienes de clase superior,usando asi la creacion de las Lambdas como funciones de clase inferior.

### Ejemplo: Multiplicador imaginario.

```python
def mi_funcion(n):
    #esta funcion devuelve un lambda que multiplica por n 
    return lambda a : a * n 

#Creando funciones especificas usando la base
duplicador= mi_funcion(2)
triplicador= mi_funcion(3)

print(duplicador(10)) #Salida: 20
print(triplicador(10)) #Salida: 30
```

## Detalles importantes y reglas de oro.

* **Solo una exprecion**: una lambda no puede tener varias lineas de codigo, solo puede ejecutar solo una cosa y devolver el resultado, no puedes poner bucles for o poner bloques try-except complejos dentro de ella.

* **Uso con filter() y map()**: Son las mejores amigas de las lambdas.

    * map(lambda x: x*2, lista): aplica la lambda a toda la lista.

    * filter(lambda x: x > 10, lista): Filtra la lista segun la condicion de la lambda.

* **Legibilidad**: Aunque las lambdas son potentes, una regla de oro es: "si usas una lambda muy compleja, mejor utiliza una funcion def comun", el codigo siempre deb de ser facil de leer para todos.
