# Sets

Se definen con llaves, igual que los diccionarios a excepcion de que en este caso no se le asigna una pareja de clave y valor.

```python
#Creando un Set
mis_pokemones= {"Pikachu","Charmander","Bulbasaur", "Pikachu"}

print(mis_pokemones)
#Salida: {"Pikachu","Charmander","Bulbasaur"}
#Nota que la repeticion de Pikachu desaparecio
```

* Los Sets no aceptan repeticion en un elemento.

* Nunca estaran ordenados, por lo tanto no se puede buscar como una lista.

## Operaciones basicas

```python
set_vacio= set() #Asi se crea un set set vacio 
#si se hubira igualado con "{}" seria un objeto identificado como diccionario 

frutas= {"manzana", "pera"}

#agregar elementos
furtas.add("naranja")

#eliminar elementos
frutas.remove("pera")

#Verificar si algo esta en el set, esto es extremadamente rapido en sets!
print("manzana" in frutas) #La Salida es True
```

## El superpoder de los Sets

```python
entrenador_a= {"Pikachu", "Squirtle", "Ditto"}
entrenador_b= {"Squirtle","Bulbasaur","Newtwo"}

#1. Intercepcion: que pokemones tienen ambos?
comunes= entrenador_a & entrenador_b #Squirtle

#2. Union: todos los pokemones sin saltar ninguno
todos= entrenador_a | entrenador_b # {"Pikachu","Squirtle","Ditto", "Bulbasaur", "Newtwo"}

#3. Diferencia: que no tiene el "a" que no tenga el "b"
solo_a= entrenador_a - entrenador_b #{"Pikachu", "Ditto"}
```


Eso es todo con el tema de los Sets. :3
