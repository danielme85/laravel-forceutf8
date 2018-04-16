# laravel-forceutf8
Simple Laravel 5 service class for neitanod's forceutf8: https://github.com/neitanod/forceutf8

### Install
Add to composer.json
 ```
 "require": {
         "danielme85/laravel-forceutf8": "dev-master",
         ....
 }
 ```
 
<b>If you use Laravel 5.5+ you could skip the next step as Composer/Laravel Auto-discovery has been enabled for this package.</b>



#### Laravel 5.x
 Add to your config/app.php under Service Providers
            
 ```
 //Service Provider
 danielme85\ForceUTF8\ForceUTF8ServiceProvider::class,
 //Facade
 'Encoding'  => danielme85\ForceUTF8\Encoding::class,
 
 ```
 
#### Lumen 5.x
 Add to your boostrap/app.php file
 ```
 $app->register(danielme85\ForceUTF8\ForceUTF8ServiceProvider::class);
 ...
 $app->configure('app'); 
 ...
 class_alias('danielme85\ForceUTF8\Encoding', 'Encoding');
 $app->withFacades();
 ```
 
### Usage
 ```
 use danielme85\ForceUTF8\Encoding;
 ...
 $newstring = Encoding::toUTF8($string);
 ```
Chekout neitanod's repo for more information on how to use the Encoding class:
https://github.com/neitanod/forceutf8
