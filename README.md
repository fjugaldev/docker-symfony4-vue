
# Docker-Symfony4-VueJS
Symfony 4 skeleton con VueJS, Vuex, Vue-router y Webpack.
Todo configurado dentro de un entorno Docker (NGINX + PHP-FM + MySQL + Redis)

## ¿Qué incluye?
-Symfony 4.2 skeleton

-Twig, Annotations, Webserver y Maker bundle

-Encore webpack con VueLoader y SassLoader configurado

-Vue, Vuex y Vue-Router

-Axios esta prototipado como variable $http

## Instalación

Clona este repositorio:

```sh
$ git clone https://github.com/fjugaldev/docker-symfony4-vue.git
```

El proyecto de symfony esta dentro de la carpeta "Symfony".

```sh
$ cd docker-symfony4-vue # ó la carpeta donde hayas clonado el repositorio
```
```sh
$ cd symfony
```
Instalar dependencias de composer y node

```sh
$ composer install
$ yarn install #recomendado
ó
$ npm install
```

Compilar archivos js y css

```sh
$ ./node_modules/.bin/encore dev 
```

Ejecutar Servidor Web de Symfony

```sh
$ php bin/console server:run
```
Iniciará un servidor accesible en http://localhost:8080

## Vue development

Los archivos de Vue estan ubicados en la carpeta /assets/js. Modifica estos archivos como si se trata de un proyecto normal de VueJS.

Sugiero utilizar hot-reload encore server. Cuando un archivo es actualizado, webpack será lanzado automáticamente. Inícialo con este comando:

```sh
$ ./node_modules/.bin/encore dev --watch
```
Los archivos app.js y app.css serán compilados en la carpeta /public/build.

DefaultController.php contiene solo una ruta raiz que renderiza los archivos necesarios.

SassLoader esta activado, por lo que todos los cambios en /assets/js/app.scss serán compilados también.

Axios esta prototipado como $http. Este servicio estará disponible en toda la app VueJS.

Vuex y Vue-router están incluidos también. Sientete sibre de añadir tantas rutas como stores desees.
