## TP n°3 : manipuler les formulaires HTML avec PHP et persister des données en session grâce aux variables super globales.

### **1. Objectif général**

Comprendre comment collecter des données via des formulaires HTML et les traiter avec PHP en utilisant les variables superglobales $_GET et $_POST.
Manipuler une session utilisateur avec $_SESSION.

**Les ressources à votre disposition**

- Aide officielle de PHP : https://www.php.net/manual/fr/
  - Pensez à utiliser son moteur de recherche ;)
  - Aide de la fonction [session_start()](https://www.php.net/manual/fr/function.session-start.php)
- Site d'apprentissage multi language pour débutant : https://www.w3schools.com/php/default.asp
  - [Tuto sur les sessions](https://www.w3schools.com/php/php_sessions.asp)
- Évitez l'IA pour l'instant, cherchez à comprendre par vous même 😉

---

### **2. Activités pratiques guidées**

#### **1) Exercices sur la récupération des données**

**Exercice 1 : Premier formulaire**
- Utiliser le formulaire HTML [form.html](https://github.com/berengergermain/rt-web-dynamique/blob/main/form.html) qui contient un champ `nom` et un bouton de soumission.
- Envoyer les données via la méthode GET et récupérez-les grâce à la variable `$_GET` dans un fichier `result.php` et afficher le nom saisi.

> Attention à l'URL du fichier result.php sur rt-projet

**Exercice 2 : Utilisation de `$_POST`**
- Modifier l'exercice précédent pour utiliser `$_POST`.
- Comparer le comportement avec `$_GET`.

**Exercice 3 : Formulaire avec plusieurs champs**
- Créer un formulaire demandant le `nom`, `prénom` et `email`.
- Afficher ces informations après soumission.

**Exercice 4 : Validation de champs**
- Ajouter des vérifications pour s'assurer que les champs ne sont pas vides avant affichage.
- Afficher un message d'erreur si un champ est vide.

**Exercice 5 (exercice avancée) : Nettoyage des entrées utilisateur**
- Utiliser `htmlentities()` et `trim()` pour éviter les injections et erreurs d'affichage.

#### **2) Exercices sur les champs de formulaire avancés**

**Exercice 6 : Boutons radio**
- Créer un formulaire demandant le genre (`Homme`, `Femme`, `Autre`).
- Afficher le choix sélectionné après soumission.

**Exercice 7 : Cases à cocher**
- Demander à l'utilisateur de choisir ses centres d'intérêt parmi plusieurs options.
- Afficher les choix sélectionnés sous forme de liste.

**Exercice 8 : Liste déroulante**
- Créer un formulaire avec une liste de pays.
- Afficher le pays choisi après soumission.

**Exercice 9 : Champ de texte long**
- Ajouter un champ `textarea` permettant d'écrire un commentaire.
- Afficher le contenu après soumission en préservant la mise en forme.

#### **3) Exercices combinant formulaires et traitement des données**

> À partir de ce point, essayez de regrouper un formulaire HTML et son traitement PHP dans le même fichier.

**Exercice 10 : Formulaire de connexion simple**
- Demander un nom d'utilisateur et un mot de passe.
- Afficher un message de bienvenue si le login et le mot de passe correspondent à des valeurs prédéfinies (par ex: admin:1234), sinon afficher un message d'erreur.

**Exercice 11 : Conversion d'unités**
- Créer un formulaire permettant de convertir des kilomètres en miles.
- Afficher le résultat après soumission.

**Exercice 12 (exercice avancé) : Calculatrice simple**
- Créer un formulaire permettant d'entrer deux nombres et une opération (`+`, `-`, `*`, `/`).
- Afficher le résultat de l'opération choisie.

#### **4) Exercices manipulant les données de formulaire dans du code HTML**

**Exercice 13 : Génération dynamique de tableau HTML**
- Demander à l'utilisateur d'entrer plusieurs noms.
- Afficher ces noms sous forme de tableau HTML.

**Exercice 14 : Affichage conditionnel en fonction des choix utilisateur**
- Demander à l'utilisateur de choisir une couleur dans une liste.
- Changer la couleur de fond de la page en fonction du choix.

**Exercice 15 : Affichage de données sous forme de carte**
- Créer un formulaire demandant `Nom`, `Prénom` et `Age`.
- Afficher ces informations sous forme d'une carte stylisée en HTML/CSS.

#### **5) Exercices manipulant les Sessions**

> À partir de ce point, vous en savez assez pour créer une petite application web de plusieurs pages.
> Essayez d'organiser votre code dans différents fichiers et faite navigez l'utilisateur de l'un à l'autre.

**Exercice 16 : Démarrer et afficher une session**
- Créer une page `session_test.php`.
- Démarrer une session avec `session_start()`.
- Stocker une variable de session `$_SESSION['utilisateur'] = "Alice";`.
- Afficher cette variable sur la page `session_test`.php.

**Exercice 17 (exercice avancé) : Persistance des données de formulaire avec session**
- Créer un formulaire demandant le nom, email et âge d'un utilisateur.
- Lors de la soumission, stocker ces informations dans `$_SESSION`.
- Afficher ces informations sur une autre page `profil.php`.
- Ajouter un bouton "Déconnexion" qui détruit la session et redirige sur la première page.

**Exercice 18 : Compteur de visites avec session**
- Créer une page qui affiche le nombre de fois qu'un utilisateur l'a visitée.
- Utiliser `$_SESSION['visites']` pour incrémenter et afficher le compteur.
