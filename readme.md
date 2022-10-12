Se instala Node.Js desde nodejs.org

De las siguientes dos maneras, sabemos la versión de Node y de npm(Node Package Manager)
node -v
npm -v

Al empezar un repositorio, ejecutamos los siguientes comandos:

git init => Nos va a permitir enlazar nuestro repositorio a algún servicion de nube de código.

npm init => inicializa nuestro proyecto y nos abre un configurador que debemos ir cumplimentando:

    “package name”: “npm-init” —> Podemos ponerle un nombre sin embargo toma por defecto el de la carpeta.

    “version”: “1.0.0” —> Podemos cambiar la versión segun el caso, dependiendo si se efectua un cambio mayor o uno menor

    “description”:"" —> Podemos hacer una breve descripcion del proyecto.

    “entry point”: “(index.js)” —> Punto de entrada del proyecto.

    “test command”: —> Podemos incluir los comandos para validar nuestro codigo con las pruebas de integración o las unitarias.

    “git repository”: —> Podemos incluir el repositorio para mantenerlo en la nube

    “keywords”: [“javascript”, “angular”, “node”] —> Que va a utilizar nuestro proyecto.

    “author”: "Alexa Pulido<pulidoaleXXXXXXX> —> Persona que crea el proyecto (Nombre, apellido e email)

    “license”: “MIT” —> Licencias, la mas utilizada es MIT, permite distribuir nuestro codigo.

npm init -y => Esto nos crea el archivo package.json con una configuración por defecto y posteriormente podemos modificar lo que necesitemos modificar.

Las dependencias son importantes ya que con estas podemos reutilizar codigo de otros desarroladores de una forma rapida y sencilla, para instalar dependecias podemos hacerlo a través de npm, yarn, entre otros.

¿Como Instalar una Dependecia?

Para Instalar una dependencia con npm iniciamos con la siguiente forma.

npm install <nombre de la dependecia>

Dependecias de Desarrollo

Al agregar --save-dev despues del nombre de la dependendecia estamos especificando que solo vamos a utillizar la dependecia en el entorno de desarrollo y no se llevará al entorno de producción. Asi mismo podemos utilizar el flag -D despues del nombre de la dependecia.

npm install <nombre de la dependecia> --save-dev
npm install <nombre de la dependecia> -D

Dependencias de Producción

Al no agregar nada, solo el npm install o al agregar —-save despues del nombre de la dependecia estamos especificando que es una dependecia que utilizara tanto en desarrollo como en producción.

npm install <nombre de la dependecia>
npm install <nombre de la dependecia> -S
npm install <nombre de la dependecia> --save

Dependencias Globales

Estos no están ligados directamente a nuestro proyecto, sino a nuestro sistema operativo.
Al agregar —g antes del nombre de la dependecia, estamos especificando que la dependecia que estamos instalando esta en el scope global

npm install -g <nombre del paquete>

Con npm list => puedo saber que paquetes tengo instalado en mi repositorio. Aca veo la lista de paquetes que están agregados en el proyecto.

Con npm list -g => Acá veo que paquetes tengo instalados de forma global.


Las dependencias de desarrollo son aquellos paquetes que necesitamos en un proyecto mientras estamos desarrollándolo, pero una vez tenemos el código generado del proyecto, no vuelven a hacer falta. Los paquetes instalados con el flag --save-dev o -D se instalan en esta modalidad, guardándolos en la sección devDependences del fichero package.json.
.
Por otro lado, las dependencias de producción son aquellos paquetes que necesitamos tener en la web final generada, como librerías Javascript necesarias para su funcionamiento o paquetes similares. Los paquetes instalados con el flag --save-prod, -P o directamente sin ningún flag se instalan en esta modalidad, guardándolos en la sección dependences del fichero package.json.

    1) `npm install package-name -o` → Instalar de forma opcional una dependencia.

    2) Se pueden generar conflictos cuando se tienen paquetes que usan la misma dependencia pero en versiones diferentes. Para evitar esto se puede simular una instalación con `npm install package-name —dry-run`. Con esto se simula la instalación pero sin agregar ningún paquete, de manera que se verifique si se puede realizar de manera segura una instalación de dicho paquete; si no hay ningún conflicto se procede a instalar de la manera convencional.
    3) `npm install package-name@0.15.0` → Instalar la versión especifica de un paquete. Si luego se quiere instalar la versión más reciente se usa `npm install package-name@latest`.
    4) `npm install` → Instala las dependencias que estén dentro de un package.json.
    5) `npm list`
