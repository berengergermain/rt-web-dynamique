## **TP n°4 : Introduction à MySQL avec PHP**

### **1. Objectif général**

Apprendre à manipuler une base de données MySQL en PHP :

- Se connecter à une base de données.
- Exécuter des requêtes SQL en PHP.
- Récupérer et afficher des données.
- Insérer, modifier et supprimer des informations.

**Les ressources à votre disposition**

- Documentation PHP MySQLi : [https://www.php.net/manual/fr/book.mysqli.php](https://www.php.net/manual/fr/book.mysqli.php)
- Documentation SQL MySQL : [https://dev.mysql.com/doc/](https://dev.mysql.com/doc/)
- W3Schools sur MySQL : [https://www.w3schools.com/mysql/](https://www.w3schools.com/mysql/)

---

### **2. Base de données fournie**

Nous utiliserons une base `tp4_gestion_utilisateurs` contenant une table `utilisateurs` :

```sql
CREATE TABLE utilisateurs (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nom VARCHAR(50) NOT NULL,
    prenom VARCHAR(50) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    age INT NOT NULL
);

INSERT INTO utilisateurs (nom, prenom, email, age) VALUES
('Dupont', 'Alice', 'alice.dupont@example.com', 25),
('Martin', 'Paul', 'paul.martin@example.com', 30),
('Leroy', 'Sophie', 'sophie.leroy@example.com', 22),
('Bernard', 'Luc', 'luc.bernard@example.com', 40),
('Durand', 'Emma', 'emma.durand@example.com', 27),
('Morel', 'Julien', 'julien.morel@example.com', 35),
('Petit', 'Camille', 'camille.petit@example.com', 28),
('Roux', 'Nicolas', 'nicolas.roux@example.com', 32),
('Fournier', 'Elise', 'elise.fournier@example.com', 24),
('Nguyen', 'Thanh', 'thanh.nguyen@example.com', 21),
('Diop', 'Aminata', 'aminata.diop@example.com', 26),
('Lopez', 'Carlos', 'carlos.lopez@example.com', 29),
('Chen', 'Li', 'li.chen@example.com', 23),
('Haddad', 'Samir', 'samir.haddad@example.com', 33),
('Kumar', 'Anjali', 'anjali.kumar@example.com', 31);
```

---

### **3. Exercices pratiques guidés**

#### **1) Connexion à la base de données**

**Exercice 1 : Établir une connexion MySQL**

- Créer un fichier `connexion.php` qui établit une connexion avec la base `tp4_gestion_utilisateurs`.
- Afficher un message si la connexion est réussie ou échoue.

#### **2) Récupération et affichage des données**

**Exercice 2 : Afficher tous les utilisateurs**

- Récupérer toutes les lignes de la table `utilisateurs`.
- Les afficher dans une table HTML.

**Exercice 3 : Afficher un utilisateur spécifique**

- Créer une nouvelle page `voir.php`.
- Modifier l’URL pour passer un `id` en paramètre (`?id=1`).
- Récupérer et afficher uniquement l’utilisateur correspondant.

**Exercice 4 : Affichage avec tri**

- Modifier la requête de l'exercice 2 pour trier les utilisateurs par âge décroissant.

**Exercice 5 : Rechercher un utilisateur par son nom**

- Créer un formulaire PHP contenant un champ de recherche permettant de saisir un nom.
- Lors de la soumission du formulaire, afficher les utilisateurs dont le nom contient la valeur entrée.

#### **3) Insertion de nouvelles données**

**Exercice 6 : Formulaire d’ajout d’un utilisateur**

- Créer une nouvelle page `ajout.php` avec un formulaire pour ajouter un nouvel utilisateur (`nom`, `prenom`, `email`, `age`).
- Insérer ces données dans la base lors de la soumission du formulaire et afficher un message de succès ou d'erreur.

**Exercice 7 : Validation des données avant insertion**

- Vérifier que les champs ne sont pas vides et que l’email est bien au format correct.

#### **4) Mise à jour et suppression de données**

**Exercice 8 : Modifier un utilisateur**

- Ajouter un lien "Modifier" au bout de chaque ligne du tableau d'utilisateurs.
- Passez en paramètre l'identifiant de l'utilisateur à modifier.
- Créer et traiter le formulaire permettant de modifier ses informations.

**Exercice 9 : Supprimer un utilisateur**

- Ajouter un bouton "Supprimer" à côté de chaque utilisateur.
- Supprimer l’utilisateur correspondant après confirmation.

#### **5) Requêtes avancées**

**Exercice 10 : Compter le nombre d’utilisateurs**

- Afficher le nombre total d’utilisateurs inscrits.

**Exercice 11 : Pagination des résultats**

- N’afficher que 2 utilisateurs par page avec des boutons "Suivant" et "Précédent".

#### **6) Sécurité et bonnes pratiques**

**Exercice 12 : Protection contre les injections SQL**

- Modifier les requêtes pour utiliser des requêtes préparées (`mysqli_prepare`).

**Exercice 13 : Protection contre les XSS**

- Nettoyer les entrées utilisateurs avec `htmlspecialchars()`.

**Exercice 14 : Gestion des erreurs MySQL**

- Afficher des messages d'erreur clairs en cas d'échec d’une requête.

#### **7) Fonctions et modularisation du code**

**Exercice 15 : Créer une fonction générique pour exécuter des requêtes**

- Éviter les répétitions en écrivant une fonction `executerRequete($sql, $params)`.

**Exercice 16 : Organisation en plusieurs fichiers**

- Diviser le projet en plusieurs fichiers (`connexion.php`, `functions.php`, `index.php`, etc.).
