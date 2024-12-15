# Ejercicios de control de versiones
## SVN
### Actividad 1, Joan y Miquel

Actividad 1: Desarrollo colaborativo
Para el desarrollo colaborativo entre Joan y Miquel, que trabajan en el mismo proyecto de software y con el mismo código fuente, lo más conveniente es utilizar un sistema de control de versiones (SCV). Este sistema les permitirá gestionar de manera eficiente las modificaciones y evitar conflictos. A continuación, se describen los mecanismos y procedimientos que sería más conveniente utilizar:

#### Mecanismos:
- Repositorio centralizado: Utilizar un sistema de control de versiones como Subversion (SVN) para alojar el código fuente de manera centralizada.

- Ramas y fusión: Crear una rama para cada funcionalidad o tarea específica que se trabajará de manera independiente para evitar modificar directamente el código principal.

- Commit y Update regulares: Realizar commits y updates regularmente para evitar perder trabajos hechos y asegurar que se trabaja sobre la versión más actual del proyecto.

#### Explicacion paso a paso:
1. Inicialización del repositorio:
    - Joan y Miquel deben clonar el repositorio central (utilizando `svn co` ).
2. Creación de ramas:
    - Cuando comienzan a trabajar en una nueva funcionalidad, deben crear una rama separada con `svn copy` para evitar modificar directamente el código principal.
3. Desarrollo:
    - Cada vez que uno de los desarrolladores comience a trabajar, hará un `svn update` para asegurarse de que trabaja con la versión más actual del código.
    - Cuando termine una tarea, hará un `svn add` para agregar los nuevos archivos creados y luego un `svn ci` para hacer commit de los cambios al repositorio central.
4. Integración de cambios:
    - Antes de fusionar las ramas al repositorio principal, se deberá hacer una revisión de código para evitar errores.
    - Se realizará un `svn merge` para integrar los cambios de la rama al código principal.
5. Finalización:
    - Una vez la tarea esté completa y el código fusionado con la rama principal, se puede eliminar la rama con `svn delete`.

### Actividad 2, Control de versiones y modelo iterativo

En el caso de un proyecto con un modelo iterativo e incremental, el equipo de desarrolladores puede organizar el repositorio de la siguiente manera:

Estructura del repositorio:
1. Directorio principal:

    -`trunk/` → La versión más reciente del código fuente, que incluye las funcionalidades completas.
    -`branches/` → Contendrá las ramas para cada fase del proyecto, como iteraciones o nuevas funcionalidades.
    -`tags/` → Contendrá las etiquetas de cada versión importante o release del proyecto (por ejemplo, `v1.0`, `v1.1`).
2. Organización por iteraciones:

    -`branches/iteracion1/` → Contendrá el código específico para la primera iteración.
    -`branches/iteracion2/` → Contendrá el código específico para la segunda iteración.
Y así sucesivamente para las otras iteraciones y nuevas versiones del proyecto.
Proceso de trabajo:

Cuando se empiece a trabajar en una nueva iteración, se crearía una nueva rama dentro de `branches/` para desarrollar las funcionalidades de la iteración.
Cuando una iteración esté completa, se deberá hacer un `svn merge` para integrar los cambios de la rama a `trunk/`, y luego etiquetar la versión con `svn tag`.

### Actividad 3, Diferencias entre RCS y Subversion (SVN)
Diferencias generales entre RCS y Subversion:
1. RCS es un sistema de control de versiones para archivos individuales. 
2. Subversion (SVN) es un sistema de control de versiones centralizado que permite gestionar todo un proyecto (con múltiples archivos y directorios) de manera centralizada. 
 
#### Comandos en RCS y SVN:
##### RCS:

- co: Comando que se utiliza para hacer un "checkout" (obtener) un archivo del repositorio.
- ci: Comando para hacer un "commit" (guardar) de los cambios de un archivo al repositorio.

##### SVN:

- svn co: Comando para hacer un "checkout" de un repositorio completo (directorio o proyecto) desde el repositorio centralizado.
- svn ci: Comando para hacer un "commit" de los cambios realizados en el código al repositorio centralizado.
- svn st: Muestra el estado actual del repositorio local, mostrando los archivos modificados, añadidos o eliminados.
- svn add: Añade nuevos archivos al repositorio.
- svn up: Actualiza el repositorio local con las últimas modificaciones del repositorio central.

La diferencia entre el los co, ci de rcs y subversion es que rcs trata los ficheros de manera individual a diferencia de subversion que gestiona un proyecto entero.

## Diferencias entre los SCV centralizados y SCV locales.
Los SCV locales se guardan en local y solo son accesibles desde el ordenador desde el cual se encuentra el fichero o el proyecto ,en cambio los SCV centralizados guardan los archivos en un servidor centralizado, esto quiere decir que, hay la posibilidad de que trabajen varios programadores sobre el mismo proyecto. Cuando se quiera trabajar sobre el prouyecto los desarrolladores descargaran una copia del proyecto, la modificaran y luego la volveran a subir al servidor central. 

# Git
- Para inicializar un repositorio utilizamos `git init`.
- Comprobamos el estado del repositorio con `git status`.
- Añadimos el archivo al area de preparacion con `git add 1.txt`.(Previamente creado con `touch 1.txt`)

![imagen](https://cdn.discordapp.com/attachments/1317881904997072948/1317898922156625951/image.png?ex=67605c84&is=675f0b04&hm=0990dec1063fab2c7739c9e5184e589962523e8cf543d8377871ee8658eba54b&)

- Hacemos el primer commit con `git commit -m "Primer comit"`.
- Creamos 1 archivo temporal , el cual no queremos que git siga su rastro. (`touch ignorar.tmp`)
- Creamos el archivo `.gitignore` y lo editamos con lo siguiente:
```
# Ignorar ficheros por su nombre
ignorar.tmp
```
![imagen](https://cdn.discordapp.com/attachments/1317881904997072948/1317901045950713877/image.png?ex=67605e7e&is=675f0cfe&hm=05324a26ad46d5976cd7cc3aa281b2863a910fa61139b57301c0da6340dac9e2&)

- Modificamos el archivo 1.txt, escribiendo cualquier cosa, y hacemos el segundo commit con `git commit -a -m "Segundo commit con opcion -a"`. (La opción -a nos ahorra tener que escribir el comando `git add 1.txt` otra vez. Hay que tener en cuenta que la -a no agrega archivos nuevos. )

![imagen](https://cdn.discordapp.com/attachments/1317881904997072948/1317901559954149428/image.png?ex=67605ef9&is=675f0d79&hm=81b97ea3a5d283997da41e2e6214433877b4617e2dc0d26afc1442a37ad27839&)

- Por ultimo mostramos el resultado de `git log` y `git log --oneline`

![imagen](https://cdn.discordapp.com/attachments/1317881904997072948/1317902432662982736/image.png?ex=67605fc9&is=675f0e49&hm=ea7b420afe882030f3e259f6d7358b0bf0babd8ab3f9ee71c5e410864c16fac5&)

![imagen](https://cdn.discordapp.com/attachments/1317881904997072948/1317902663471599706/image.png?ex=67606000&is=675f0e80&hm=3cbc888a8a24eb4c6f09d4da8a157a450640adf3db53daaf83c0ed2400a96186&)