# Taller Git UAH
Repo dedicado al Taller de Git impartido por Bea Bermudez ([@chuceria](https://github.com/chucheria)) y por Rubén Gómez ([@rgomezbertoli](https://github.com/rgomezbertoli))

## Indice

<ol>
    <li>Qué es control de versiones y Git</li>
    <li>Instalación de Git</li>
    <li>Crea tu primer repositorio en Github</li>
    <li>Clonar un repositorio existente</li>
    <li>Comprobar estado</li>
    <li>Guardar cambios</li>
    <li>Enviar cambios (EJERCICIO)</li>
    <li>Conflictos (EJERCICIO)</li>
    <li>Trabajar con ramas (EJERCICIO)</li>
</ol>

## 1. Qué es control de versiones y Git

Un sistema de control de versiones monitoriza los cambios de un proyecto. Conforme avanza el proyecto cada uno de los cambios que se guardan forman versiones a las que se puede volver en cualquier momento del proyecto. Algunas de las preguntas a las que responde un control de versiones son:

- ¿Qué cambios se han hecho?
- ¿Quién ha hecho esos cambios?
- ¿Cuándo se hicieron los cambios?

Git es un sistema de control de versiones, otros son Subversion, Mercurial, Plastic SCM.

## 2. Instalación de Git

En la guía principal de Git podemos encontrar los pasos correspondientes para realizar la instalación en cualquier sistema:

[Guía de Instalación](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

## 3. Crea tu primer repositorio en Github

Para crear tu primer repositorio primero has de crearte un usuario en la plataforma [Link](https://github.com/join)

Una vez tengamos ese usuario podremos crear tu primer repositorio con una simple configuración en la web y ya estarás listo para darle duro.

Cómo en este taller vamos a trabajar al menos con 2 ordenadores necesitaremos que os junteis al menos por parejas y despues os enseñaremos a añadir a vuestro compañero al repositorio para que podáis trabajar como lo haríais en un equipo.

## 4. Clonar un repositorio existente

Si quieres tener una **copia** de un repositorio de Git, como el que acabas de crear el commando que necesitas es `$ git clone repositorio`. Con este comando se copian todas las versiones de todos los archivos que han sido registrados en Git.

De momento vamos a usar la opción `https` pero si tienes un SSH ya configurado puedes usarlo de esa manera.

## 5. Comprobar Estado

Es importante saber cuales son los cambios que hemos realizado desde la ultima vez que nos sincronizamos con nuestra rama de desarrollo. Para ello tenemos los siguientes comandos:

```bash
$ git status
```
Con este comando podremos saber que archivos han sido modificados desde la última vez que guardamos. Tambien nos da información de que archivos están seleccionados para ser guardados.

```bash 
$ git log 
```
Nos permite ver una lista de cambios y cual fue el último que se envió a nuestro repositorio remoto. Tambien nos permite ver el identificador y la pequeña descripción que escribimos cuando guardamos.

## 6. Guardar cambios

Una vez que tengo mi repositorio en mi _local_ puedo modificar los archivos y una vez que esté satisfecha con los cambios además de guardarlos en mi ordenador tengo que decirle a Git que los registre.

Por ejemplo, si modifico mi archivo _README.md_ y lo guardo, le indico a Git que registre los cambios de la siguiente manera:

```bash
$ git add README.md
```

Después de esto si compruebas el estado de tus archivos podrás ver que ¡ha cambiado algo!

Una vez que hayas añadido todos los archivos cambiados puedes escribir un mensaje descriptivo de los cambios que has hecho, en este caso podríamos escribir:

```bash
$ git commit -m "Actualizar README"
```

El `-m` es para escribir el mensaje directamente, si solo escribimos `git commit` nos abrirá el editor que tengamos por defecto.

Los mensajes son importantes porque registran cambios que luego podemos ver de nuevo en el `git log`, viendo así el historial de cambios sin necesidad de pasar por el código.

## 7. Enviar Cambios

Todo lo que hemos hecho hasta ahora es realizar cambios de forma local, por lo que nuestros compañeros aún no pueden ver los cambios que hemos realizado desde su propio ordenador. Para que puedan verlo necesitamos enviarlos a nuestro repositorio remoto.

```bash
$ git push
```

Con este comando se envian todos los cambios que hemos guardado de forma local para que cualquier compañero que tenga acceso al repositorio pueda verlos y traerselos a su local.

```bash
$ git pull
```
A través de este comando podemos descargarnos esos cambios que se encuentran en el repositorio remoto a nuestro local.

__Importante!__ Antes de enviar nuestros cambios siempre debemos traernos los cambios que estan en nuestro repositorio remoto. Para recordar mejor esto os dejo este gif:

![Pull Before Push](https://media1.tenor.com/images/137473de67ac7a2859d63ca4176b3c64/tenor.gif?itemid=7767237)

Y ahora vamos a practicar todo lo que hemos aprendido con un ejercicio simple.

### Ejercicio

Vamos a realizar los siguientes pasos:

- Creamos un archivo de texto en la carpeta donde hemos clonado nuestro repositorio
- Vamos a comprobar que hay cambios que hay que guardar
- Realizamos un guardado
- Enviamos este guardado a nuestro repositorio remoto
- Nuestr@ compañer@ se descarga ese cambio a su repositorio local
- Ahora nuestr@ compañer@ modificará ese fichero y los subirá los cambios para que nos los descarguemos

## 8. Conflictos

Cuando varias personas trabajan sobre un mismo proyecto es muy común que en algunas ocasiones varias de estas personas modifiquen las mismas lineas dentro de un archivo.

En estos casos, GIT no quiere tomar partido en la decisión de cual es la versión correcta y genera un conflicto para que los responsables se den cuenta de que han tocado las mismas lineas y que deben llegar a un acuerdo y generar una versión en la que todos estén de acuerdo.

En muchas ocasiones, estos conflictos son generados de forma indirecta debido a diferentes criterios de estructura o formateo del código; por lo que es importante que según se abra un proyecto se acuerden estas normas para evitar generar conflictos innecesarios.

### Ejercicio

Vamos a poner en práctica como podemos resolver los conflictos y para ello vamos a usar nuestro maravilloso VSCode, ya que dispone de una herramienta dedicada a ello. Os vamos a hacer una demostración.

![DEMO](https://media3.giphy.com/media/toXKzaJP3WIgM/giphy.gif)

## 9. Trabajar con ramas

Normalmente no trabajamos solos, y a parte podría pasar que trabajasemos sobre un producto que ya está funcionando y en producción. Para no romper ni el producto que funciona ni el desarrollo de nuestros compañeros una buena práctica es trabajar en ramas.

Una rama es una copia del repositorio en el estado del último _commit_ que se separa del desarrollo principal y en el que puedes hacer cambios sin modificar el código principal.

Vamos a ver el ejemplo de este repositorio:

```bash
* 070e618 (HEAD -> master, origin/master, origin/HEAD) Sección de Conflictos
*   cb63aaf merge solve
|\
| * 61fa4b2 Generando Conflicto
* | ab49cdc change emoji
|/
* 5015fd6 ejercicio folder
* aa5f856 Puntos 6 y 7 hechos =)
* da186d9 cambio indice
* eda50f4 Apartado crear repo y listado de indices
* 08b1d82 Update README.md
* 572794f Añadido paso de instalación de entorno
* 560c8ea update readme
* c192d57 Initial commit
```

En el _commit_ `5015fd6` se creó una rama independiente del desarrollo principal, se hicieron dos commits `ab49cdc` y `61fa4b2` y se juntó el desarrollo con la rama principal, por defecto es master.

Los pasos para crear una rama y cambiarse a la rama son muy sencillos:

```bash
$ git branch rama
$ git checkout rama
```

Y si lo quiero hacer todo de una vez puedo usar:

```bash
$ git checkout -b rama
```

Una vez que estoy en la rama puedo modificar archivos, guardar mis cambios y enviar cambios al repositorio remoto de la misma manera que si estuviese en master. Y cuando esté lista para unirlo al código principal puedo hacer un `pull request` desde GitHub.

Los cambios que hago y envío son sobre la rama en la que estoy trabajando y así lo tengo que indicar cuando los envíe:

```bash
$ git push origin rama
```

Se creará la rama en el repositorio remoto si no está creada y se actualizará en otro caso.

### Ejercicio

- Crea una rama nueva
- Modifica algún archivo
- Guarda tus cambios
- Envía tus cambios a la nueva rama

**Bonus**: Bajate los cambios de otra rama que no sea la tuya.

![](https://media3.giphy.com/media/12e5dX36aMp2Ba/giphy.gif)