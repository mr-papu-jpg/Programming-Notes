# Clases

Las clases en python es la forma estandar de definir un conjunto de objetos de su clase perteneciente XD jajajaja, yo veo un objeta mas de la manera de JavaScript.

## pass

Si en python se deja una clase o condicional en blanco o cualquier otra estructura, esta daria error.

*pass* siver para decirle al interprete de python "no hagas nada", eso es todo, se usa para dejar estructuras en blanco mientras quieres que el programa corra de forma efuciente.

```python
class EnemigoFinal:
    pass
```

## Como definir una clase?

Las clases son el molde o el plano de los objetos, por convencio se usa PascalCase (pirmera letra en cada palabra en mayuscula).

```python
class Pokemon:
    reino="Animalia"
```

## Como crear un constructor?

Un cosntructor es una funcion especial que inicializa la creacion del objeto pasandole los atributos en sus parametros.

* **self**: es oblogatorio, representa a "este objeto en particular".

```python
class Pokemon:
    def __init__(self, nombre, tipo, nivel):
        self.nombre= nombre
        self.tipo= tipo
        self.nivel= nivel

#Creando el objeto:
mi_pika= Pokemon("Pikachu", "Electrico", 25)
print(mi_pika.nombre) #acceso directo
```

## como crear propiedades privadas?

A difierencia de muchos lengujes, en python no existen propiedades privadas, sin embargo, hay convenciones de que algo no debe de tocarse hacia afuera.

**ejemplo**:

```python
class Jugador:
    def __init__(self, nickname):
        self.nickname= nickname
        self.__vida= 100 #privada, madie la debe cambiar directamente
        self.inventario=[]

    def recibir_danio(self, cantidad):
        self.__vida -= cantidad
        if self.__vida < 0:
            self.vida = 0
            print(f"{self.nickname} ahora tiene {self.__vida} de vida.")

    def curar(self, cantidad):
        pass

p1=Jugador("Ang11")
p1.recibir_danio(20)
#p1.__vida= 500 # esto no se puede
```
