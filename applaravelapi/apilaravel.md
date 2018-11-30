# Paso 1: Crear Proyecto laravel
- composer create-project --prefer-dist laravel/laravel blog

# Paso 1.1 Agregar 
  ## /opt/lampp/htdocs/repo-laravel/blog12/app/Providers/AppServiceProvider.php
  use Illuminate\Support\Facades\Schema;

    - public function boot()
    - {
        - Schema::defaultStringLength(191);
    - }
  
# Paso 2: Instalar passport
- composer require laravel/passport


# migracion products
php artisan make:migration create_products_table



  - $table->string('name');
  - $table->text('detail');
