A port of Laravel 3's Asset class. Made to work with Laravel 4.1.


## Usage

### Composer Side

add `"teepluss/asset": "dev-master"` to the `require` section of your `composer.json` so that it should look something the code below.

```composer
...
...
...
"require": {
	...
	...
	...
	"teepluss/asset": "dev-master"
},
...
...
...
```

add the `https://github.com/Ardakilic/laravel4-asset` vcs source to your `composer.json` in `repositories` section (if there is no repositories section, create it first). It should look something like this:

```{
	"name": "laravel/laravel",
	"description": "The Laravel Framework.",
	...
	...
	...
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/Ardakilic/laravel4-asset"
        }
    ],
	"require": {
		"laravel/framework": "4.1.*",
		...
		...
	},
...
...
...
```

### Laravel Side

add the following code to the `providers` section of the `app/config/app.php` file

```php
'Teepluss\Asset\AssetServiceProvider',
```

so that it'll look something like the following

```php
'providers' => array(

	...
	...
	...
	'Teepluss\Asset\AssetServiceProvider',

),
```

and add the following code to the `aliases` section of the `app/config/app.php` file

```php
'Asset' => 'Teepluss\Asset\Facades\Asset'
```

so that it'll look something like the following

```php
'aliases' => array(

	...
	...
	...
	'Asset'       => 'Teepluss\Asset\Facades\Asset',

),
```
