# Manejo de archivos y ficheros

Siempre que habras un archivo, debes de cerrarlo, es una regla de oro, la mejor practica es usar la sentencia **with**.

## 1. Archivo de texto .txt 

La forma mas basica, usamos el archivo, open(archivo, modo).

| **Modo** | **Descripcion** |
|:--|:--|
| r | Read: Solo lectura, error si no existe |
| w | Write: escribe desde cero,;borra el anterior |
| a | Append: aniade contenido al final del archivo |

```python
#Escritura
with open("notas.txt", "w", encoding="utf-8") as archivo:
    archivo.write("Hola, esta es la primera linea")
    archivo.write("Seguimos aprendiendo python, esta es la segunda linea")

#lectura
with open("notas.txt", "r") as archivo:
    contenido=archivo.read()
    print(contenido)
```

## Archivos JSON

Estos a mi parecer son loa mas usados actualmente, por eso es fundamental saber como manejarlos. Se usa el modulo nativo json.

* json.dump(): escribe datos en el archivo.

* json.load(): lee datos de archivo y loa convierte en diccionario.

<!--end list--->

```python
import json

datos={"nombre": "Angel", "puntos": 100, "activo": true}

#Guardar
with open("data.json", "w") as f:
    json.dump(datos, f, indent=4)
    #el indent ayuda a que sea legible

#Leer
with open("data.json", "r") as f:
    mi_diccionario= json.load(f)
```

## Archivos CSV

Los archivos separados por coma se manejas con el modulo csv. Es como una hoja de excel simplificada.

```python
import csv

#Escribir csv
with open("usuarios.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerow([1, "Ana"])
    writer.writerow([2, "Pedro"])

#Leer CSV
with open("usuarios.csv", "r") as f:
    reader= csv.reader(f)
    for fila in reader:
        print(f"ID: {fila[0]}, Nombre: {fila[1]}")
```

# XML

Se usa el modulo xml.etree.ElementTree.

```python
import xml.etree.ElementTree as ET 

#Ejemplo de estructura xml:
#<data><items><item>Valor</item></items></data>

tree= ET.parse('datos.xml')
root= tree.getroot()

for item in root.findall('item'):
    print(item.text)
```

# En excel

Python no lee excel de forma nativa, la libreria estandar es pandas o openpyxl.

```python
#instala antes pandas
import pandas as pd 

#leer excel
df= pd.read_excel("archivo.xlsx")
print(df.head()) #Muestra las primeras 5 filas

#guardar excel
df.to_excel("nuevo_archivo.xlsx", index= False)
```

### recuerda usar el modulo *os*

Se usa mas que todo para el manejo de rutas.

```python
import os

#une captetas de forma inteligente segun du sistema operativo

ruta= ps.path.join("documentos", "tareas", "notas.txt")

with open(ruta, "r") as archivo:
    print(archivo.read())
```

## Resumen

* Context manager(with): usalo siempre para que;python cierre el archivp automaticamente.

* Encoding: usa `encoding="utf-8"` ql abrir archivos de texto para evitar problemas de tildes y la letra enie.

* JSON: ideal para configuraciones de APIs.

* CSV: Ideal para bases de datos simples y hojas de calculo.
