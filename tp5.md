### TP n°5 : Manipulation du DOM et introduction à Fetch en JavaScript

#### **1. Objectif général :**

Consolider vos compétences en JavaScript en manipulant le DOM et en utilisant Fetch pour effectuer des appels vers un serveur.

- Manipuler le DOM pour générer dynamiquement du contenu HTML.
- Utiliser Fetch pour récupérer des données et les afficher.
- Gérer des événements utilisateur (clics, soumissions de formulaires).

**Les ressources à votre disposition**

- Documentation MDN JavaScript : [https://developer.mozilla.org/fr/docs/Web/JavaScript](https://developer.mozilla.org/fr/docs/Web/JavaScript)
- [Manipulation du DOM](https://developer.mozilla.org/fr/docs/Web/API/Document_Object_Model/Introduction)
- [Documentation Fetch](https://developer.mozilla.org/fr/docs/Web/API/Fetch_API)

---

### **2. Activités pratiques guidées**

#### **1) Manipulation du DOM**

**Exercice 1 : Cibler des éléments**

- Reprendre le fichier `user_list.php` du TP4
- Ajouter un identifiant `id="table"`
- Afficher le noeud du DOM dans la console du navigateur en utilisant la fonction javascript `document.getElementById()`
- Adapter l'utilisation de la fonction pour afficher les lignes `tr`

**Exercice 2 : Ajouter un élément**

- Ajouter un bouton avec pour identifiant `button-add`
- Ajouter un écouteur d'événement `click` sur le bouton grâce à la fonction `document.getElementById(...).addEventListener(...)` et afficher un message dans la console du navigateur


#### **2) Introduction à Fetch**

**Exercice 3 : Récupérer des données depuis une API**

- Utiliser l’API publique suivante : `https://jsonplaceholder.typicode.com/users`.
- Créer une page HTML avec un bouton "Charger les utilisateurs".
- Lorsque le bouton est cliqué, récupérer les données utilisateurs de l’API et les afficher dans une liste HTML.

Snippet de départ :

```html
<button id="load-users">Charger les utilisateurs</button>
<script>
document.getElementById("load-users").addEventListener("click", function() {
    fetch("https://jsonplaceholder.typicode.com/users")
        .then(response => response.json())
        .then(users => {
            console.log(users);
        });
});
</script>
```

**Exercice 4 : Ajouter les données récupérées depuis une API au DOM**

- Reprendre le code de l'exercice précédent et le compléter comme suit :
-- ajouter dans le code html une balise `<ul id="list"></ul>`
-- parcourir la liste des utilisateurs récupérée via fetch pour ajouter autant d'entrées dans la liste `<li></li>` que d'utilisateurs


#### **3) Aller plus loin**

**TP 4 V2**

Après ces premières initiations via des exercices simples, vous pouvez approfondir vos connaissances et vous exercer en utilisans le [TP4 V2](https://github.com/berengergermain/rt-web-dynamique/blob/main/tp4_v2.md)

**Pratique personnelle et installation d'un environnement local**

Pour maîtriser PHP et JavaScript, il est essentiel de pratiquer régulièrement chez soi en dehors des TPs encadrés. N’hésitez pas à reproduire, modifier et tester les exercices vus en cours pour développer vos compétences.

Comment installer PHP et un serveur local :
- Windows : Téléchargez et installez XAMPP, qui inclut Apache, PHP et MySQL dans un seul package. Une fois installé, démarrez Apache via le panneau de contrôle pour tester vos fichiers PHP dans le dossier htdocs.
- MacOS : Installez MAMP, un package similaire à XAMPP pour macOS. Placez vos fichiers PHP dans le dossier htdocs et démarrez les services Apache et MySQL.
- Linux : Utilisez la commande suivante pour installer Apache, PHP et MySQL :
```bash
sudo apt update
sudo apt install apache2 php mysql-server
```

Placez vos fichiers PHP dans le répertoire `/var/www/html` et accédez-y via `http://localhost`.
