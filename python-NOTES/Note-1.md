# Listas

A lo que en otros leguajes como Java, JavaScript, c y c++ se le conoce este termino como arrays o vectores o matrizes por ai llegan a ser de mas dimensiones, a este se le conoce como "listas", elementos de cualquier tipo sea numerico, strign, float, ect... puede estar dentro de estas listas.

## Definicion:

Se definen con corchetes, el indice empieza con 0:


```python
#creando una lista de equipo pokemon
equipo = ["pikachu", "charizard", "Bulbasaur"]

#Acceso por indice
print(equipo[0]) #salida: pikachu

#indice negativo (empieza desde el final)
print(equipo[-1]) # salida: Bulbasaur (el ultimo)

```

## Modificacion

A diferencia de las *tuplas*, las listas se pueden transformar:

```python
#Cambiar un elementos
equipo[1]="Arcanine"

#Agregar al final
equipo.append("Newtwo")

#Insertar una posicion especifica al indice

equipo.insert(1, "Squirtle")

#Eliminar por valor
equipo.remove("Pilachu")

#Eliminar el ultimo y guardarlo
ultimo= equipo.pop()
```

## Slicing (rebanado): el poder de python.

Esymta es una de las partes mas importantes para dominar python avanzado, te permite extraer porciones de la lista, **Sintaxis**: lista[inicio:fin:paso].

```python
numeros=[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

#Del indice 1 al 5 (el 5 no se incluye)
print(numeros[2:5]) #[2, 3, 4]

#Los primeros 3 numeros
print(numeros[:3]) #[0, 1, 2]

#saltando de 2 en 2
print(numeros[::2]) #[0, 2, 4, 6, 8]

#Invertir la lista (truco clasico)
print(numeros[::-1]) # la lista invertida XD

```

Otra forma para crear listas es la siguiente:

```python
#Ejemplo: crear una lista de los numeros cuadrados pares del 0 al 9
cuadrados_pares=[x**2 for x in range(10) if x % 2 ==0]

print(cuadrados_pares) # [4, 16, 36, 64]
```

### Resumen de metodos a memorizar

* **.append()**:
    aniade al final
* **.extend()**:
    Une una lista a otra.
* **.sort()**:
    Ordena la lista (modifica la original)
* **.reverse()**:
    Invierte el orden.
* **len()**:
    Devuelve el tamanio de la lista.
