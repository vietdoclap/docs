```
cd /any/path
git clone https://github.com/laravel/laravel.git anyname
cd anyname
composer install
chown -R www-data:www-data anyname
chmod -R 755 anyname
chmod -R 777 anyname/storage
cp .env.example .env
php artisan key:generate
```
**If Apache, to check it's running with which user**
```
ps aux | egrep '(apache|httpd)'
root      1439  0.0  1.1 432212 40248 ?        Ss   14:26   0:00 /usr/sbin/apache2 -k start
www-data  7564  0.0  0.3 432244 12536 ?        S    14:31   0:00 /usr/sbin/apache2 -k start
www-data  7568  0.0  0.3 432244 12536 ?        S    14:31   0:00 /usr/sbin/apache2 -k start
......
```
