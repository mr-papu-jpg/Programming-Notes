# Comandos de Linux y Termux (1)

## 1. *grep* (El buscador de texto).

imagina que tienes 20 proyectos y necesitas saber que funcion especificamente tiene error o nesecitas corregir.

* **Comando**: grep -r "nombre de la funcion"

* **Para que sirve?**: busca la palabra en todos los archivos actual (ahorra tiempo).

## 2. *find* (El buscador de archivos).

si creaste un archivo y no sabes en que carpeta esta.

* **Comando**: find . -name "App.tsx"

* **Para que sirve**: localiza el archivo en segundos.

## 3. *top* o *htop* (El monitor de recursos)

Como se programa en celular, la memoria RAM es oro.

* **Comando**: htop, si no se tiene instalalo con: pkg install htop.

* **Para que sirve?**: sirve para ver todos los procesos que eatan consumiendo tu bateria y memoria. Es muy viaual y te permite cerrar procesos que se hayan quedado "pegados" (usando F9 o k).

## 4. *mkdir -p* (crear rutas completas):

Sirve para no hacer la tarea repetitiva de: crear una carpeta, abrir la carpeta creada, crear otra carpeta nueva...

* **Comando**: mkdir -p proyecto/frontend/src/components

* **Para que sirve?**: crea toda la ruta de carpetas de un solo golpe.

## 5. alias (Tus propios atajos).

Si estas cansado de escribir comandos:

* **Ejemplo**: alias g="git status" o alias nv="nvim".

* **Para que sirve?**: Te permite crear "apodos" para los comandos. Puedes guardarlos en el archivo .bashrc o .zshrc para que sean permanentes.

## 6. chmod (Permisos).

A veces intentaras ejecutar un archivo de python o un archivo que te dira "Permission denied".

* **Comando**: chmod +x nombre-del-archivo.sh

* **Para que sirve?**: Le da permiso al archivo para que se comporte como un programa ejecutable.

## 7. du -sh (Cuanto pesa tu proyecto?).

Las caroetas de node_modules en React, son famosas por ser demasiado pesadas.

* **Comando**: du -sh *

* **Para que sirve?**: Te dice cuanto espacio ocupa cada carpeta, ideal para saber que borrarsi te quedas sin espacio en el dispositivo.

### Esos son los comandos por ahora :3
