//Spinning the containers 
docker-compose up -d

docker-compose exec web composer install
docker-compose exec web cp .env.example .env 
docker-compose exec web php artisan key:generate

DB_CONNECTION=mysql DB_HOST=mysql DB_PORT=3306 DB_DATABASE=laravel_authorisation DB_USERNAME=laravel_user DB_PASSWORD=laravel_password

//running the application 
docker-compose exec web php artisan serve --host=0.0.0.0 --port=8000

//rebuilding a single container
docker build -t laravel_authorisation .

//Running a single container
docker run -p 8000:8000 laravel_authorisation