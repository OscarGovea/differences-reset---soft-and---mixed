#Comandos RESET

Con el fin de entender el funcionamiento de los comandos RESET, se dara una pequeña introducción a las zonas de trabajo de Git.
Cuando se modifica un archivo en su repositorio, el cambio al principio no esta preparado para hacer un *commit*. Con el fin de hacerlo (el *commit*, debe ponerla en escena, es decir, añadirlo al git índice usando *add*. Cuando realiza una confirmación (*commit*), los cambios que se cometen son los que se han añadido al índice.
![alt text](https://github.com/OscarGovea/differences-reset---soft-and---mixed/blob/master/WorkingArea.png "Working Area")

##git reset [*mode*] [*commit*]
De esta forma se restablece la cabeza rama actual a *commit* y posiblemente actualiza el índice (que se quede en el árbol de la *commit*) y el árbol de trabajo depende de *modo* . Si se omite *modo*, por defecto es "--mixed".
![alt text](https://github.com/OscarGovea/differences-reset---soft-and---mixed/blob/master/GitReset.png)

##git --soft
No toca el archivo índice o el árbol de trabajo (pero restablece la cabeza a *commit*). Esto deja a todos sus archivos modificados (los cambios que se tiene que hacer con un *commit*) como git status lo pondría.

##git --mixed
Restablece el índice, pero no el árbol de trabajo (es decir, los archivos modificados se conservan pero no marcados para *commit*) e informa de lo que no se ha actualizado. Esta es la acción por defecto.

##Diferencias entre --soft y --mixed
La diferencia entre --mixed y --soft es si el índice se modifica o no.

![alt text](https://github.com/OscarGovea/differences-reset---soft-and---mixed/blob/master/GitResetHard.png "¡Siempre hay mas opciones!")