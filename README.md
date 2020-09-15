# SIOC CR
Sistema Integrado de Operaciones Comerciales (SIOC).

Calzados Rosita (CR).

#* Configuración de la aplicación. *#

### Pasos Iniciales. ###

#Creando proyecto [Consola]:

composer create-project laravel/laravel sioc --prefer-dist v7.x
composer require laravel/ui:^2.4
php artisan ui vue
php artisan ui vue --auth
composer require laravel-frontend-presets/argon
php artisan ui argon
composer dump-autoload
php artisan migrate --seed [Configurar parametros de base de datos antes]

#Instalar Node.js para que funcione el npm
npm install && npm run dev [Solo si es requerido]

npm run watch

#Configurar Base de Datos [Dev Only].

[.env] 

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=sioc_cr
DB_USERNAME=root
DB_PASSWORD=root!

#Migrar tablas de usuarios.

php artisan migrate
php artisan migrate:rollback


#Credenciales de la plantilla.
admin@argon.com
secret

#Inicializar proyecto en git/github.
git init
git status

---
/vendor/
node_modules/
npm-debug.log
yarn-error.log

# Laravel 4 specific
bootstrap/compiled.php
app/storage/

# Laravel 5 & Lumen specific
public/storage
public/hot

# Laravel 5 & Lumen specific with changed public path
public_html/storage
public_html/hot

storage/*.key
.env
Homestead.yaml
Homestead.json
/.vagrant
.phpunit.result.cache