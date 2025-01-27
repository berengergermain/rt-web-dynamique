## TP n°1 : Introduction au PHP et premiers pas

### **1. Objectif général**

Découvrir PHP, comprendre son rôle côté serveur, et apprendre à écrire et exécuter des scripts simples.

**Les ressources à votre disposition**

- Aide officielle de PHP : https://www.php.net/manual/fr/
  - Pensez à utiliser son moteur de recherche ;)
- Site d'apprentissage multi language pour débutant : https://www.w3schools.com/php/default.asp
- Évitez l'IA pour l'instant, cherchez à comprendre par vous même.

---

### **2. Activités pratiques guidées**

**Exercice 1 : Premier affichage**

- Créer un fichier `premier_script.php`.
- Utiliser `echo` pour afficher une phrase simple comme : *"Bienvenue dans mon premier script PHP !"*.

**Exercice 2 : Affichage multi-lignes**

- Utiliser plusieurs instructions `echo` pour afficher :
  - Une phrase par ligne.
  - Bonus : inclure des balises HTML dans les chaînes pour formater le texte.
 
**Exercice 3 : Concaténation de chaînes**

- Créer deux variables pour le prénom et le nom d’une personne.
- Afficher une phrase complète, par exemple : *"Bonjour, je m'appelle Alice Dupont."*

**Exercice 4 : Utilisation de variables simples**

- Créer un script qui déclare trois variables :
  - Une chaîne de caractères.
  - Un nombre entier.
  - Un nombre à virgule.
- Afficher un message combinant ces variables, par exemple : *"Je m'appelle Alice, j'ai 20 ans et je mesure 1.75 mètre."*

**Exercice 5 : Calculs mathématiques simples**

- Créer deux variables avec des nombres.
- Calculer et afficher :
  - Leur somme.
  - Leur produit.
  - Leur différence.
  - Leur division.
  - Leur puissance.

**Exercice 6 : Constantes**

- Déclarer une constante avec `define()` pour le nom de votre site (ex. : "MonSiteWeb").
- Afficher cette constante à plusieurs endroits dans la page.
- Bonus : Ajouter une constante pour l’année en cours.

**Exercice 7 : Les dates**

- Afficher la date et l’heure actuelles au format suivant : *"Nous sommes le vendredi 24 janvier 2025, il est 14h30."*
- Aide : Consulter la documentation et tester différents formats.

**Exercice 8 : Conversion d’unités**

- Créer une variable pour une distance en kilomètres (ex. : `$distance_km = 15;`).
- Convertir et afficher cette distance en mètres et en centimètres.

**Exercice 9 : Génération d’un nombre aléatoire**

- Utiliser la fonction `rand()` pour générer un nombre aléatoire entre 1 et 100.
- Afficher ce nombre dans un message : *"Votre nombre aléatoire est : X."*

**Exercice 10 : Page HTML dynamique avec PHP**

- Créer une page contenant :
  - Un titre personnalisé affiché dynamiquement avec une variable PHP.
  - Un paragraphe indiquant l’heure actuelle.

- Remplacer l'affichage de l'heure actuelle par un message différent selon l’heure (ex. : "Bonjour", "Bon après-midi", "Bonsoir").

- Améliorer la page avec un affichage HTML.

- Un lien vers un autre fichier PHP (créer un fichier `merci.php`) qui affiche un message comme : *"Merci d’avoir visité notre site."*

- Bonus : Afficher le titre du site sur les deux pages en utilisant le même code (pas de copier/coller).
