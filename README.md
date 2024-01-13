# 🔖 Bienvenue sur Book Your Medias !
## Description
Réalisation d'une application web mettant en relation une médiathèque et ses consommateurs. L'utilisateur peut se connecter/s'inscrire et réserver des oeuvres. Un espace back-end est disponible pour les employés, permettant ainsi la gestion des délivrances des livres, films, albums.

## 💾 Comment installer le projet ?
1. Cloner le dépôt Git sur son ordinateur.
2. Lancer `composer install`, suivi de composer `dump-autoload`.
3. Créer un fichier _config/db.php_, à partir du fichier _config/db.php.dist_ et ajouter les paramètres de votre base de données. Ne supprimer pas le fichier _.dist_.
4. Importez _database.sql_ dans votre serveur SQL, vous pouvez le faire manuellement ou utiliser le script **migration.php** qui importera un fichier _database.sql_. Lancer : `php migration.php`.
5. Exécutez le serveur web PHP interne avec `php -S localhost:8000 -t public`. L'option -t avec public comme paramètre signifie que votre hôte local ciblera le dossier /public.
6. Allez sur http://localhost:8000 avec votre navigateur préféré.


## 🧑‍💻 Comment attribuer le rôle d'administrateur à un utilisateur ?
Nous souhaitons rendre administrateur l'utilisateur suivant (insérer ces données via la page _Inscription_) :
-   Email : _support@bookmedias.fr_
-   Pseudo : _claudia-admin_
-   Mot de passe : _admin_

1.  Avant tout, l’utilisateur doit se déconnecter.
2. Ouvrir un terminal et se connecter sur mysql. Commande : `mysql -u nomUtilisateur -p`.
3. Après s'être placer sur la bonne base de donnée, lancer la commande `UPDATE user SET role=1 WHERE pseudo="claudia-admin";`. 
4. Lorsque _claudia-admin_ se connectera, un lien vers le back office sera disponible.
