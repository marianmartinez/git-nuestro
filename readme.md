Ejercicio 1

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
  git reset --hard HEAD~1
  El comando 'git reset' nos permite mover una rama(puntero) donde queramos en el grafo.
  La única condición para poder utilizarlo es estar posicionados en la rama (que HEAD esté apuntando a ella)
  y en este caso es así.
  Con HEAD~1 indicamos que queremos movernos una posición en el grafo (volver al commit padre)
  Utilizamos el modificador --hard para, además, descartar los cambios del working directory. (Es como si además del
  'git reset HEAD~1' se realizara un 'git checkout' de cada archivo que tuviéramos en el working directory. 
  Si no incluimos este modificador los cambios del working directory se mantendrían.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
  git reset --hard 'HEAD@{5}'
  Git guarda un log de todas las referencias de lo que ha pasado. Para verlo podemos utilizar el comando 'git reflog'.
  Aquí podemos identificar en qué paso volveríamos a tener el trabajo deseado y volver a él con el comando que he indicado.
  También podíamos utilizar directamente la referencia en lugar de 'HEAD@{5}'. Ej git reset --hard 85124bc
  

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
- ¿Qué comando o comandos utilizaste en el paso 25?
- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
- ¿Qué comando o comandos utilizaste en el paso 27?
- ¿Qué comando o comandos utilizaste en el paso 28?
- ¿Qué comando o comandos utilizaste en el paso 29?
- ¿Qué comando o comandos utilizaste en el paso 30?
- ¿Qué comando o comandos usaste en el paso 32?
- ¿Qué comando o comandos usaste en el punto 33?
