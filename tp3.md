## TP n°3 : Interaction avec l'utilisateur via les formulaires HTML et PHP

### **1. Objectif général**

Comprendre comment collecter des données via des formulaires HTML et les traiter avec PHP en utilisant les variables superglobales $_GET et $_POST.

**Les ressources à votre disposition**

- Aide officielle de PHP : https://www.php.net/manual/fr/
  - Pensez à utiliser son moteur de recherche ;)
- Site d'apprentissage multi language pour débutant : https://www.w3schools.com/php/default.asp
- Évitez l'IA pour l'instant, cherchez à comprendre par vous même.

---

### **2. Activités pratiques guidées**

#### **1) Exercices sur la récupération des données**

**Exercice 1 : Premier formulaire**
- Utilisez le formulaire HTML [form.html](https://github.com/berengergermain/rt-web-dynamique/blob/main/form.html) qui contient un champ `nom` et un bouton de soumission.
- Envoyer les données via la méthode GET et récupérez les grâce à `$_GET` dans un fichier result.php et afficher le nom saisi.

**Exercice 2 : Utilisation de `$_POST`**
- Modifier l'exercice précédent pour utiliser `$_POST`.
- Comparer le comportement avec `$_GET`.

**Exercice 3 : Formulaire avec plusieurs champs**
- Créer un formulaire demandant le `nom`, `prénom` et `email`.
- Afficher ces informations après soumission.

**Exercice 4 : Validation de champs**
- Ajouter des vérifications pour s'assurer que les champs ne sont pas vides avant affichage.
- Afficher un message d'erreur si un champ est vide.

**Exercice 5 : Nettoyage des entrées utilisateur**
- Utiliser `htmlspecialchars()` et `trim()` pour éviter les injections et erreurs d'affichage.

#### **2) Exercices sur les champs avancés**

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

**Exercice 10 : Formulaire avec mot de passe**
- Créer un champ de mot de passe et afficher un message si le champ est vide.
- Masquer l'affichage du mot de passe dans la récupération.

#### **3) Exercices combinant formulaires et traitement des données**

**Exercice 11 : Formulaire de connexion simple**
- Demander un nom d'utilisateur et un mot de passe.
- Afficher un message de bienvenue si le nom correspond à une valeur prédéfinie.

**Exercice 12 : Calculatrice simple**
- Créer un formulaire permettant d'entrer deux nombres et une opération (`+`, `-`, `*`, `/`).
- Afficher le résultat de l'opération choisie.

**Exercice 13 : Formulaire de contact**
- Créer un formulaire demandant `Nom`, `Email` et `Message`.
- Afficher un message confirmant l'envoi.

**Exercice 14 : Conversion d'unités**
- Créer un formulaire permettant de convertir des kilomètres en miles.
- Afficher le résultat après soumission.

#### **4) Exercices manipulant les données de formulaire dans du code HTML**

**Exercice 16 : Génération dynamique de tableau HTML**
- Demander à l'utilisateur d'entrer plusieurs noms.
- Afficher ces noms sous forme de tableau HTML.

**Exercice 17 : Affichage conditionnel en fonction des choix utilisateur**
- Demander à l'utilisateur de choisir une couleur dans une liste.
- Changer la couleur de fond de la page en fonction du choix.

**Exercice 18 : Affichage de données sous forme de carte**
- Créer un formulaire demandant `Nom`, `Prénom` et `Age`.
- Afficher ces informations sous forme d'une carte stylisée en HTML/CSS.

**Exercice 19 : Formulaire d'inscription avec confirmation**
- Demander `Nom`, `Email` et `Mot de passe`.
- Ajouter un champ `Confirmer mot de passe` et vérifier qu'il correspond au premier champ.

#### **5) Exercices manipulant les Sessions**

**Exercice 20 : Démarrer et afficher une session**
- Créer une page `session_test.php`.
- Démarrer une session avec `session_start()`.
- Stocker une variable de session `$_SESSION['utilisateur'] = "Alice";`.
- Afficher cette variable sur la page.

**Exercice 21 : Persistance des données de formulaire avec session**
- Créer un formulaire demandant le nom, email et âge d'un utilisateur.
- Lors de la soumission, stocker ces informations dans `$_SESSION`.
- Afficher ces informations sur une autre page `profil.php`.
- Ajouter un bouton "Déconnexion" qui détruit la session et redirige sur la première page.

**Exercice 22 : Compteur de visites avec session**
- Créer une page qui affiche le nombre de fois qu'un utilisateur l'a visitée.
- Utiliser `$_SESSION['visites']` pour incrémenter et afficher le compteur.
