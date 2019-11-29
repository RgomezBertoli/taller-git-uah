# Taller Git UAH
Repo dedicado al Taller de Git impartido por Bea Bermudez ([@chuceria](https://github.com/chucheria)) y por Rubén Gómez ([@rgomezbertoli](https://github.com/rgomezbertoli))

## Indice

<ol>
    <li>Qué es control de versiones y Git</li>
    <li>Instalación de Git</li>
    <li>Crea tu primer repositorio en Github</li>
    <li>Clonar un repositorio</li>
    <li>Guardar cambios</li>
    <li>Comprobar estado</li>
    <li>Enviar cambios (EJERCICIO)</li>
    <li>Trabajar con ramas (EJERCICIO)</li>
    <li>Conflictos (EJERCICIO)</li>
</ol>

## Qué es control de versiones y Git

Un sistema de control de versiones monitoriza los cambios de un proyecto. Conforme avanza el proyecto cada uno de los cambios que se guardan forman versiones a las que se puede volver en cualquier momento del proyecto. Algunas de las preguntas a las que responde un control de versiones son:

- ¿Qué cambios se han hecho?
- ¿Quién ha hecho esos cambios?
- ¿Cuándo se hicieron los cambios?

Git es un sistema de control de versiones, otros son Subversion, Mercurial, Plastic SCM.

## Instalación de Git

En la guía principal de git podemos encontrar los pasos correspondientes para realizar la instalación en cualquier sistema:

[Guía de Instalación](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

## Crea tu primer repositorio en Github

Para crear tu primer repositorio primero has de crearte un usuario en la plataforma [Link](https://github.com/join)

Una vez tengamos ese usuario podremos crear tu primer repositorio con una simple configuración en la web y ya estarás listo para darle duro.

Cómo en este taller vamos a trabajar al menos con 2 ordenadores necesitaremos que os junteis al menos por parejas y despues os enseñaremos a añadir a vuestro compañero al repositorio para que podáis trabajar como lo haríais en un equipo.

## Comprobar Estado

Es importante saber cuales son los cambios que hemos realizado desde la ultima vez que nos sincronizamos con nuestra rama de desarrollo. Para ello tenemos los siguientes comandos:

```
git status
```
Con este comando podremos saber que archivos han sido modificados desde la última vez que guardamos. Tambien nos da información de que archivos están seleccionados para ser guardados.

```
git log
```
Nos permite ver una lista de cambios y cual fue el último que se envió a nuestro repositorio remoto. Tambien nos permite ver el identificador y la pequeña descripción que escribimos cuando guardamos.

## Enviar Cambios

Todo lo que hemos hecho hasta ahora es realizar cambios de forma local, por lo que nuestros compañeros aún no pueden ver los cambios que hemos realizado desde su propio ordenador. Para que puedan verlo necesitamos enviarlos a nuestro repositorio remoto.

```
git push
```

Con este comando se envian todos los cambios que hemos guardado de forma local para que cualquier compañero que tenga acceso al repositorio pueda verlos y traerselos a su local.

```
git pull
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
