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

- php artisan migrate


  protected $fillable = [
        'name', 'detail'
    ];


- 1) Login: Verb:GET, URL:http://localhost:8000/oauth/token

- 2) Register: Verb:GET, URL:http://localhost:8000/api/register

- 3) List: Verb:GET, URL:http://localhost:8000/api/products

- 4) Create: Verb:POST, URL:http://localhost:8000/api/products

- 5) Show: Verb:GET, URL:http://localhost:8000/api/products/{id}

- 6) Update: Verb:PUT, URL:http://localhost:8000/api/products/{id}

- 7) Delete: Verb:DELETE, URL:http://localhost:8000/api/products/{id} 
