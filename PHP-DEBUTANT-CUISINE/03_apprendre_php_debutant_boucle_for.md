# 🍳 Cours PHP pour Débutant – La Boucle `for` 🍰⚙️

---

## 🎯 Pourquoi une boucle ?

Imagine que tu veux **remplir 10 assiettes** une par une 🍽️

Tu pourrais écrire :
```php
echo "Je remplis l’assiette numéro 1<br>";
echo "Je remplis l’assiette numéro 2<br>";
echo "Je remplis l’assiette numéro 3<br>";
// ...
```

Mais soyons honnêtes…  
👉 Au bout de 10 lignes, tu renverses la sauce 😅  
👉 Au bout de 100, t’as cramé le plat 🔥👨‍🍳

Heureusement, PHP te donne un **outil magique** : la **boucle** 🔁  
Elle te permet de **répéter une action automatiquement**, sans te fatiguer.

---

## 💡 C’est quoi une boucle ?

Une **boucle**, c’est comme un **chef qui dresse les assiettes une à une** 👨‍🍳  
Tu lui dis :  
> “Mets la garniture, ajoute la sauce, passe à l’assiette suivante.”  

Et lui le fait sans broncher 🍝  

💬 En PHP, ça se traduit comme ceci :  

```php
for ($i = 1; $i <= 10; $i++) {
    echo "Je remplis l’assiette numéro $i<br>";
}
```

---

## 🧩 Le fonctionnement de la boucle `for` ⚙️

Regarde cette ligne :
```php
for ($i = 1; $i <= 10; $i++)
```

C’est une **recette en 3 étapes** 🧂

| Étape | Ce qui se passe dans ta cuisine |
|----------|---------------------------|
| `$i = 1` | Tu commences à **la première assiette** 🍽️ |
| `$i <= 10` | Tu continues tant que tu n’as pas **servi les 10 assiettes** 👨‍🍳 |
| `$i++` | Tu **passes à l’assiette suivante** ➡️ |

---

### 🥣 1️⃣ `$i = 1` — Le début du service

Le chef prépare la **première assiette**.  
Tout est propre et prêt pour le dressage.

---

### 🔥 2️⃣ `$i <= 10` — Le service continue

Tu continues à servir **jusqu’à la dixième assiette**.  
Quand `$i` devient 11 :  
> “🎉 Service terminé, tout le monde est servi !”

La boucle s’arrête toute seule.

---

### 🍰 3️⃣ `$i++` — Passer au plat suivant

Chaque fois qu’une assiette est terminée :  
> “+1 assiette dressée ✅”

🧠 En langage cuisine : `$i++`, c’est comme dire **“suivant !”**

---

## 💬 Ce que fait la boucle

```php
for ($i = 1; $i <= 10; $i++) {
    echo "Je remplis l’assiette numéro $i<br>";
}
```

Résultat :
```
Je remplis l’assiette numéro 1
Je remplis l’assiette numéro 2
...
Je remplis l’assiette numéro 10
```

Quand la boucle atteint 11 :  
> “✅ Service terminé, tout le monde est servi !” 🍽️

---

## 🧁 Exemple 2 – Cuisson des gâteaux 🧑‍🍳

```php
for ($gateau = 1; $gateau <= 5; $gateau++) {
    echo "Je cuis le gâteau numéro $gateau<br>";
}
```

Résultat :
```
Je cuis le gâteau numéro 1
Je cuis le gâteau numéro 2
Je cuis le gâteau numéro 3
Je cuis le gâteau numéro 4
Je cuis le gâteau numéro 5
```

💬 Et voilà, tous tes gâteaux sont sortis du four, **sans rien rater !** 🎂

---

## 👨‍🍳 En résumé version cuisine

| Élément | Dans la cuisine | En PHP |
|----------|----------------|--------|
| `$i = 1` | Première assiette | Valeur de départ |
| `$i <= 10` | Tant qu’il reste des plats à faire | Condition de fin |
| `$i++` | Passer à l’assiette suivante | Incrémentation |
| `for` | Répéter le geste | Boucle magique |

---

## 💬 Phrase à retenir
> La boucle `for`, c’est ton **service automatique** :  
> tu dis au commis **quand commencer**, **quand s’arrêter**,  
> et il répète l’action sans jamais se plaindre. 🍳✨

---

# 🧪 Exercices (niveau cuisine)

### 🍽️ Exercice 1
Affiche :  
> “Je remplis l’assiette numéro X”  
pour X allant de 1 à 10.

### 🧁 Exercice 2
Affiche :  
> “Je cuis le gâteau numéro X”  
pour X allant de 1 à 5.

### 🍳 Exercice 3
Affiche :  
> “Je casse l’œuf numéro X”  
pour X allant de 1 à 6.

### 🧂 Exercice 4
Affiche :  
> “Je verse la cuillère numéro X”  
pour X allant de 1 à 4.

### 🥗 Exercice 5
Affiche :  
> “Je dresse l’assiette numéro X”  
pour X allant de 1 à 5.

### 🧮 Exercice 6
Affiche tous les **nombres pairs** de cuillères (2, 4, 6, 8, 10).

### ⏳ Exercice 7
Affiche un **compte à rebours** de cuisson (10 à 1).

### 🧁 Exercice 8
Affiche la **table de multiplication du sucre** (5 x 1, 5 x 2, etc.) façon pâtissier.

### 🍞 Exercice 9
Affiche :  
> “Je prépare le sandwich numéro X”  
pour X allant de 1 à 3, puis affiche :  
> “Tous les sandwichs sont prêts !” 🥪

### ☕ Exercice 10
Affiche ton **nom de chef** 5 fois ☕

---

# ✅ Solutions

```php
// 1
for ($i = 1; $i <= 10; $i++) {
    echo "Je remplis l’assiette numéro $i<br>";
}

// 2
for ($i = 1; $i <= 5; $i++) {
    echo "Je cuis le gâteau numéro $i<br>";
}

// 3
for ($i = 1; $i <= 6; $i++) {
    echo "Je casse l’œuf numéro $i<br>";
}

// 4
for ($i = 1; $i <= 4; $i++) {
    echo "Je verse la cuillère numéro $i<br>";
}

// 5
for ($i = 1; $i <= 5; $i++) {
    echo "Je dresse l’assiette numéro $i<br>";
}

// 6
for ($i = 2; $i <= 10; $i += 2) {
    echo "Je verse $i cuillères de sucre<br>";
}

// 7
for ($i = 10; $i >= 1; $i--) {
    echo "Temps restant : $i minutes<br>";
}

// 8
for ($i = 1; $i <= 10; $i++) {
    $quantite = 5 * $i;
    echo "5 x $i = $quantite grammes de sucre<br>";
}

// 9
for ($i = 1; $i <= 3; $i++) {
    echo "Je prépare le sandwich numéro $i<br>";
}
echo "Tous les sandwichs sont prêts !<br>";

// 10
for ($i = 1; $i <= 5; $i++) {
    echo "Chef Laurent<br>";
}
```
