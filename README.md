# alpine-nginx-phpfpm-mysql-docker-skeleton

Replace everything in code directory with your code.

Note: **Nginx points to code/public directory.**

For Laravel appliations:
Copy everything into code folder and do laravel stuff. `artisan` commands should be run on `phpfpm` contianer.
For example: 
- To composer install: `docker exec -it phpfpm composer install`
- To generate app key: `docker exec -it phpfpm php artisan key:generate`



Tested on a WSL2 setup.