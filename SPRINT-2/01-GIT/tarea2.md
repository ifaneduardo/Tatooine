# Como hacer un flujo de trabajo en GIT.
¡Bienvenido! Estas a punto de aprender como se lleva a cabo un flujo de trabajo en GIT.
Pero primero, vamos con lo basico... *¿Que es GIT?*

![Que es GIT](https://www.generadormemes.com/media/created/k291mby0rknbjs2nu6u1o1vwam3eghi3an7rx6za05p0r9hl0chjysq4l4xslh8.jpg)
Git es un sistema de control de versiones que te permite regresar en el tiempo a ciertos momentos de tu código o documento. 
Si en algún momento del proyecto queremos volver a una versión anterior podríamos anticiparnos y no correr el riesgo de perder algún archivo que estará dentro de nuestro proyecto. Dada la facilidad para trabajar con ramas en Git, hay que ser cuidadosos y no caer en el error de crear ramas descontroladamente haciendo que el repositorio resulte caótico.

***Los 3 comandos básicos para agregar nuestro proyecto a Github, son:***
~~~
    git add .
    git commit -m "Nombre de la nueva versión"
    git push -u origin 
~~~

![GIT](http://www.senin.org/wp-content/uploads/2016/08/index1@2x.png)
Si aun no estas muy familiarizado con las fases de GIT, [¡Da click aqui!](https://github.com/ifaneduardo/Tatooine/blob/develop/SPRINT-2/01-GIT/README.md)

***Nuestro repositorio local (la carpeta que clonamos) tiene 3 diferentes fases por la cual pasa nuestro código:***
1. Working directory: En esta parte podemos hacer cualquier cambio y no afectar nuestro repositorio.
2. Staging area: Archivos modificados.
3. Git repository: Archivos confirmados.

***El código tiene 3 estatus principalees en cada diferente fase, pero en KondoSoft manejamos 5:***
1. Untracked: No se lleva un registro de/los archivo(s).
2. Tracked: Ya existe un registro de/los archivo(s).
3. Modified: El/los archivo(s) estan siendo modificado.
4. Staged: El/los archivo(s) ya se añadieron y estan listos para hacer un snapshot o un commit.
5. commited: El/los archivo(s) fueron respaldados y se les hizo un snapshot en el tiempo.
***(Nosotros profundizaremos solo en Modified, Staged y Commited).***
___
#### Fase 1: “Working Directory”.
En cuanto modificamos algo de nuestro código, éste tiene status de modificado.
Si ejecutamos el comando git status, nos mostrará qué archivos han sido modificados (o creados).
!["Que es GIT"](https://miro.medium.com/max/621/1*xXbJ7u_lw4nTDZqq8mf_tg.png).
Después de que hicimos los cambios necesarios, pasamos a la siguiente etapa: Staging Area
~~~
git add .
~~~
Es lo mismo que poner
~~~
git add NombreDelArchivo.text
~~~
Ahora todos los archivos modificados dentro de Working directory los pasamos a Staging Area.
___
#### Fase 2: “Staging Area”
Aquí es donde le podemos dar nombre a nuestra nueva versión. Y crear una “copia” de cómo quedaría nuestra nuestro repositorio en producción.
(Aún no se publica en github, eh!)Para pasar a la fase siguiente de nuestro código (de Staging Area al Git repository), escribimos lo siguiente.
~~~
git commit -m "Aqui va un comentario"
~~~
el "-m" significa que le vamos a agregar un comentario.

Ahora el código pasa de preparado a confirmado.
___
#### Fase 3. “Git repository”
Una vez que el código esta confirmado ya esta listo para sincronizarse con el servidor de Git (en nuestro caso github). Para hacer esto, escribimos:
~~~
git push origin "el nombre del branch"
~~~
Cuando trabajamos un repositorio con varias personas se tiene que descargar los cambios que hizo esa persona, ¡pero hey! si dos personas al mismo tiempo, tratan de meter push en el repositorio mandará un mensaje de que tenemos que primero descargar la versión de la persona que hizo el primer push para después juntarlo y subirlo.
Para eso ejecutamos:
~~~
git pull origin master
~~~
Y git automáticamente agrega los cambios, (y se pasa por el proceso checkout the proyect.
___
¿No quedo del todo claro?¿Entiendes mejor en diagramas que en textos? Pues aqui te dejo un diagrama sobre el flujo antes explicado:
![Diagrama](https://miro.medium.com/proxy/1*D1lbqiz2Y6quKrt00p9DqQ.png).


Ahora podemos ir con mas confianza ejecutar comandos y perder el miedo a romper cosas!!