### Run modes

To just run index.php by PHP 7.4:
 
     docker run -it --rm -v "$PWD":/app -w /app php:7.4-cli php index.php
 
Use Composer:

    php composer.phar ...
    
... or if you haven't ```php``` on you host system: 

    docker run -it --rm -v "$PWD":/app -w /app php:7.4-cli php composer.phar ...

### Helpers

#### Simple autoloader

If you don't use Composer and it's autoloader:

    /**
    
    Directory structure:
    
    ./Space/Foo.php
    ./Space2/Inner/Bar.php
    
    */
    
    <?php
    
    require 'autoload.php';
    
    use Space\Foo;
    use Space2\Inner\Bar;
    
    $a = new Foo();
    $b = new Bar();
