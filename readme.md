# Ejercicio 1
>KC Git & Github Module

### 1- ¿Qué comando utilizaste en el paso 11? ¿Por qué?

``` 
git reset --hard HEAD~1
```

El comando **git reset** nos permite mover una rama (puntero) donde queramos en el grafo.
La única condición para poder utilizarlo es estar posicionados en la rama (que HEAD esté apuntando a ella) y en este caso es así.

Con **HEAD~1** indicamos que queremos movernos una posición en el grafo (volver al commit padre).

Utilizamos el modificador **--hard** para, además, descartar los cambios del *working directory*. Es como si además del
**git reset HEAD~1** se realizara un **git checkout** de cada archivo que tuviéramos en el *working directory*. Si no incluimos este modificador los cambios del working directory se mantendrían.

### 2- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

``` 
git reset --hard 'HEAD@{5}'
``` 
  
Git guarda un log de todas las referencias de lo que ha pasado. Para verlo podemos utilizar el comando **git reflog**.
Aquí podemos identificar en qué paso volveríamos a tener el trabajo deseado y volver a él con el comando indicado. En mi caso como he cambiado de rama y he añadido commits en master, se han añadido referencias nuevas, si no en lugar de un 5 hubiera habido un 1 en el comando.
También podríamos utilizar directamente la referencia en lugar de **'HEAD@{num}'**. Ej. **git reset --hard 85124bc**

### 3- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No causó ningún conflicto, ya que para que un conflicto se de, es necesario que se modifique la misma línea del mismo archivo en dos ramas diferentes y ,en este caso, ambas ramas parten del commit con el archivo creado con el texto inicial y posteriormente sólo se modifica en la rama styled.

### 4- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Sí causó conflicto, ya que el archivo **git-nuestro.md** se ha modificado en las ramas **styled** y **htmlify** coincidiendo en las mismas líneas. Ambas ramas partían con el archivo con el texto inicial y se modificó a posteriori. Así que al absorber styled a htmlify se genera un conflicto porque git no sabe cual de las modificaciones elegir como correcta.
 
### 5- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No causó ningún conflicto, ya que en master no se había hecho ninguna modificación del archivo **git-nuestro.md** desde su creación, y la rama styled se creó a partir de ese commit de creación del archivo. Por lo tanto, al hacerse el *merge* sólo en rama styled se han realizado modificaciones del archivo posteriores a su creación, por lo que git elegiría esos cambios.

### 6- ¿Qué comando o comandos utilizaste en el paso 25?
```
log --graph --decorate --pretty=oneline
```

Podemos crear un alias de este comando con **git config alias.graph "log --graph --decorate --pretty=oneline"**

Tras ésto sólo tendríamos que ejecutar **git graph**

### 7- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
### 8- ¿Qué comando o comandos utilizaste en el paso 27?
### 9- ¿Qué comando o comandos utilizaste en el paso 28?
### 10- ¿Qué comando o comandos utilizaste en el paso 29?
### 11- ¿Qué comando o comandos utilizaste en el paso 30?
### 12- ¿Qué comando o comandos usaste en el paso 32?
