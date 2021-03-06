# Git and Github Course
![banner](https://miro.medium.com/max/700/1*Jl2VDHVzFBDdXggRprziUg.png)

### Qué es Git

Git es una herramienta que realiza una función del control de versiones de código de forma distribuida, de la que destacamos varias características:

1. Es muy potente
2. Fue diseñada por Linus Torvalds
3. No depende de un repositorio central
4. Es software libre
5. Con ella podemos mantener un historial completo de versiones
6. Podemos movernos, como si tuviéramos un puntero en el tiempo, por todas las revisiones de código y desplazarnos una manera muy ágil.
7. Es muy rápida
8. Tiene un sistema de trabajo con ramas que lo hace especialmente potente
9. En cuanto a la funcionalidad de las ramas, las mismas están destinadas a provocar proyectos divergentes de un proyecto principal, para hacer experimentos o para probar nuevas 10. funcionalidades.
11. Las ramas pueden tener una línea de progreso diferente de la rama principal donde está el core de nuestro desarrollo. En algún momento podemos llegar a probar algunas de esas 12. mejoras o cambios en el código y hacer una fusión a nuestro proyecto principal, ya que todo esto lo maneja Git de una forma muy 

## Texto plano

Un Texto plano (plain text), son aquellos archivos formados exclusivamente por texto (sólo caracteres), sin ningún formato; es decir, no requieren ser interpretados para leerse (aunque pueden ser procesados en algunos casos). También son llamados archivos de texto llano, simple o sin formato. En otras palabras, son archivos que contienen solo texto, pero no hay información sobre el tipo de letra, ni formas (negrita, subrayados...), ni tamaños.

## Configuración Básica

Configurar Nombre que salen en los commits
```ssh
	git config --global user.name "dasdo"
```
Configurar Email
```ssh	
	git config --global user.email dasdo1@gmail.com
```
Marco de colores para los comando
```ssh
	git config --global color.ui true
```

## Iniciando repositorio

Iniciamos GIT en la carpeta donde esta el proyecto
```ssh
	git init
```
Añadimos todos los archivos para el commit
```ssh
	git add .
```
Hacemos el primer commit
```ssh
	git commit -m "Texto que identifique por que se hizo el commit"
```
subimos al repositorio
```ssh
	git push origin master
```
## Estados en Git

### Committed
Tras hacer un commit y tener tus camboos confirmados tienes la certeza de que todos los datos se han almacenado de forma segura en tu línea del tiempo de Git

### Modified

Cuando hay una modificación en algún archivo el estado modified nos indica que esa modificación ha sido detectada pero no está a salvo ya que todavía no se ha confirmado que se quieren guardar esos datos.

### Staged

El estado staged nos indica que se han puesto en cola uno o varios archivos modificados, en su versión actual, para que se incluyan en el próximo commit y poder ser guardados definitivamente en la línea temporal de nuestra base de datos de Git.

## Ramas en git

Cuando hablamos de ramificaciones, significa que tú has tomado la rama principal de desarrollo (master) y a partir de ahí has continuado trabajando sin seguir la rama principal de desarrollo. En muchos sistemas de control de versiones este proceso es costoso, pues a menudo requiere crear una nueva copia del código, lo cual puede tomar mucho tiempo cuando se trata de proyectos grandes.

1. Master
Es la rama principal. Contiene el repositorio que se encuentra publicado en producción, por lo que debe estar siempre estable.

2. Development
Es una rama sacada de Master. Es la rama de integración, todas las nuevas funcionalidades se deben integrar en esta rama. Luego que se realice la integración y se corrijan los errores (en caso de haber alguno), es decir que la rama se encuentre estable, se puede hacer un merge de development sobre la rama Master.

3. Release
Las ramas de release apoyan la preparación de nuevas versiones de producción. Para ellos se arreglan muchos errores menores y se preparan adecuadamente los metadatos. Se suelen originar de la rama develop y deben fusionarse en las ramas master y develop

### Origin
Origin es simplemente el nombre predeterminado que recibe el repositorio remoto principal contra el que trabajamos. Cuando clonamos un repositorio por primera vez desde GitHub o cualquier otro sistema remoto, el nombre que se le da a ese repositorio "maestro" es precisamente origin.

### Head
Se refiere al commit en el que está tu repositorio posicionado en cada momento. Por regla general HEAD suele coincidir con el último commit de la rama en la que estés, ya que habitualmente estás trabajando en lo último. Pero si te mueves hacia cualquier otro commit anterior entonces el HEAD estará más atrás.

### Log
El comando que podemos usar para ver el histórico de commits, estando situados en la carpeta de nuestro proyecto.

## ¿Qué es un Branch (rama) y cómo funciona un Merge en Git?
Git es una base de datos muy precisa con todos los cambios y crecimiento que ha tenido nuestro proyecto. Los commits son la única forma de tener un registro de los cambios. Pero las ramas amplifican mucho más el potencial de Git.

Todos los commits se aplican sobre una rama. Por defecto, siempre empezamos en la rama master (pero puedes cambiarle el nombre si no te gusta) y creamos nuevas ramas, a partir de esta, para crear flujos de trabajo independientes.

Crear una nueva rama se trata de copiar un commit (de cualquier rama), pasarlo a otro lado (a otra rama) y continuar el trabajo de una parte específica de nuestro proyecto sin afectar el flujo de trabajo principal (que continúa en la rama master o la rama principal).

Los equipos de desarrollo tienen un estándar: Todo lo que esté en la rama master va a producción, las nuevas features, características y experimentos van en una rama “development” (para unirse a master cuando estén definitivamente listas) y los issues o errores se solucionan en una rama “hotfix” para unirse a master tan pronto como sea posible.

Crear una nueva rama lo conocemos como Checkout. Unir dos ramas lo conocemos como Merge.

Podemos crear todas las ramas y commits que queramos. De hecho, podemos aprovechar el registro de cambios de Git para crear ramas, traer versiones viejas del código, arreglarlas y combinarlas de nuevo para mejorar el proyecto.

Solo ten en cuenta que combinar estas ramas (sí, hacer “merge”) puede generar conflictos. Algunos archivos pueden ser diferentes en ambas ramas. Git es muy inteligente y puede intentar unir estos cambios automáticamente, pero no siempre funciona. En algunos casos, somos nosotros los que debemos resolver estos conflictos “a mano”.


## GIT CLONE

Clonamos el repositorio de github o bitbucket
```ssh
	git clone <url>
```
Clonamos el repositorio de github o bitbucket ?????
```ssh
	git clone <url> git-demo
```

## GIT ADD


Añadimos todos los archivos para el commit
```ssh
	git add .
```
Añadimos el archivo para el commit
```ssh
	git add <archivo>
```
Añadimos todos los archivos para el commit omitiendo los nuevos
```ssh
	git add --all 
```
Añadimos todos los archivos con la extensión especificada
```ssh
	git add *.txt
```
Añadimos todos los archivos dentro de un directorio y de una extensión especifica
```ssh
	git add docs/*.txt
```
Añadimos todos los archivos dentro de un directorios
```ssh
	git add docs/
```
## GIT COMMIT

Cargar en el HEAD los cambios realizados
```ssh
	git commit -m "Texto que identifique por que se hizo el commit"
```
Agregar y Cargar en el HEAD los cambios realizados
```ssh
	git commit -a -m "Texto que identifique por que se hizo el commit"
```
De haber conflictos los muestra
```ssh
	git commit -a 
```
Agregar al ultimo commit, este no se muestra como un nuevo commit en los logs. Se puede especificar un nuevo mensaje
```ssh
	git commit --amend -m "Texto que identifique por que se hizo el commit"
```

## GIT PUSH

Subimos al repositorio
```ssh
	git push <origien> <branch>
```
Subimos un tag
```ssh
	git push --tags
```
## GIT LOG

Muestra que cambios hubo en un archivo
```ssh
	git show <archivo>
```
Muestra los logs de los commits
```ssh
	git log <archivo>
```
Muestras los cambios en los commits
```ssh
	git log --oneline --stat
```
Muestra graficos de los commits
```ssh
	git log --oneline --graph
```
## GIT DIFF

Muestra los cambios realizados a un archivo
```ssh
	git diff <archivoId>
	git diff --staged
```
Muestra las diferencias en dos archivos
```ssh
	git diff <commitAid> <commitBid>
```

![clase apointment](https://static.platzi.com/media/user_upload/Analizar%20cambios%20en%20los%20archivos%20de%20tu%20proyecto%20con%20Git-f6f2fe08-e2e9-46ef-86fa-6180354bc151.jpg)

## ¿Qué es el staging y los repositorios? Ciclo básico de trabajo en Git

Para iniciar un repositorio, o sea, activar el sistema de control de versiones de Git en tu proyecto, solo debes ejecutar el comando git init.

Este comando se encargará de dos cosas: primero, crear una carpeta .git, donde se guardará toda la base de datos con cambios atómicos de nuestro proyecto; y segundo, crear un área que conocemos como Staging, que guardará temporalmente nuestros archivos (cuando ejecutemos un comando especial para eso) y nos permitirá, más adelante, guardar estos cambios en el repositorio (también con un comando especial).

Ciclo de vida o estados de los archivos en Git:

Cuando trabajamos con Git nuestros archivos pueden vivir y moverse entre 4 diferentes estados (cuando trabajamos con repositorios remotos pueden ser más estados, pero lo estudiaremos más adelante):

1. Archivos Tracked: son los archivos que viven dentro de Git, no tienen cambios pendientes y sus últimas actualizaciones han sido guardadas en el repositorio gracias a los comandos git add y git commit.
2. Archivos Staged: son archivos en Staging. Viven dentro de Git y hay registro de ellos porque han sido afectados por el comando git add, aunque no sus últimos cambios. Git ya sabe de la existencia de estos últimos cambios, pero todavía no han sido guardados definitivamente en el repositorio porque falta ejecutar el comando git commit.
3. Archivos Unstaged: entiéndelos como archivos “Tracked pero Unstaged”. Son archivos que viven dentro de Git pero no han sido afectados por el comando git add ni mucho menos por git commit. Git tiene un registro de estos archivos, pero está desactualizado, sus últimas versiones solo están guardadas en el disco duro.
4. Archivos Untracked: son archivos que NO viven dentro de Git, solo en el disco duro. Nunca han sido afectados por git add, así que Git no tiene registros de su existencia.
Recuerda que hay un caso muy raro donde los archivos tienen dos estados al mismo tiempo: staged y untracked. Esto pasa cuando guardas los cambios de un archivo en el área de Staging (con el comando git add), pero antes de hacer commit para guardar los cambios en el repositorio haces nuevos cambios que todavía no han sido guardados en el área de Staging (en realidad, todo sigue funcionando igual pero es un poco divertido).

## Comandos para mover archivos entre los estados de Git
Nos permite ver el estado de todos nuestros archivos y carpetas.
```ssh
	git status
```
Nos ayuda a mover archivos del Untracked o Unstaged al estado Staged. Podemos usar git nombre-del-archivo-o-carpeta para añadir archivos y carpetas individuales o git add -A para mover todos los archivos de nuestro proyecto (tanto Untrackeds como unstageds).
```ssh
	git add <archivo>
```
Nos ayuda a sacar archivos del estado Staged para devolverlos a su estado anterior. Si los archivos venían de Unstaged, vuelven allí. Y lo mismo se venían de Untracked.
```ssh
	git reset HEAD <archivo>
```
Nos ayuda a mover archivos de Unstaged a Tracked. Esta es una ocasión especial, los archivos han sido guardados o actualizados en el repositorio. Git nos pedirá que dejemos un mensaje para recordar los cambios que hicimos y podemos usar el argumento -m para escribirlo (git commit -m "mensaje").
```ssh
	git commit
```
Eliminar archivos o regresarlos a Untracked:
Este comando nos ayuda a eliminar archivos de Git sin eliminar su historial del sistema de versiones. Esto quiere decir que si necesitamos recuperar el archivo solo debemos “viajar en el tiempo” y recuperar el último commit antes de borrar el archivo en cuestión.
```ssh
	git rm: este comando necesita alguno de los siguientes argumentos para poder ejecutarse correctamente:
	- git rm --cached: Mueve los archivos que le indiquemos al estado Untracked.
	- git rm --force: Elimina los archivos de Git y del disco duro. Git guarda el registro de la existencia de los archivos, por lo que podremos recuperarlos si es necesario 	  (pero debemos usar comandos más avanzados).
```
Podemos volver a cualquier versión anterior de un archivo específico o incluso del proyecto entero. Esta también es la forma de crear ramas y movernos entre ellas.
```ssh 
git checkout + ID 
```
Borra toda la información que tengamos en el área de staging (y perdiendo todo para siempre. Este comando nos ayuda a volver en el tiempo. Pero no como git checkout que nos deja ir, mirar, pasear y volver. Con git reset volvemos al pasado sin la posibilidad de volver al futuro. Borramos la historia y la debemos sobreescribir. No hay vuelta atrás.
```ssh
git reset <id> --hard
```
Mantiene allí los archivos del área de staging para que podamos aplicar nuestros últimos cambios pero desde un commit anterior.
```ssh
git reset <id> --soft
```
![rm and reset](https://static.platzi.com/media/user_upload/Presentaci%C3%B3n%20sin%20t%C3%ADtulo%20%281%29-273bafef-16e4-4076-892c-1e10d3409c94.jpg)
Devuelve el ultimo commit que se hizo y pone los cambios en el estado anterior.
```ssh
	git reset --soft HEAD^
```
Devuelve el ultimo commit y todos los cambios
```ssh
	git reset --hard HEAD^
```
Devuelve los 2 ultimo commit y todos los cambios
```ssh
	git reset --hard HEAD^^
```
Rollback merge/commit
```ssh
	git log
	git reset --hard <commit_sha>
```
![Status git](https://static.platzi.com/media/user_upload/estados-git-0acb84f7-5080-4098-99d9-59012a3b8e86.jpg)

## GIT REMOTE

Agregar repositorio remoto
```ssh
	git remote add origin <url>
```
Cambiar de remote
```ssh
	git remote set-url origin <url>
```
Remover repositorio
```ssh
	git remote rm <name/origin>
```
Muestra lista repositorios
```ssh
	git remote -v
```
Muestra los branches remotos
```ssh	
	git remote show origin
```
Limpiar todos los branches eliminados
```ssh
	git remote prune origin 
```
## 
Nos permite descargar los archivos de la última versión de la rama principal y todo el historial de cambios en la carpeta .git.
```ssh
	git clone url_del_servidor_remoto 
```
Luego de hacer git add y git commit debemos ejecutar este comando para mandar los cambios al servidor remoto.
```ssh
	git push
```
Lo usamos para traer actualizaciones del servidor remoto y guardarlas en nuestro repositorio local (en caso de que hayan, por supuesto).
```ssh
	git fetch
```
También usamos el comando git merge con servidores remotos. Lo necesitamos para combinar los últimos cambios del servidor remoto y nuestro directorio de trabajo.
```ssh
	git merge
```
Básicamente, git fetch y git merge al mismo tiempo.
```
git pull
```

## GIT BRANCH

Crea un branch
```ssh
	git branch <nameBranch>
```
Lista los branches
```ssh
	git branch
```
Comando -d elimina el branch y lo une al master
```ssh
	git branch -d <nameBranch>
```
Elimina sin preguntar
```ssh
	git branch -D <nameBranch>
```
Cambiar entre ramas
```
	git checkout -b rama
```
## Crear un nuevo commit en la rama master combinando

los cambios de la rama cabecera:
```shh
	git checkout master
	git merge cabecera
```
# Crear un nuevo commit en la rama cabecera combinando

los cambios de cualquier otra rama:
```ssh
	git checkout cabecera
	git merge cualquier-otra-rama
```

## GIT REMOTE

Agregar repositorio remoto
```ssh
	git remote add origin <url>
```
Cambiar de remote
```ssh
	git remote set-url origin <url>
```
Remover repositorio
```ssh
	git remote rm <name/origin>
```
Muestra lista repositorios
```ssh
	git remote -v
```
Muestra los branches remotos
```ssh	
	git remote show origin
```
Limpiar todos los branches eliminados
```ssh
	git remote prune origin 
```
## Apuntes de la clase
```ssh
	# Primero: Guardar la URL del repositorio de GitHub
	# con el nombre de origin
	git remote add origin URL

	# Segundo: Verificar que la URL se haya guardado
	# correctamente:
	git remote
	git remote -v

	# Tercero: Traer la versión del repositorio remoto y
	# hacer merge para crear un commit con los archivos
	# de ambas partes. Podemos usar git fetch y git merge
	# o solo el git pull con el flag --allow-unrelated-histories:
	git pull origin master --allow-unrelated-histories

	# Por último, ahora sí podemos hacer git push para guardar
	# los cambios de nuestro repositorio local en GitHub:
	git push origin master
```

## LLave Pública y Llave Privada

Las llaves públicas y privadas nos ayudan a cifrar y descifrar nuestros archivos de forma que los podamos compartir sin correr el riesgo de que sean interceptados por personas con malas intenciones.

La forma de hacerlo es la siguiente:

1. Ambas personas deben crear su llave pública y privada.
2. Ambas personas pueden compartir su llave pública a las otras partes (recuerda que esta llave es pública, no hay problema si la “interceptan”).
3. La persona que quiere compartir un mensaje puede usar la llave pública de la otra persona para cifrar los archivos y asegurarse que solo puedan ser descifrados con la llave privada de la persona con la que queremos compartir el mensaje.
4. El mensaje está cifrado y puede ser enviado a la otra persona sin problemas en caso de que los archivos sean interceptados.
5. La persona a la que enviamos el mensaje cifrado puede usar su llave privada para descifrar el mensaje y ver los archivos.
6. Puedes compartir tu llave pública pero nunca tu llave privada.


## Configura tus llaves SSH en local

Esta funcionalidad nos permite crear una llave publica y privada, esto nos permite agregar a nuestro github una coneccion mas segura entre nuestro usuario git y nuestro github.

1. Primer paso: Generar tus llaves SSH. Recuerda que es muy buena idea proteger tu llave privada con una contraseña.
```ssh
	ssh-keygen -t rsa -b 4096 -C "tu@email.com"
	Segundo paso: Terminar de configurar nuestro sistema.
```
2. En Windows y Linux:
```ssh
	# Encender el "servidor" de llaves SSH de tu computadora:
	eval $(ssh-agent -s)

	# Añadir tu llave SSH a este "servidor":
	ssh-add ruta-donde-guardaste-tu-llave-privada
``` 

2. En Mac:

```ssh
	# Encender el "servidor" de llaves SSH de tu computadora:
	eval "$(ssh-agent -s)"

	# Si usas una versión de OSX superior a Mac Sierra (v10.12)
	# debes crear o modificar un archivo "config" en la carpeta
	# de tu usuario con el siguiente contenido (ten cuidado con
	# las mayúsculas):
	Host *
		AddKeysToAgent yes
		UseKeychain yes
		IdentityFile ruta-donde-guardaste-tu-llave-privada

	# Añadir tu llave SSH al "servidor" de llaves SSH de tu
	# computadora (en caso de error puedes ejecutar este
	# mismo comando pero sin el argumento -K):
	ssh-add -K ruta-donde-guardaste-tu-llave-privada
```

## Conexion a Github con ssh
Luego de crear nuestras llaves SSH podemos entregarle la llave pública a GitHub para comunicarnos de forma segura y sin necesidad de escribir nuestro usuario y contraseña todo el tiempo.

Para esto debes entrar a la Configuración de Llaves SSH en GitHub, crear una nueva llave con el nombre que le quieras dar y el contenido de la llave pública de tu computadora.

Ahora podemos actualizar la URL que guardamos en nuestro repositorio remoto, solo que, en vez de guardar la URL con HTTPS, vamos a usar la URL con SSH:
```ssh
git remote set-url origin url-ssh-del-repositorio-en-github
```

## Los tags o etiquetas nos permiten asignar versiones a los commits con cambios más importantes o significativos de nuestro proyecto.

Comandos para trabajar con etiquetas:

Crear un nuevo tag y asignarlo a un commit
```ssh
git tag -a nombre-del-tag id-del-commit
```
Borrar un tag en el repositorio local
```ssh
git tag -d nombre-del-tag
```
Listar los tags de nuestro repositorio local
```ssh
git tag o git show-ref --tags
```
Publicar un tag en el repositorio remoto
```ssh
git push origin --tags
```
Borrar un tag del repositorio remoto
```ssh
git tag -d nombre-del-tag y git push origin :refs/tags/nombre-del-tag.
```

### [More about tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)


