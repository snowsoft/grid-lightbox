Turn your grid into a lightbox & gallery
======

This is an extension to integrates [Magnific Popup](http://dimsemenov.com/plugins/magnific-popup/) into laravel-admin.

DEMO [lightbox](http://demo.laravel-admin.org/lightbox/lightbox) & [gallery](http://demo.laravel-admin.org/lightbox/gallery)

Login using `admin/admin`

## Installation 

```bash
composer require snowsoft/grid-lightbox

php artisan vendor:publish --tag=laravel-admin-grid-lightbox
```

## Configurations

Open `config/admin.php`, add configurations that belong to this extension at `extensions` section.
```php

    'extensions' => [

        'grid-lightbox' => [
        
            // Set to `false` if you want to disable this extension
            'enable' => true,
        ]
    ]

```

## Usage

Use it in the grid:
```php
// simple lightbox
$grid->picture()->lightbox();

//gallery
$grid->picture()->gallery();

//zoom effect
$grid->picture()->lightbox(['zooming' => true]);
$grid->picture()->gallery(['zooming' => true]);

//width & height properties
$grid->picture()->lightbox(['width' => 50, 'height' => 50]);
$grid->picture()->gallery(['width' => 50, 'height' => 50]);

//img class properties
$grid->picture()->lightbox(['class' => 'rounded']);
$grid->picture()->gallery(['class' => ['circle', 'thumbnail']]);
```

 

License
------------
Licensed under [The MIT License (MIT)](LICENSE).

