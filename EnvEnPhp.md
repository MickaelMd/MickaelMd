Installer et utiliser un fichier .env en PHP
============================================

Pour installer et utiliser un fichier `.env` en PHP, il est courant d'utiliser une bibliothèque comme **vlucas/phpdotenv** qui facilite la gestion des variables d'environnement. Voici les étapes à suivre pour installer et configurer un fichier `.env` dans un projet PHP :

Étapes d'installation et configuration :
----------------------------------------

### 1\. Installer Composer (si ce n'est pas déjà fait) :

Si tu n'as pas encore installé Composer, tu peux le télécharger depuis [getcomposer.org](https://getcomposer.org).

### 2\. Installer la bibliothèque `vlucas/phpdotenv` :

Dans ton projet, ouvre un terminal à la racine de ton projet et exécute la commande suivante :

    composer require vlucas/phpdotenv

### 3\. Créer un fichier `.env` :

À la racine de ton projet, crée un fichier nommé `.env`. Dans ce fichier, tu peux définir des variables d'environnement, par exemple :

    DB_HOST=localhost
    DB_PORT=3306
    DB_DATABASE=nom_de_la_base
    DB_USERNAME=root
    DB_PASSWORD=mot_de_passe

### 4\. Charger les variables d'environnement dans ton projet PHP :

Dans ton fichier PHP principal (par exemple, `index.php`), tu dois charger et utiliser les variables de ton fichier `.env`. Voici un exemple de code :

    <?php
    require 'vendor/autoload.php';
    
    use Dotenv\Dotenv;
    
    // Charger le fichier .env
    $dotenv = Dotenv::createImmutable(__DIR__);
    $dotenv->load();
    
    // Utiliser une variable d'environnement
    $dbHost = $_ENV['DB_HOST'];
    $dbPort = $_ENV['DB_PORT'];

### 5\. Accéder aux variables d'environnement :

Une fois le fichier `.env` chargé, tu peux accéder aux variables définies via `$_ENV` ou `getenv()` :

    echo $_ENV['DB_DATABASE']; // ou
    echo getenv('DB_DATABASE');

### Attention :

Ne pas oublier d'ajouter ton fichier `.env` dans le fichier `.gitignore` si tu utilises Git, pour éviter de partager des informations sensibles (comme les mots de passe) :

    .env

Avec cette configuration, tu seras capable de gérer tes configurations d'application via des variables d'environnement dans PHP.
