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

[Configuration de Laravel4](http://four.laravel.com/#configuration)