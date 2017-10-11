Self-upgrade laravel cli
composer global require "laravel/installer"

Self-upgrade composer
composer selfupdate/self-update

Install fresh Laravel framework
https://tecadmin.net/install-laravel-framework-on-ubuntu/#
cd /var/www
git clone https://github.com/laravel/laravel.git
cd /var/www/laravel
composer install
chown -R www-data.www-data /var/www/laravel
chmod -R 755 /var/www/laravel
chmod -R 777 /var/www/laravel/app/storage
cp .env.example .env
php artisan key:generate
