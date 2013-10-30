Comment installer Laravel4
==========================

Condensé des outils utilisés [ici](https://github.com/Sryther/myDropCode/blob/master/usedTools.md)

Etape 1
-------

Configuration serveur :

* Autoriser OpenSSL en https, ouvrir :

	C:\wamp\bin\php\'votre version php'\php.ini

Chercher la ligne (Ctrl+F) "openssl", enlever le ";" devant "extension".

Pré-requis :

* version PHP >= 5.3.7
* MCrypt PHP Extension (installé et configuré de base)

Etape 2
-------

Laravel utilise Composer pour gérer ses dépendances : [Site de Composer](http://getcomposer.org/)

### Windows

2 - Installer Composer :

* Via l'installateur Windows
* Via le fichier composer.phar [ici](http://getcomposer.org/) :

Ajouter le répertoire où vous avez placé Composer (C:\bin dans cet exemple) et le répertoire de PHP (C:\wamp\bin\php\'votre version php') dans le PATH.

Commandes pour récupérer composer.phar :

	mkdir C:\bin
	cd C:\bin

Placez composer.phar dans C:\bin

Créer un fichier .bat :

	echo @php "%~dp0composer.phar" %*>composer.bat

Fermer puis ré-ouvrir le terminal.

### Mac

2 - Installer Composer :

Changer dans le php.ini > detect_unicode = Off
Lancer Curl :

	$ cd /path/to/my/project
	$ curl -s http://getcomposer.org/installer | php

### Linux

2 - Installer Composer :

Lancer Curl :

	$ curl -sS https://getcomposer.org/installer | php
	$ mv composer.phar /usr/local/bin/composer

3 - Ouvrez votre terminal :
	
	cd /path/to/my/project
	composer create-project laravel/laravel --prefer-dist

Etape 3
-------

Lire les définitions des différents commits.

Plus d'infos : [Configuration de Laravel4](http://four.laravel.com/#configuration)

Etape 4
-------
 
### Modifier ses hosts :

Windows : C:\Windows\system32\drivers\etc\hosts

Mac & Linux : /etc/hosts
 
Rajouter cette ligne :

127.0.0.1       myDropCode.local
 
### Ajouter un Virtual Host :

Windows : C:\wamp\bin\apache\<Version Apache>\conf\extra\httpd-vhosts.conf

Mac : /etc/apache2/extra/httpd-vhosts.conf

Linux : créer un fichier au nom du projet ("myDropCode") dans /etc/apache2/sites-avalaible/
 
Ecrire dedans :
 
	<VirtualHost *:80>
	    DocumentRoot "<Chemin vers le dossier du site>"
	    ServerName <Nom du projet>.local
	    <directory "<Chemin vers le dossier du site>">
	        Options Indexes FollowSymLinks
	        AllowOverride all
	        Order Deny,Allow
	        Deny from all
	        Allow from 127.0.0.1
	    </directory>
	</VirtualHost>
 
Enregistrer.
La balise <Directory> évite d'écrire un .htaccess dans le dossier du site.
 
### Activer les Virtual Hosts (only Linux & Windows) :

Windows : ouvrir le fichier C:\wamp\bin\apache\<Version Apache>\conf\httpd.conf

Chercher la ligne :
 
	# Virtual hosts
	# Include conf/extra/httpd-vhosts.conf
 
Décommentez la ligne :

	# Include conf/extra/httpd-vhosts.conf
 
Linux : sudo a2ensite myDropCode
 
### Redémarrer Apache :

Windows : clic-gauche Wamp > Redémarrer les services

Linux & Mac : sudo apachectl restart
 
Le site est prêt à être utilisé.
 
### More
 
Files :
 
Les fichiers du site sont contenus (sauf si vous avez modifié) dans :

Windows : C:\wamp\www\myCodeDrop\

Linux : /var/www/myDropCode

Mac : /Library/WebServer/Documents/myCodeDrop


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
