## Bandit Nivel 0

**Objetivo:**  
Encontrar la contraseña del siguiente nivel.

**Comandos utilizados:**
bash
ls
cat readme

## Explicacion
Se listaron los archivos del directorio y se leyó el archivo que contenía la contraseña.

## Contraseña obtenida:
ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If



## Bandit Level 1

**Objetivo:**  
Encontrar la contraseña del siguiente nivel almacenada en un archivo llamado `-`.

**Comandos utilizados:**
bash
ls
cat ./-

## Explicacion
Se listaron los archivos del directorio y se utilizó una ruta relativa para poder leer un archivo con nombre especial.

## Contraseña obtenida:
263JGJPfgU6LtdEvgfWU1XP5yac29mFx



## Bandit Level 2

**Objetivo:**  
Encontrar la contraseña del siguiente nivel almacenada en un archivo con espacios y guiones en su nombre.

**Comandos utilizados:**
bash
ls
cat -- "--spaces in this filename--"

## Explicacion
Se utilizaron comillas para que la terminal interpretara correctamente el nombre del archivo que contiene espacios.

## Contraseña obtenida:
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx



## Bandit Level 3

**Objetivo:**  
Encontrar la contraseña del siguiente nivel en un archivo oculto dentro del directorio `inhere`.

**Comandos utilizados:**
bash
ls -la
cat ...Hiding-From-You

## Explicacion
Se accedió al directorio indicado y se listaron los archivos ocultos utilizando la opción -a. Luego se leyó el archivo oculto que contenía la contraseña.

## Contraseña obtenida:
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ



## Bandit Level 4

**Objetivo:**  
Encontrar la contraseña del siguiente nivel almacenada en el único archivo legible por humanos dentro del directorio `inhere`.

**Comandos utilizados:**
bash
cd inhere
file ./*
cat ./-fileXX

## Explicacion
Se analizó el tipo de cada archivo con el comando file para identificar el único archivo de texto legible, el cual contenía la contraseña.

## Contraseña obtenida:
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw



## Bandit Level 5

**Objetivo:**  
Encontrar la contraseña del siguiente nivel en un archivo dentro del directorio `inhere` que sea legible por humanos, tenga un tamaño de 1033 bytes y no sea ejecutable.

**Comandos utilizados:**
bash
cd inhere
find . -type f -size 1033c ! -executable
cat ./ruta/del/archivo

**Explicacion:**  
Se utilizó el comando find con filtros de tipo, tamaño y permisos para localizar el único archivo que cumple con todas las condiciones indicadas.

## Contraseña obtenida:
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG



## Bandit Level 6

**Objetivo:**  
Encontrar la contraseña del siguiente nivel almacenada en un archivo del sistema que pertenezca al usuario bandit7, al grupo bandit6 y tenga un tamaño de 33 bytes.

**Comandos utilizados:**
bash
find / -type f -size 33c -user bandit7 -group bandit6 2>/dev/null
cat /ruta/del/archivo

**Explicacion:**
Se utilizó el comando find desde la raíz del sistema aplicando filtros por tamaño, propietario y grupo. Se redirigieron los errores para evitar mensajes de permisos denegados.

## Contraseña obtenida:
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj



## Bandit Level 7

**Objetivo:**  
Encontrar la contraseña del siguiente nivel almacenada en el archivo `data.txt` junto a la palabra `millionth`.

**Comandos utilizados:**
bash
ls
grep millionth data.txt

## Explicación:
Se utilizó el comando grep para buscar la línea que contiene la palabra clave millionth dentro del archivo, identificando así la contraseña correspondiente.

## Contraseña obtenida: 
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc



## Bandit Level 8

**Objetivo:**  
Encontrar la contraseña del siguiente nivel identificando la única línea que aparece una sola vez dentro del archivo `data.txt`.

**Comandos utilizados:**
bash
sort data.txt | uniq -u

## Explicación:
Se ordenaron las líneas del archivo para agrupar las repetidas y luego se utilizó uniq -u para mostrar únicamente la línea que no se repite.

## Contraseña obtenida: 
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM



## Bandit Level 9

**Objetivo:**  
Encontrar la contraseña del siguiente nivel dentro del archivo `data.txt`, identificando una cadena legible precedida por varios caracteres `=`.

**Comandos utilizados:**
bash
strings data.txt | grep "==="

## Explicación:
Se ordenaron las líneas del archivo para agrupar las repetidas y luego se utilizó uniq -u para mostrar únicamente la línea que no se repite.

## Contraseña obtenida: 
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey



## Bandit Level 10

**Objetivo:**  
Encontrar la contraseña del siguiente nivel.

**Comandos utilizados:**
bash
ls -la
cat .hidden

## Explicación:
En este nivel, la contraseña no se encuentra en un archivo visible de forma normal.
Se utilizó el comando ls -la para listar todos los archivos, incluidos los ocultos..
Al identificar el archivo oculto llamado .hidden, se usó el comando cat para mostrar su contenido y así obtener la contraseña del siguiente nivel.

## Contraseña obtenida: 
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

