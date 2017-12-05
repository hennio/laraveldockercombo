# Laravel docker combo

Development is done on the Laravel-framework combined with Docker. All data is stored locally on your device! 

## Official Documentation

Documentation will follow below.

### Installation
Make sure you have installed Docker!

After pull execute code below in working directory: 

    docker run --rm -v $(pwd):/app composer/composer install

Or in Windows:

    docker run --rm -v "c:/fullPath/laraveldockercombo":/app composer/composer install

Start the application:

    docker-compose up -d

**_The first run wil take a few minutes_**

End the application:

    docker-compose down


We first need to copy the .env.example file into our own .env file. This file will not be checked into version control & we’ll have separate ones for development & production. For now, just copy .env.example -> .env

After that:

```
docker-compose exec app php artisan key:generate #when using windows you might need to use winpty in front of this phrase
docker-compose exec app php artisan optimize
```



Visit the combo with your browser:

	0.0.0.0:8080

or 

    localhost:8080



### Integrated tools
To be done

## Thanks

Dockerintegration done with this [tutorial](https://medium.com/@shakyShane/laravel-docker-part-1-setup-for-development-e3daaefaf3c) by Shaky Shane.

## License

The CCT Workspace is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).
