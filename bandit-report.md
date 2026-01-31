## Bandit Nivel 0

**Objetivo:**  
Encontrar la contraseña del siguiente nivel.
contraseña: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

**Comandos utilizados:**
ls
cat readme

## Bandit Level 1

**Objetivo:**  
Encontrar la contraseña del siguiente nivel almacenada en un archivo llamado `-`.
contraseña: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

**Comandos utilizados:**
ls
cat ./-

## Bandit Level 2

**Objetivo:**  
Encontrar la contraseña del siguiente nivel almacenada en un archivo con espacios y guiones en su nombre.
contraseña: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

**Comandos utilizados:**
ls
cat -- "--spaces in this filename--"

## Bandit Level 3

**Objetivo:**  
Encontrar la contraseña del siguiente nivel en un archivo oculto dentro del directorio `inhere`.
contraseña: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

**Comandos utilizados:**
ls -la
cat ...Hiding-From-You

## Bandit Level 4

**Objetivo:**  
Encontrar la contraseña del siguiente nivel almacenada en el único archivo legible por humanos dentro del directorio `inhere`.
contraseña: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

**Comandos utilizados:**
cd inhere
file ./*
cat ./-fileXX

## Bandit Level 5

**Objetivo:**  
Encontrar la contraseña del siguiente nivel en un archivo dentro del directorio `inhere` que sea legible por humanos, tenga un tamaño de 1033 bytes y no sea ejecutable.

**Explicacion:**  
Se utilizó el comando find con filtros de tipo, tamaño y permisos para localizar el único archivo que cumple con todas las condiciones indicadas.
Contraseña: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

**Comandos utilizados:**
```bash
cd inhere
find . -type f -size 1033c ! -executable
cat ./ruta/del/archivo

## Bandit Level 6

**Objetivo:**  
Encontrar la contraseña del siguiente nivel almacenada en un archivo del sistema que pertenezca al usuario bandit7, al grupo bandit6 y tenga un tamaño de 33 bytes.

**Explicacion:**
Se utilizó el comando find desde la raíz del sistema aplicando filtros por tamaño, propietario y grupo. Se redirigieron los errores para evitar mensajes de permisos denegados.
Contraseña: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

**Comandos utilizados:**
```bash
find / -type f -size 33c -user bandit7 -group bandit6 2>/dev/null
cat /ruta/del/archivo

## Bandit Level 7

**Objetivo:**  
Encontrar la contraseña del siguiente nivel almacenada en el archivo `data.txt` junto a la palabra `millionth`.

## Explicación:
Se utilizó el comando grep para buscar la línea que contiene la palabra clave millionth dentro del archivo, identificando así la contraseña correspondiente.

## Contraseña obtenida: 
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

**Comandos utilizados:**
```bash
ls
grep millionth data.txt

## Bandit Level 8

**Objetivo:**  
Encontrar la contraseña del siguiente nivel identificando la única línea que aparece una sola vez dentro del archivo `data.txt`.

## Explicación:
Se ordenaron las líneas del archivo para agrupar las repetidas y luego se utilizó uniq -u para mostrar únicamente la línea que no se repite.

## Contraseña obtenida: 
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

**Comandos utilizados:**
```bash
sort data.txt | uniq -u
