# laravel-sub-domain-cpanel
this describes how to configure subdomain for laravel project.

Using `example.com`
if you own `example.com` and want to create `subdoamin.example.com` and handle it with laravel.
then follow these steps.

1. Create sub domain in cpanel and point its directory to laravel project directory.
2. now in your `routes/web.php` add this snippet.

```php

/*subdoamin*/
Route::domain('subdoamin.example.com')->group(function () {
    //mobile routes
    Route::get('/', function(){
        dd("Reserved For subdoamin.example.com Site") ;
    });
}
);

```

Now visit 

```php
subdoamin.example.com
```

and you will get
 
```php
Reserved For subdoamin.example.com Site
```
