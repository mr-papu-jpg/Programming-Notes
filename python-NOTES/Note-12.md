# Comprension de Listas.

Imagina que quieres crear una lista de los cuadrados de los numeros del 0 al 1.

**Usamos comprension de listas**:

```python
cuadrados=[n**2 for n in range(5)]
```

## La formula magica

La estructura siempre es: *[expresion for elemento in iterable if condicion]*.

| Parte | Descripcion |
|:---:|:---:|
| **Exprecion** | Lo que quieres que se guarde en la lista como resultado |
| **Elemento** | La variable temporal que toma el valor del ciclo |
| **Iterable** | Lista de datos (lista, rango, ect) |
| **Condicion** | (Opcional) un if para filtrar elementos que estran |

### Ejemplo con filtro (solo numeros pares):

```python
pares[n for n in range(10) if n % 2 == 0]
#Resultado: [0, 2, 4, 6, 8]
```

## Crear listas con range()

La funcion range() no crea una liata por si sola, crea un objeto de rango, para convertirlo en una lista usamos la funcion list().

### Sintaxis de range(inicio, fin, paso).

* Inicio: es Opciona, por defecto empieza por 0.

* Fin: donde termina, no incluye ese numero.

* Paso (opcional): Es la opcion de cada cuanto salta de otra interacion.

```python
#lista del 0 al 9
numeros= list(range(10))

#lista del 5 al 15
rango_especifico= list(range(5, 16))

#lista de numeros de 10 en 10 hasta 50
decenas= list(range(0, 51, 10))
```

## Por que es una practica comun?

En python la compresion de lista se usa constantemente para:

* **1. Inicializar ceros**: Crear listas de ceros o valores vbase rapidamente.

* **2. Filtrar colecciones**: crea una lista a partir de una grande a travez de solo una linea.

* **3. Rendimiento**: La practica de compresion xe listas es la mas optimizada, mas que el uso de appends en un bucle for.
