## Disabling Admin File Edit
Add this to `wp-config.php` to disable file editing from admin panel. If someone gains access to your WordPress dashboard, they won't be able to touch your theme and function codes.
```php
define('DISALLOW_FILE_EDIT', true)
```

## Hiding WP Version
```php
function hide_wp_version() {return '';}
add_filter('the_generator', 'hide_wp_vesion');
```
