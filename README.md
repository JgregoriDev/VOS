# VOS 
Proyecto realizado con la libreria react y framework symfony para backend.

Paso 1: Preparación del entorno de desarrollo

1. Instala PHP y Composer en tu sistema.
2. Asegúrate de tener MariaDB instalado y configurado en tu entorno. Crea una base de datos y un usuario con los privilegios necesarios.

Paso 2: Creación del proyecto Symfony

1. Abre una terminal y navega hasta la ubicación donde deseas crear tu proyecto Symfony.
2. Ejecuta el siguiente comando para crear un nuevo proyecto Symfony:

```
composer create-project symfony/website-skeleton myproject
```

3. Navega al directorio del proyecto:

```
cd myproject
```

Paso 3: Configuración de la conexión a la base de datos

1. Abre el archivo `.env` en el directorio raíz del proyecto y configura los parámetros de conexión a la base de datos:

```
DATABASE_URL=mysql://usuario:contraseña@localhost:puerto/nombre_de_la_base_de_datos
```

Reemplaza `usuario`, `contraseña`, `localhost`, `puerto` y `nombre_de_la_base_de_datos` con tus propios valores.

Paso 4: Creación de entidades y migraciones

1. Crea tus entidades de Doctrine en el directorio `src/Entity`. Puedes usar la herramienta `make:entity` de Symfony para generar las clases de entidades automáticamente:

```bash
php bin/console make:entity
```

2. Genera las migraciones de la base de datos:

```bash
php bin/console make:migration
```

3. Ejecuta las migraciones para crear las tablas en la base de datos:

```bash
php bin/console doctrine:migrations:migrate
```

Paso 5: Desarrollo de la aplicación

1. Desarrolla tu aplicación Symfony según tus necesidades, creando controladores, rutas y vistas en el directorio `src/Controller`, `config/routes.yaml` y `templates/` respectivamente.

Paso 6: Despliegue de la aplicación

1. Configura el servidor web (por ejemplo, Apache o Nginx) para que apunte al directorio `public/` de tu proyecto Symfony.
2. Asegúrate de que el servidor web tenga los permisos adecuados para acceder a los archivos y directorios necesarios.

Paso 7: Prueba de la aplicación

1. Abre un navegador y visita la URL de tu aplicación Symfony.
2. Verifica que la aplicación funcione correctamente y que pueda acceder y utilizar la base de datos MariaDB según sea necesario.

¡Felicidades! Ahora has desplegado con éxito tu aplicación Symfony utilizando MariaDB como base de datos. Recuerda que este tutorial solo cubre los pasos básicos para configurar y desplegar la aplicación. Puedes expandir y personalizar aún más tu aplicación Symfony según tus necesidades específicas.
