# Vue 3 + TypeScript + Vite

HTML

En primer lugar tenemos cuatro inputs de tipo texto para introducir el nickname, email, contraseña, y numero de telefono, seguido de un boton para guardar al nuevo usuario. 

Despues tenemos otra caja de texto para introducir el id del usuario al que nos referimos y un boton para eliminarlo.

La tabla extendera según la cantidad de usuarios que encuentre a través del script getUser.

Debajo de la tabla tenemos los inputs para poder actualizar los valores. una caja de texto para introducir el nuevo valor y un desplegable para indicar a que item nos referimos.


JAVASCRIPT

Con addUsersHTML añadimos una fila de la tabla con los datos del usuario (excluyendo el password) que ha recibido a través de la llamada.

En getUsers se conecta al get del Backend para obtener todos los usuarios y llamar en bucle a addUsersHTML pasando los valores de cada usuario de uno en uno en cada llamada que se hace en el bucle. Esta funcion es llamada cada vez que se carga la pagina

El script save sera ejecutado al clicar en el boton save. Este script recoge los valores introducidos en las cuatro primeras cajas de texto mencionadas anteriormente y los guardara en userNew. Despues conectara con al post del Backend enviando el userNew a través del json. 

En actualizar es muy parecido a lo que se hace con save, con la diferencia que los valores que recoge son del desplegable option y de la caja valorNew

En borrar recogemos la id en la caja de texto id y conectamos al delete del Backend enviando por url el id del usuario que se va a borrar 