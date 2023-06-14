
# Documentation for Deploying Laravel and MySQL to Railway

This documentation will guide you through the process of deploying a Laravel application with MySQL to Railway. Railway is a hosting platform that allows you to easily run your Laravel applications.

## Step 1: Get Started with GitHub Project

1. Create a new repository on GitHub.
2. Clone the repository to your local machine.
3. Select the part of the project that you want to deploy to Railway.

## Step 2: Add MySQL to the Project

1. Make sure you have the MySQL service provided by Railway installed.
2. Configure the MySQL connection in the `variables` file of your Laravel project:

   ```
   DB_CONNECTION=mysql
   DB_HOST={mysql_host_address}
   DB_PORT={mysql_port}
   DB_DATABASE={database_name}
   DB_USERNAME={mysql_username}
   DB_PASSWORD={mysql_password}
   ```

## Step 3: Create Environment (Prod, Dev, or Test)

1. Create a new environment configuration in the Railway project.
2. Adjust the environment configuration in the `variables` file of the Laravel project.

## Step 4: Go to Setting Change Branch and Generate Domain

1. Open the Setting menu in Railway.
2. Select the "Change Branch and Generate Domain" option.
3. Choose the branch you want to deploy.
4. Railway will generate a unique URL that you can use to access your application.

## Step 5: Configuration for HTTPS

1. Open the `app/Providers/AppServiceProvider.php` file.
2. Add the following code inside the `boot()` method:

   ```php
   public function boot()
   {
       if ($this->app->environment('production')) {
           URL::forceScheme('https');
       }
   }
   ```

3. Open the `app/Http/Middleware/TrustProxies.php` file.
4. Adjust the contents of the file with the following code:

   ```php
   <?php
   
   namespace App\Http\Middleware;
   
   use Illuminate\Http\Middleware\TrustProxies as Middleware;
   use Illuminate\Http\Request;
   
   class TrustProxies extends Middleware
   {
       protected $proxies = '*';
   
       // ...
   }
   ```

## Step 6: Configure Variables in the Laravel Project

1. Open the `.env` file in the Laravel project.
2. Configure the following variables according to the environment you're deploying to:

   ```
   APP_KEY={manually_generated_in_terminal}
   APP_ENV={environment_location}
   DB_HOST={mysql_variable_value}
   DB_PORT={mysql_variable_value}
   DB_DATABASE={mysql_variable_value}
   DB_USERNAME={mysql_variable_value}
   DB_PASSWORD={mysql_variable_value}

   # Add manual variable
   NIXPACKS_BUILD_CMD=composer install && npm run build && php artisan optimize && php artisan config:cache && php artisan view:cache && php artisan migrate --force
   ```

With these steps, you are now ready to deploy your Laravel application with MySQL to Railway. Make sure to refer to Railway's official documentation for more details on configuration and features provided by the platform.

Happy deploying!
```

Please note that in the code snippet provided, the term `variables` is used instead of `.env` file. This is because Railway may use a different naming convention for environment variables. Please adjust the instructions accordingly based on the specific naming conventions used by Railway.
