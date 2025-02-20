### TP n°5 : Introduction à JavaScript

#### **Objectif général :**

Découvrir la syntaxe de base de JavaScript et apprendre à interagir avec le DOM et le BOM, manipuler des événements et récupérer des données à partir d'une API distante.

---

### **Plan de la séance**

#### **1. Introduction à JavaScript**

- Qu'est-ce que JavaScript et à quoi sert-il ?
- Où écrire du code JavaScript ? (fichier `.js`, balise `<script>` dans HTML)
- Premiers pas avec `console.log()`

**Tuto 1 : Premier script JavaScript**
- Créez un fichier `script.js` et incluez-le dans un fichier `index.html`.
- Dans `script.js`, ajoutez le code suivant et observez le résultat dans la console du navigateur :

```js
console.log("Bonjour, JavaScript !");
```

**Exercice 1 :**
- Ajoutez une variable pour stocker le nom de l'utilisateur et adaptez le console.log() pour afficher le message "Bonjour, <nom de l'utilisateur>".
- Utilisez une constante au lieu d'une variable.

---

#### **2. Manipulation du DOM**

- Comprendre ce qu'est le DOM
- Sélectionner des éléments avec `document.querySelector()` et `document.getElementById()`
- Modifier le texte et les styles CSS dynamiquement

**Tuto 2 : Modifier un élément HTML**
- Ajoutez un paragraphe dans `index.html` :

```html
<p id="text">Texte initial</p>
<button id="changeText">Changer le texte</button>
```

- Dans `script.js`, ajoutez le code suivant pour modifier le texte en cliquant sur le bouton :

```js
const button = document.getElementById("changeText");
const paragraph = document.getElementById("text");

button.addEventListener("click", () => {
    paragraph.textContent = "Texte modifié !";
});
```

**Exercice 2**
- Reprenez le tuto n°2 et trouvez comment ajouter du balisage HTML à la place du texte.

---

#### **3. Gestion des événements**

- Introduction aux événements (click, mouseover, keydown...)
- Ajout d'écouteurs d'événements avec `addEventListener()`

**Tuto 3 : Changer la couleur d'un élément au survol**

- Ajoutez un div stylisé dans `index.html` :

```html
<div id="box" style="width: 100px; height: 100px; background-color: blue;"></div>
```

- Ajoutez le code suivant dans `script.js` :

```js
const box = document.getElementById("box");

box.addEventListener("mouseover", () => {
    box.style.backgroundColor = "red";
});

box.addEventListener("mouseout", () => {
    box.style.backgroundColor = "blue";
});
```

**Exercice 3:**
- Reprenez le tuto n°3 et faites en sorte que les changements de couleur se produisent lors de l'appui sur la touche du clavier correspondant à la première lettre de la couleur.

---

#### **4. Interaction avec le BOM**

- Introduction au BOM (Browser Object Model)
- Utilisation de `alert()`, `confirm()` et `prompt()`

**Tuto 4 : Afficher une alerte et demander une confirmation**

- Ajoutez un bouton dans `index.html` :

```html
<button id="alertButton">Afficher une alerte</button>
<button id="confirmButton">Demander confirmation</button>
```

- Ajoutez le code suivant dans `script.js` :

```js
const alertButton = document.getElementById("alertButton");
const confirmButton = document.getElementById("confirmButton");

alertButton.addEventListener("click", () => {
    alert("Ceci est une alerte !");
});

confirmButton.addEventListener("click", () => {
    const response = confirm("Voulez-vous continuer ?");
    if (response) {
        console.log("L'utilisateur a confirmé.");
    } else {
        console.log("L'utilisateur a annulé.");
    }
});
```

**Exercice 4:**
- Combinez les techniques des tutos n°3 et n°4 pour changer la couleur du texte uniquement si l'utilisateur est d'accord.

---

#### **5. Interaction avec une API distante**

- Introduction à `fetch()` pour récupérer des données depuis une API
- Manipulation des données JSON

**Tuto 5 : Afficher une blague aléatoire depuis une API**

- Ajoutez un bouton dans `index.html` :

```html
<button id="getJoke">Obtenir une blague</button>
<p id="joke"></p>
```

- Ajoutez le code suivant dans `script.js` pour récupérer une blague et l'afficher :

```js
const jokeButton = document.getElementById("getJoke");
const jokeText = document.getElementById("joke");

jokeButton.addEventListener("click", () => {
    fetch("https://official-joke-api.appspot.com/random_joke")
        .then(response => response.json())
        .then(data => {
            jokeText.textContent = `${data.setup} - ${data.punchline}`;
        })
        .catch(error => {
            jokeText.textContent = "Erreur lors du chargement de la blague.";
        });
});
```

**Exercice 5 (bonus +2pts)**
- Codez votre propre API de blagues en PHP et contactez-la avec javascript !
