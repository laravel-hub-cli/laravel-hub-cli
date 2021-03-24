# Laravel Hub CLI

The Laravel Hub CLI is an un-official tool for scaffolding new Laravel applications. The name **Laravel Hub** is inspired by Docker and Docker Hub where individuals and teams can share their container images.

Whereas in docker you would create your docker image using a `docker-compose` file, in Laravel Hub you would create your Laravel Application using a `laravel-compose` file.

# Compose File API

- [env](#env)
- [name](#name)
- [touch](#touch)
- [mkdir](#mkdir)
- [version](#version)
- [php-packages](#php-packages)
- [php-packages-dev](#php-packages-dev)
- [npm-packages](#npm-packages)
- [npm-packages-dev](#npm-packages)

## `env`

The `env` API allows you update or insert (upsert) keys in the applications `.env` file.

An example is show below:

```yaml
env:
 APP_NAME: "Laravel"
 DB_DATABASE: "laravel"
 NEW_ENV_KEY: "value"
```

## `name`

- Required: True

The `name` key is required, the sluggified version of the name will be used to generate the folder name where the application will be installed.

## `touch`

The `touch` API allows you create files in your application. Any required directories will also be created.

An example is show below:

```yaml
touch:
  - "app/Support/helpers.php"
```

## `mkdir`

The `mkdir` API allows you create directories in your application. Any required parent directories will also be created.

An example is show below:

```yaml
mkdir:
  - "resources/svg"
```

## `version`

The `version` API allows you to declare what version of Laravel you want to install. You can specify any value that composer will accept.

An example is show below:

```yaml
version: "7.x"
```

## `php-packages`

The `php-packages` API allows you require composer packages into your application.

An example is show below:

```yaml
php-packages:
  - laravel/telescope
  - laravel/socialite
```

## `php-packages-dev`

The `php-packages-dev` API allows you require dev only composer packages into your application.

An example is show below:

```yaml
php-packages-dev:
  - brianium/paratest
```

## `npm-packages`

The `npm-packages` API allows you install NPM packages into your application.

An example is show below:

```yaml
npm-packages:
  - "tailwindcss/@latest"
```

## `npm-packages-dev`

The `npm-packages` API allows you install NPM dev packages into your application.

An example is show below:

```yaml
npm-packages-dev:
  - "alpinejs"
```