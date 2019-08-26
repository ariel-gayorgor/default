# Always include the .env.testing for this is the one responsible for testing connection
# Steps
# 1.) php artisan config:cache
# 2.) php aritsan migrate --env=testing
# 3.) php artisan db:seed --env=testing
# 4.) do the phpunit testing following the syntax

# To execute all testscripts regardless if unit or feature ./vendor/bin/phpunit 
# To execute per file ./vendor/bin/phpunit tests/Unit/filename.php or tests/Feature/filename.php
# To execute per file per method name ./vendor/bin/phpunit method name tests/Unit/filename.php or tests/Feature/filename.php
# To execute per method name ./vendor/bin/phpunit method name


Reminder:
#
If .env.testing is not include you can alway copy your existing .env on you local and have it named .env.testing
#
See .env.testing configuration "#" is not included else it won't run

DB_CONNECTION=mysql_test

DB_TEST_HOST=127.0.0.1

DB_TEST_PORT=3306

DB_TEST_DATABASE=testing

DB_TEST_USERNAME=root

DB_TEST_PASSWORD=

#
Make sure that you configuration/database has the following setup "#" is not included else it won't run. 
#
You may follow the configuration on you locals

#'mysql_test' => [
#    'driver' => 'mysql',
#    'url' => env('DATABASE_TETS_URL'),
#    'host' => env('DB_TEST_HOST', '127.0.0.1'),
#    'port' => env('DB_TEST_PORT', '3306'),
#    'database' => env('DB_TEST_DATABASE', 'testing'),
#    'username' => env('DB_TEST_USERNAME', 'root'),
#    'password' => env('DB_TEST_PASSWORD', ''),
#    'unix_socket' => env('DB_TEST_SOCKET', ''),
#    'charset' => 'utf8mb4',
#    'collation' => 'utf8mb4_unicode_ci',
#    'prefix' => '',
#    'prefix_indexes' => true,
#    'strict' => true,
#    'engine' => null,
#    'options' => extension_loaded('pdo_mysql') ? array_filter([
#        PDO::MYSQL_ATTR_SSL_CA => env('MYSQL_ATTR_SSL_CA'),
#    ]) : [],],
