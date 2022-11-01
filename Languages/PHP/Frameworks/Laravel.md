## Clear all cache
```php
php artisan clear-compiled 
php artisan view:clear
php artisan cache:clear
php artisan config:clear
```
## Generate new key in .env and clear cache
```php
php artisan key:generate
php artisan config:cache
```