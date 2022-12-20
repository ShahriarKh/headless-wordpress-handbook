## Disable Admin File Edit
Add this to `wp-config.php` to disable file editing from admin panel. If someone gains access to your WordPress dashboard, they won't be able to touch your theme and function codes.
```php
define('DISALLOW_FILE_EDIT', true)
```

</br>  

## Hide WP Version
```php
function hide_wp_version() {return '';}
add_filter('the_generator', 'hide_wp_vesion');
```

</br>

## Delete `readme.html`
The file is located at the root of WordPress. If someone navigates to `example.com/readme.html`, a readme will appear, showing that you're using WordPress.
