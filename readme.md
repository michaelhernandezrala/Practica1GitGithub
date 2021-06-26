*Respuestas al ejercicio 1*

-¿Qué comando utilizaste en el paso 11? ¿Por qué?
 
 Se puede hacer de dos maneras:

   a) git reset HEAD~1 + git restore  
   b) git reset --hard HEAD~1

 En los comandos del apartado a) el comando reset nos permite mover tanto el 
 puntero HEAD como la rama actual a un determinado commit y el comando 
 restore nos permite restaurar todos los archivos de un determinado commit
 en nuestro working copy. 
 El comando del apartado b) nos permite ejecutar los dos comandos del 
 apartado a) de una sola vez.

-¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

 Para ello primero hacemos uso del comando git reflog. Con el obtenemos un 
 historial de todas las operaciones que se han realizado hasta el momento.
 De la información mostrada hemos de localizar el identificador del commit 
 que ha realizado en el apartado 9. Una vez localizado, hacemos uso del
 reset --hard para mover tanto el puntero HEAD como la rama STYLED a ese commit
 y recuperar la version correcta del fichero.
 De esa manera, se rehace el commit deshecho.
 
-El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
 
 No se produce ningún conflicto. Esto es debido a que el merge que se produce
 es de tipo fast forward. Esto es debido a que el commit en el que se 
 encuentra el branch MASTER es padre del branch STYLED.

-El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?  

 Sí porque un mismo archivo ha sido editado en varias lineas iguales 
 en dos ramas diferentes, HTMLIFY y STYLED.
 
-El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
 No se produce ningún conflicto. Esto es debido a que el merge que se produce
 es de tipo fast forward. Esto es debido a que el commit en el que se 
 encuentra el branch MASTER es padre del branch STYLED.

-¿Qué comando o comandos utilizaste en el paso 25?

 Se ha hecho uso del comando git log --graph

-El merge del paso 26, ¿Podría ser fast forward? ¿Por qué? 

 Si porque la rama MASTER sabe como llegar a la rama TITLE.

-¿Qué comando o comandos utilizaste en el paso 27? 
 
 Se ha hecho uso del comando git reset HEAD~1 para volver al commit anterior

-¿Qué comando o comandos utilizaste en el paso 28? 

 git restore git-nuestro.md

-¿Qué comando o comandos utilizaste en el paso 29? 
 
 git branch -D title

-¿Qué comando o comandos utilizaste en el paso 30?

 Haciendo uso del git reflog localizamos el identificador del commit realizado en el 
 apartado 23 en el que se añade el título al poema. Hacemos un git checkout id_commit 
 y luego volveríamos a crear la rama title con el comando git branch title

-¿Qué comando o comandos usaste en el paso 32?

 Hacemos uso del comando git log y copiamos el id del primer commit que se hizo. 
 Después ejecutamos el comando git reset id (copiamos el id que hemos copiado)

-¿Qué comando o comandos usaste en el punto 33?

 Hacemos uso del comado git reflog y copiamos el id del commit que se realizo en el 
 apartado 23 y despues ejecutamos el comando git reset id (id del commit copiado)


