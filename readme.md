Comment installer Laravel4
==========================

Etape 1
-------

Laravel utilise Composer pour gérer ses dépendances :
1 - [RSite de Composer](http://getcomposer.org/)

2 - Installer Composer :
* Via l'installateur Windows
* Via le fichier composer.phar :
Ajouter le répertoire où vous avez placé Composer (C:\bin dans cet exemple) et le répertoire de PHP (C:\wamp\bin\php\'votre version php') dans le PATH.
Commandes pour récupérer composer.phar :
	C:\Users\username>cd C:\bin
	C:\bin>php -r "eval('?>'.file_get_contents('https://getcomposer.org/installer'));"
Créer un fichier .bat :
	C:\bin>echo @php "%~dp0composer.phar" %*>composer.bat
Fermer puis ré-ouvrir le terminal.

3 - Ouvrez votre terminal et entrez cette commande :
	composer create-project laravel/laravel --prefer-dist

Etape 2
-------

Configuration serveur :
* Autoriser OpenSSL en https, ouvrir :
	C:\wamp\bin\php\'votre version php'\php.ini
 Chercher la ligne (Ctrl+F) "openssl", enlever le ";" devant "extension".
* PHP >= 5.3.7
* MCrypt PHP Extension

Etape 3
-------

Lire les définitions des différents commits.
Plus d'infos : [Configuration de Laravel4](http://four.laravel.com/#configuration)



## Laravel PHP Framework

[![Latest Stable Version](https://poser.pugx.org/laravel/framework/version.png)](https://packagist.org/packages/laravel/framework) [![Total Downloads](https://poser.pugx.org/laravel/framework/d/total.png)](https://packagist.org/packages/laravel/framework) [![Build Status](https://travis-ci.org/laravel/framework.png)](https://travis-ci.org/laravel/framework)

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable, creative experience to be truly fulfilling. Laravel attempts to take the pain out of development by easing common tasks used in the majority of web projects, such as authentication, routing, sessions, and caching.

Laravel aims to make the development process a pleasing one for the developer without sacrificing application functionality. Happy developers make the best code. To this end, we've attempted to combine the very best of what we have seen in other web frameworks, including frameworks implemented in other languages, such as Ruby on Rails, ASP.NET MVC, and Sinatra.

Laravel is accessible, yet powerful, providing powerful tools needed for large, robust applications. A superb inversion of control container, expressive migration system, and tightly integrated unit testing support give you the tools you need to build any application with which you are tasked.

## Official Documentation

Documentation for the entire framework can be found on the [Laravel website](http://laravel.com/docs).

### Contributing To Laravel

**All issues and pull requests should be filed on the [laravel/framework](http://github.com/laravel/framework) repository.**

### License

The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)
