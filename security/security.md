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
The file is located at the root of WordPress installation folder. If someone navigates to `example.com/readme.html`, a readme will appear, showing that you're using WordPress.

</br>

## Change `wp-admin` URL
The `example.com/wp-admin` URL can be found easily. Change it to something else.

</br>

## Change `wp-content` URL
By looking at the src of media (like an image) on your website, someone can easily see that you're using WordPress. You can change it:
1. Rename the folder
2. Add this to `wp-config.php`:
```php
define('WP_CONTENT_FOLDERNAME', 'new-folder-name');            //Rename wp-content folder
define('WP_CONTENT_DIR', ABSPATH . WP_CONTENT_FOLDERNAME);     //Define new directory path
define('WP_SITEURL', 'http://' . $_SERVER['HTTP_HOST'] . '/'); //Define new directory URL
define('WP_CONTENT_URL', WP_SITEURL . WP_CONTENT_FOLDERNAME);
```