# laravel-7-2

# Step 1 : Install Laravel 5.7
composer create-project --prefer-dist laravel/laravel app

# Step 2: Update Database Configuration
- DB_CONNECTION=mysql
- DB_HOST=127.0.0.1
- DB_PORT=3306
- DB_DATABASE=here your database name(blog)
- DB_USERNAME=here database username(root)
- DB_PASSWORD=here database password(root)

# Step 3: Create Table
php artisan make:migration create_products_table --create=products

--- 

# database/migrations

     - $table->string('name');
     - $table->text('detail');
---
# run migraciones
- php artisan migrate

# Step 4: Create Resource Route

# routes/web.php
Route::resource('products','ProductController');


