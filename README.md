<<<<<<< HEAD
<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

You may also try the [Laravel Bootcamp](https://bootcamp.laravel.com), where you will be guided through building a modern Laravel application from scratch.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the [Laravel Partners program](https://partners.laravel.com).

### Premium Partners

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[WebReinvent](https://webreinvent.com/)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel/)**
- **[Cyber-Duck](https://cyber-duck.co.uk)**
- **[DevSquad](https://devsquad.com/hire-laravel-developers)**
- **[Jump24](https://jump24.co.uk)**
- **[Redberry](https://redberry.international/laravel/)**
- **[Active Logic](https://activelogic.com)**
- **[byte5](https://byte5.de)**
- **[OP.GG](https://op.gg)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
=======
# laravel-render-template

Do you want to host your Laravel application for FREE and stress free? This guide will take you step by step until your application is hosted on render.com. 

Now, let's get started.

## 1. Set up an account on render.com

You need to [click to sign up](https://dashboard.render.com/login) on Render. It is preferable to sign up with GitHub since you will be using GitHub in the hosting process.

## 2. Force Laravel to accept only https

To force Laravel to allow https by default, make sure you `App/Provider/AppServiceProvider.php` contains the line and block of code below:

```php
public function boot()
    {
        if (env('APP_ENV') == 'production') {
            $this->app['request']->server->set('HTTPS', true);
        }
    }
```

## 3. Create a remote repository with laravel-render-template.

Here, you will use `Laravel-render-template`. So [click to create](https://github.com/codingnninja/Laravel-render-template-host) a remote repo.

![Laravel render template](https://res.cloudinary.com/nyscapp/image/upload/v1686174427/create_laravel-render_template_hpcqts.png)

You need to click on `use this template` and then `create a new repository`. Fill your repository name and you're done.

## 4. Link local and remote repository.

It is time to merge the local and remote repo and push everything to the remote repo. In this case, you need to choose the option that fit your need.

### 4.1 Using a new Laravel project.

Do you still remember the remote repository you created? Well, you will know what to do about it soon. 

Run the following commands line by line:

```sh
git init
git add .
git commit -m "first commit"
git branch -M main
```

![Github url](https://res.cloudinary.com/nyscapp/image/upload/v1686174426/laravel_render_repo_url_sztour.png)

Yeah, it is time to use the url of the repository you created and you can copy it like in the image above. Use it as a replacement for the `url` in the first command below:

```sh
git remote add origin https://github.com/OWNER/REPOSITORY.git
git pull && git push -u origin main
```
### 4.2 Using an existing project with no remote repo.

If you're working on an existing project you want to host, you need the commands below:

```sh
git remote add origin https://github.com/OWNER/REPOSITORY.git
git branch -M main
git pull && git push -u origin main
```
You need to replace the `url` above with the one you copied from your remote repository.

### 4.3 Using an existing project that is already connected to a remote repo.

To do this, you need to reset the remote `url` in your local repository by running the command below:

```sh
git remote set-url origin https://github.com/OWNER/REPOSITORY.git
git remote -v
git add .
git commit -m "first commit"
git pull && git push
```

## 5. Setting up host web service on render
[Click to create](https://dashboard.render.com/select-repo?type=web) a new web service on Render. Then you will be prompted on what to do next. You see Github and Gitlab logos, and `connect account` by the right-hand side of your screen.

Click `connect account` under the Github logo to link your Github account. Choose the repository you want to host after setting up the web service. The image below gives you an insight.

![Render web service section](https://res.cloudinary.com/nyscapp/image/upload/v1686211207/render_create_webserive_w4lh78.png)
## 6. Setting up Enviroment variables

> Make sure your Laravel application is already working.

Here, we will add `environment` variables to the render web service you created the other time. Navigate to the `dashboard` and you will see all the services you have created just like in the image below:

![Dashboard of a render account](https://res.cloudinary.com/nyscapp/image/upload/v1686211207/dashboard_seriveces_cclxzh.png)

Then, click on the web service you want to host on and navigate to `environment`. You should see a view that looks like below:

![Render enviroment section](https://res.cloudinary.com/nyscapp/image/upload/v1686211206/laravel_render_environment_variable_chirww.png)

Now, add all the `environment` variables your application depends on one by one. Let's start with `APP_KEY`.

### Generate application key.

Run the code below in the root directory of your Laravel project and copy its output.

```sh
php artisan key:generate --show
```

Add `APP_KEY` as the key and the generated string as its value.
## 7. Setup a database (PostgreSQL & MySQL)

To use MySQL on render, you need to be a paid user so we're using PostgreSQL in this write up. [Create](https://dashboard.render.com/new/database) PostgreSQL database service on render.

![Create new PostgreSQL](https://res.cloudinary.com/nyscapp/image/upload/v1686174426/Laravel_render_postgresql_h5ynsn.png)

Make sure you enter your preferred `name`, `database name`, `user name` and `region`. The rest are optional. So look for `create database` button at the bottom of the page to complete the setup.

Remenber, you can use an external MySQL or ProgreSQL services. You need to follow similar process to set it up.

Note: Make sure the name of your database include something like `db` to differentiate the services on your dashboard but that is up to you.

### Adding database environment variables.

When you finished setting up PostreSQL above, you should have copied `Hostname`, `Port`, `Database`, `Username`, `Password` because you need to add them to the `enviroment` as variables.

![Dashboard of a render account](https://res.cloudinary.com/nyscapp/image/upload/v1686211207/dashboard_seriveces_cclxzh.png)

If you forgot to copy them, you can go back to your dashboard and select your database to copy the information.

![Database connection information](https://res.cloudinary.com/nyscapp/image/upload/v1686212167/database_render_info_hclqgy.png)


|  Key     | Value   |
| -------- | ------- |
| DB_CONNECTION| pgsql |
| Port     | 5432    |
| Hostname | your hostname|
| Database | your dbname|
| Username | your username|
| Password | your password|

The keys and values above show how to add `environment` variables on render.com and the image below also gives some insight.

![Render enviroment section](https://res.cloudinary.com/nyscapp/image/upload/v1686211206/laravel_render_environment_variable_chirww.png)

Now, your application should be working correctly. And don't forget, it is important to keep this your application repository private for security and other reasons.

## Content of Laravel-render-template

It contains the following files and folders:

1. `Dockerfile` contains the information to setup our a serve environment. 
2. `scripts/00-laravel-deploy.sh` contains all necessary information to install Laravel and its dependencies. Below is its content:

```sh
#!/usr/bin/env bash
echo "Running composer"
composer install --no-dev --working-dir=/var/www/html

echo "Caching config..."
php artisan config:cache

echo "Caching routes..."
php artisan route:cache

echo "Running migrations..."
php artisan migrate --force 
```

We add the above commands because they're the default to install Laravel, dependencies, and run its operations. If you run a certain command after installing a package before it works on your machine, you also need to run the same here.

For example, Laravel-cloudinary package requires it users to publish it to work on their machine. So, if you use Laravel-cloudinary, you also need the command for the serve too. Then, you need to add the command below to the above commands:

```sh
echo "Publishing cloudinary provider..."
php artisan vendor:publish --provider="CloudinaryLabs\CloudinaryLaravel\CloudinaryServiceProvider" --tag="cloudinary-laravel-config"
```

3. `conf/nginx-site.conf` contains nginx (server) configuration.
4. `.dockerignore` contains contains the files you don't want to ship with Docker.
## Troubleshooting

> 1. Always check the logs on the server.

> 2. Sometimes, you might be running packages that need update which may affect the application to work properly. So, make it an habit to run `composer update` once in a while.

> 3. If your database can't connect despite adding all necessary details correctly, then you can hardcode the database connection information into your laravel project.

Navigate to `config/database.php` to change your default database connection to pgsql.

```sh
'default' => env('DB_CONNECTION', 'pgsql')
```

And add database connection details below:

```php
'pgsql' => [
            'driver' => 'pgsql',
            'url' => env('DATABASE_URL'),
            'host' => env('DB_HOST', 'Hostname'),
            'port' => env('DB_PORT', '5432'),
            'database' => env('DB_DATABASE', 'dbname'),
            'username' => env('DB_USERNAME', 'username'),
            'password' => env('DB_PASSWORD', '********'),
            'charset' => 'utf8',
            'prefix' => '',
            'prefix_indexes' => true,
            'schema' => 'public',
            'sslmode' => 'prefer',
        ]
```

> 4. Click to visit [render docs for Laravel]()
## Need help?

Chat me up on Twitter via [Ayobami Ogundiran](https://twitter.com/codingnninja)



>>>>>>> c91ef8bf3fdd4d668663e59cadd3def17e06f99f
