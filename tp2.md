## TP n°2 : Manipuler des tableaux et des fonctions

### **1. Objectif général**

* Découvrir les tableaux PHP et comprendre leur principe de fonctionnement.
* Écrire ses propres fonctions pour structurer et réutiliser son code.
* Générer dynamiquement des (portions de) pages HTML simples.

**Les ressources à votre disposition**

- Aide officielle de PHP : https://www.php.net/manual/fr/
  - Pensez à utiliser son moteur de recherche ;)
- Site d'apprentissage multi language pour débutant : https://www.w3schools.com/php/default.asp
- Évitez l'IA pour l'instant, cherchez à comprendre par vous même.

---

### **2. Activités pratiques guidées**

#### **1) Exercices sur les tableaux**

**Exercice 1 : Déclaration et affichage d'un tableau**

- Créer un tableau contenant 5 prénoms.
- Afficher chaque élément du tableau avec une boucle `foreach`.

**Exercice 2 : Ajout et suppression d'éléments**

- Ajouter un nouvel élément à la fin du tableau et afficher le tableau mis à jour.
- Supprimer le premier élément du tableau et afficher le tableau mis à jour.

**Exercice 3 : Tableau associatif**

- Créer un tableau associatif représentant une personne avec les clés `nom`, `prénom` et `age`.
- Afficher ces informations sous la forme : *"Nom : Dupont, Prénom : Alice, Age : 25 ans"*.

**Exercice 4 : Tri d'un tableau**

- Créer un tableau contenant plusieurs nombres et le trier avec `sort()`.
- Afficher le tableau trié.

**Exercice 5 : Recherche dans un tableau**

- Créer un tableau contenant une liste de fruits.
- Vérifier si "Banane" est présent dans le tableau avec `in_array()`.
- Afficher un message indiquant si le fruit est trouvé ou non.

**Exercice 6 : Fusion de tableaux**

- Créer deux tableaux différents et les fusionner avec `array_merge()`.
- Afficher le tableau résultant.

#### **2) Exercices sur les fonctions**

**Exercice 7 : Fonction simple**

- Créer une fonction `bonjour()` qui affiche "Bonjour, bienvenue !" lorsqu'elle est appelée.
- Appeler cette fonction dans un script et observer le résultat.

**Exercice 8 : Fonction avec paramètre**

- Créer une fonction `direBonjour($prenom)` qui affiche "Bonjour, [prénom] !".
- Appeler cette fonction avec différents prénoms.

**Exercice 9 : Fonction avec valeur par défaut**

- Créer une fonction salutation(\$nom, \$civilite = "M.") qui affiche "Bonjour M./Mme [nom]".
- Tester avec et sans le deuxième paramètre.

**Exercice 10 : Fonction avec retour de valeur**

- Créer une fonction `addition($a, $b)` qui retourne la somme de deux nombres.
- Tester cette fonction avec différentes valeurs et afficher le résultat.

**Exercice 11 : Fonction calculant une moyenne**

- Créer une fonction `moyenne($notes)` qui calcule la moyenne d'un tableau de notes.
- Tester cette fonction avec plusieurs ensembles de notes.

**Exercice 12 : Fonction récursive**

- Créer une fonction `factorielle($n)` qui calcule la factorielle d'un nombre.
- Tester avec plusieurs valeurs de `$n`.

#### **3) Exercices combinant tableaux et fonctions**

**Exercice 13 : Fonction affichant un tableau**

- Créer une fonction `afficherTableau($tab)` qui affiche tous les éléments d'un tableau passé en paramètre.
- Tester cette fonction avec un tableau contenant des noms de villes.

**Exercice 14 : Filtrage d'un tableau avec une fonction**

- Créer une fonction `filtrerTableau($tab, $limite)` qui retourne un tableau contenant uniquement les nombres supérieurs à `$limite`.
- Tester cette fonction avec un tableau de nombres.

**Exercice 15 : Fonction retournant un tableau**

- Créer une fonction `genererTableau($taille)` qui retourne un tableau contenant `$taille` nombres aléatoires.
- Afficher le tableau retourné.

**Exercice 16 : Transformation d'un tableau avec une fonction**

- Créer une fonction `mettreMajuscule($mots)` qui transforme tous les mots d'un tableau en majuscules.
- Tester cette fonction avec un tableau de mots.

#### **4) Exercices manipulant des tableaux dans du code HTML**

**Exercice 17 : Affichage d'une liste de contacts**

- Créer un tableau PHP contenant plusieurs contacts avec `nom`, `prénom` et `email`.
- Afficher ces contacts sous forme de liste `<ul>` en HTML.

**Exercice 18 : Affichage d'un tableau HTML**

- Créer un tableau PHP contenant des produits (`nom`, `prix`, `quantité`).
- Générer un tableau HTML (`<table>`) affichant ces informations sous forme de colonnes.

**Exercice 19 : Génération dynamique de menu**

- Créer un tableau PHP contenant une liste de pages (`Accueil`, `Services`, `Contact`).
- Générer dynamiquement un menu `<nav>` avec des liens HTML correspondants.

**Exercice 20 : Affichage conditionnel dans un tableau HTML**

- Créer un tableau PHP de notes d'étudiants.
- Afficher chaque note dans une ligne de tableau HTML, en mettant en gras celles supérieures à 15.
