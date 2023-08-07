## Laravel Artisan command line note


### 1. Basic Artisan command
> Install laravel

```bash
composer create laravel/laravel your_project --prefer-dist
```
> Check Laravel version
```bash
php artisan --version
```
> Run Laravel project
```bash
php artisan serve (default port 8000) (1)
php artisan serve --port=83           (2)
php artisan serve --port 83           (3)         
```

### 2. Create controller
> Create  controller basic
```bash
php artisan make:controller YourController
```
> Create resource controller
```bash
php artisan make:controller YourController --resource (1)
php artisan make:controller YourController -r         (2)
```
> Create API controller
```bash:
php artisan make:controller YourController --api
```
### 3. Create Migration table and Model
> Create Migrations table
```bash:
php artisan make:migration create_example_table
```
> Create Model basic
```bash:
php artisan make:model YourModel
```
> Create Model with Migration
```bash:
php artisan make:model YourModel --migration (1)
php artisan make:model YourModel -m          (2)
```
> Create Model with basic controller
```bash:
php artisan make:model YourModel --controller (1)
php artisan make:model YourModel -c           (2)
```
> Create Model with API controller
```bash:
php artisan make:model YourModel --api
```
> Create Model with basic controller and migration
```bash:
php artisan make:model YourModel --controller --migration (1)
php artisan make:model YourModel -c -m                    (2)
php artisan make:model YourModel -cm                      (3)
```
> Create Model with API controller and migration
```bash:
php artisan make:model YourModel --api --migration (1)
php artisan make:model YourModel --api -m          (2)
```
> Create Model with Resource controller
```bash:
php artisan make:model YourModel --resource (1)
php artisan make:model YourModel -r         (2)
```

> Create Model with Resource controller and Migration table
```bash:
php artisan make:model YourModel --all                                  (1)
php artisan make:model YourModel -a                                     (2)
php artisan make:model YourModel --migration --controller --resource    (3)
php artisan make:model YourModel -m -c -r                               (4)
php artisan make:model YourModel -mcr                                   (5)

```
### 4. Migrations actions
> Migrate fresh command is used to drop all the tables from the database and then re-runs all the migration
```bash:
php artisan migrate:fresh
```
> Migrate refresh command is used rollback all the migrations and then re-run all the migrations basically, it is used to re-create the entire database.
```bash:
php artisan migrate:refresh
```
> Migrate rollback is used to rollback the last database migration
```bash:
php artisan migrate:rollback
```

### 5. Route commands

> Check route list
```bash:
php artisan route:list
```
> Filter the route list by URI
```bash:
php artisan route:list --path=items // example
```
> Filter the route list by method
```bash:
php artisan route:list --method=GET // example
php artisan route:list --method=POST // example
```
> Filter the route list by method and URI
```bash:
php artisan route:list --method=GET --path=items // example
php artisan route:list --method=POST --path=posts // example
```
