### TP n°4 : Gestion d'une base de données en PHP

#### **1. Objectif général :**

Apprendre à interagir avec une base de données MySQL en PHP :

- Se connecter à une base de données.
- Exécuter des requêtes SQL en PHP.
- Récupérer et afficher des données.
- Insérer, modifier et supprimer des informations.

**Les ressources à votre disposition**

- Documentation PHP MySQLi : [https://www.php.net/manual/fr/book.mysqli.php](https://www.php.net/manual/fr/book.mysqli.php)
- Documentation SQL MySQL : [https://dev.mysql.com/doc/](https://dev.mysql.com/doc/)
- W3Schools sur MySQL : [https://www.w3schools.com/mysql/](https://www.w3schools.com/mysql/)

---

### **2. Activités pratiques guidées**

#### **1) Premiers pas avec une base de données**

**Exercice 1 : Création de la base de données et d'une table**

- Dans PHPMyAdmin, créez une base de données, sélectionnez-la puis exécutez le script SQL suivant :

```sql
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    user_name VARCHAR(50) NOT NULL,
    password VARCHAR(255) NOT NULL
);

INSERT INTO users (user_name, password) VALUES
('Alice', 'password123'),
('Bob', 'securepass'),
('Charlie', 'mypassword');
```

**Exercice 2 : Connexion à la base de données en PHP**

- Créez un fichier `db_connect.php` contenant le code suivant :

```php
<?php
$host = 'localhost';
$dbname = 'users_db';
$user = ''; // Votre nom d'utilisateur mysql.
$password = ''; // Votre mot de passe mysql
$conn = mysqli_connect($host, $user, $password, $dbname);

if (!$conn) {
    die("Échec de la connexion : " . mysqli_connect_error());
}
echo "Connexion réussie !";
?>
```

- Testez et vérifiez que la connexion fonctionne.

**Exercice 3 : Récupération des utilisateurs dans une page PHP**

- Créez un fichier `user_list.php` qui :
  - Se connecte à la base de données.
  - Exécute une requête `SELECT * FROM users`.
  - Faite une boucle while pour parcourir les résultats et afficher les en mode debug avec \`var\_dump()\`.
    - Un peu d'aide ? cf. [https://www.w3schools.com/php/php\_mysql\_select.asp](https://www.w3schools.com/php/php_mysql_select.asp) (n'oubliez pas que pour l'instant, vous codez en procédural, pas en objet).

**Exercice 4 : Affichage des utilisateurs dans un tableau HTML**

- Modifiez l'exercice précédent pour afficher les utilisateurs dans un tableau HTML.

Exemple de code avec des éléments à compléter :

```php
<?php
$host = 'localhost';
$dbname = 'users_db';
$user = 'root';
$password = '';
$conn = mysqli_connect($host, $user, $password, $dbname);

if (!$conn) {
    die("Échec de la connexion : " . mysqli_connect_error());
}

$query = "SELECT * FROM users";
$result = mysqli_query($conn, $query);

// TODO : Ajouter le début du tableau HTML
while ($row = mysqli_fetch_assoc($result)) {
    // TODO : Afficher chaque utilisateur dans une ligne de tableau
}
// TODO : Fermer le tableau HTML

mysqli_close($conn);
?>
```

---

#### **2) Implémentation d'un système de connexion avec base de données**

**Exercice 5 : Formulaire de connexion**\
Créez une page `login.php` contenant :

- Un formulaire HTML avec deux champs : `user_name` et `password`.
- Un bouton de validation.
- Une action qui envoie les données à `login_process.php` via `POST`.

**Exercice 6 : Vérification des identifiants en base de données**\
Dans `login_process.php`, compléter le code suivant pour rechercher l'utilisateur dans la base de données :

```php
<?php
// Connection à la base de données

// Récupération des données du formulaire.
$user_name = $_POST['user_name'];
$user_password = $_POST['password'];

// Compléter la clause WHERE pour retrouver le bon utilisateur
$query = "SELECT * FROM users WHERE ";
$result = mysqli_query($conn, $query);

if (mysqli_num_rows($result) > 0) {
    // Affichage de l'utilisateur.
} else {
    echo "Identifiants incorrects.";
}

mysqli_close($conn);
?>
```

---

#### **3) Introduction aux sessions et protection des pages**

**Exercice 7 : Démarrer une session après connexion**\
Dans `login_process.php`, si l'utilisateur est authentifié, au lieu de l'afficher :

- Démarrez une session avec `session_start()`.
- Stockez `user_name` dans `$_SESSION`.
- Redirigez vers `profile.php`.

Voici un exemple pour faire une redirection en PHP :

```php
<?php
header("Location: login.php");
exit();
?>
```

**Exercice 8 : Page de profil protégée**
Créez une page `profile.php` qui :

- Vérifie si un utilisateur est stocké en session.
- Affiche le profile de l'utilisateur si c'est le cas.
- Redirige vers `login.php` dans le cas contraire

**Exercice 9 : Déconnexion**

- Ajoutez un bouton "Déconnexion" sur `profile.php`.
- Créez `logout.php` pour détruire la session et rediriger vers `login.php`.
