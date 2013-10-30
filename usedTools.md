Outils utilisés
===============

Communs à tous
--------------

* [Git](http://git-scm.com/)
* [Laravel 4](http://four.laravel.com/docs/introduction)
* [Composer](http://getcomposer.org/)

### PHP & ses extensions

* version PHP >= 5.3.7
* MCrypt PHP Extension (installé et configuré de base)
* OpenSSL PHP Extension (requis pour Composer)

### Editeur de texte

* [Sublime Text 2](http://www.sublimetext.com/2) / [Présentation de Sublime Text 2](http://www.grafikart.fr/tutoriels/sublime-text-2/sublime-text-2-180)

### Hébergement en ligne du dépôt Git

* [Github](https://github.com/) -> [myDropCode repository](https://github.com/Sryther/myDropCode)

### Répartition des tâches / To Do liste

* [Trello](https://trello.com/)

Windows
-------

* [Wamp](www.wampserver.com) ou [EasyPHP](www.easyphp.org)

Linux & Mac
-----------

* [LAMP](http://doc.ubuntu-fr.org/lamp) ou [MAMP](http://www.mamp.info/en/index.html) ou packages pré-installés

Plus
----

### Plugins Sublime Text 2

Suivre ce [lien](http://www.grafikart.fr/blog/sublime-text-2-les-plugins-que-jutilise).

Résumé du lien ci-dessus :

Des plugins font de cette éditeur un des éditeurs les plus rapides du marché. Ces plugins vous aiderons à améliorer votre expérience.

Pour installer un plugin :

Ouvrir la console de Sublime Text 2 et copier ce code :

	import urllib2,os; pf='Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler( ))); open( os.path.join( ipp, pf), 'wb' ).write( urllib2.urlopen( 'http://sublime.wbond.net/' +pf.replace( ' ','%20' )).read()); print( 'Please restart Sublime Text to finish installation')

Redémarrer ST2 (Sublime Text 2).

Pour installer des plugins, faites Ctrl + Shift + P et écrivez "install" puis faites Entrée (ou dans Préférences > Package Control).
Une nouvelle pop-up apparait : écrivez le nom du plugin que vous souhaitez installer et faites Entrée.

Installer les plugins suivants :

* Emmet
* Sublime Code Intel
* Blade Snippets
* Laravel Blade Highlighter
* Le thème de votre choix (Google it)