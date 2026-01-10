# Manejo de **pip**

*pip* es el manejador de paquetes de python, es esencial saber su manejo y como funciona particularmente en tu maquina, en mi caso, yo uso termux, a si que solo veremos como manejarlo en termux y similares (linux...).

```bash
#Confirmar instalacion de python
pkg install python

#asegurarse de pip este actualizado
pip install --upgrade pip
```

## Sintaxis Basica de *pip*

|Comando|Descripcion|
|:--:|:---|
|pip install nombre|Instala una libreria|
|pip uninstall nombre|Desinstala una libreria|
|pip list|Muestra todo lo que tienes instalado|
|pip freeze > requirements.txt|Guarda tu lista de librerias en un archivo (estandar de proyectos)|
|pip show nombre|Muestra detalles de una linreria especifica|

## Librerias que yo voy a instalar

### Desarrollo web:

Para hacer sitios web robustos desde termux:

* **django**: El framework mas completo:  `pip install django`.

* **gunicorn**: Un servidor para poner tu web en produccion.

* **python-dotenv**: para manejar contrasenias y claves secretas de forma segura
