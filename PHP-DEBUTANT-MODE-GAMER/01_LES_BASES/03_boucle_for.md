# 🎮 Cours PHP pour Débutant – La Boucle `for` ⚔️🧠

---

## 🎯 Pourquoi une boucle ?

Imagine que tu veux **battre 10 ennemis** un par un 👾

Tu pourrais écrire :
```php
echo "Je combats l’ennemi numéro 1<br>";
echo "Je combats l’ennemi numéro 2<br>";
echo "Je combats l’ennemi numéro 3<br>";
// ...
```

Mais soyons honnêtes…  
👉 Au bout de 10 lignes, t’as envie de **ragequit** 😅  
👉 Au bout de 100, ton clavier explose 💥🎮

Heureusement, PHP te donne une compétence épique : la **boucle** 🌀  
Elle te permet de **répéter une action automatiquement** sans te fatiguer.

---

## 💡 C’est quoi une boucle ?

Une **boucle**, c’est comme un **personnage qui farm de l’XP en boucle** 😎  
Tu lui dis :  
> “Tue un monstre, gagne de l’XP, recommence… jusqu’à atteindre le niveau max !”  

Et lui le fait sans broncher 🧙‍♂️  

💬 En PHP, ça se traduit comme ceci :  

```php
for ($i = 1; $i <= 10; $i++) {
    echo "Je combats l’ennemi numéro $i<br>";
}
```

---

## 🧩 Le fonctionnement de la boucle `for` ⚙️

Regarde cette ligne :
```php
for ($i = 1; $i <= 10; $i++)
```

C’est une **formule magique** en trois étapes ✨

| Élément | Signification dans le jeu |
|----------|---------------------------|
| `$i = 1` | Je **commence** à l’ennemi numéro **1** 👾 |
| `$i <= 10` | Je **continue** tant que je n’ai **pas battu les 10 ennemis** 💀 |
| `$i++` | Je **passe au prochain ennemi** ➡️ |

---

### 🔹 1️⃣ `$i = 1` — Le début de la quête

Tu lances ta mission au **niveau 1**.  
Ton personnage est prêt à combattre le premier monstre.

---

### 🔹 2️⃣ `$i <= 10` — La condition de victoire

Tu continues à combattre **jusqu’à ce que les 10 ennemis soient vaincus**.  
Quand `$i` devient 11 :  
> “🎉 Mission accomplie, tous les ennemis sont éliminés !”

La boucle s’arrête toute seule.

---

### 🔹 3️⃣ `$i++` — Le passage au prochain round

Chaque fois que tu gagnes un combat, tu avances vers le suivant :  
> “+1 ennemi battu ✅”

🧠 En langage gamer : `$i++` c’est ton **gain d’expérience** → tu passes au **niveau suivant**.

---

## 💬 Ce que fait la boucle

```php
for ($i = 1; $i <= 10; $i++) {
    echo "Je combats l’ennemi numéro $i<br>";
}
```

Résultat :
```
Je combats l’ennemi numéro 1
Je combats l’ennemi numéro 2
...
Je combats l’ennemi numéro 10
```

Quand la boucle atteint 11 :  
> “🎖️ Tous les ennemis sont vaincus. Quête terminée !”

---

## 🧮 Exemple 2 – Potion collector 🧪

```php
for ($potion = 1; $potion <= 5; $potion++) {
    echo "Je ramasse la potion numéro $potion<br>";
}
```

Résultat :
```
Je ramasse la potion numéro 1
Je ramasse la potion numéro 2
Je ramasse la potion numéro 3
Je ramasse la potion numéro 4
Je ramasse la potion numéro 5
```

💬 Et voilà, ton inventaire est plein, et PHP a tout fait **automatiquement** ! 🧳

---

## 🎮 En résumé gamer

| Élément | Dans le jeu | En PHP |
|----------|--------------|--------|
| `$i = 1` | Début de la quête | Valeur de départ |
| `$i <= 10` | Continuer jusqu’à atteindre l’objectif | Condition de fin |
| `$i++` | Passer au niveau suivant | Incrémentation |
| `for` | Répéter l’action | Boucle magique |

---

## 💬 Phrase à retenir
> La boucle `for`, c’est ton **mode “auto-farm”** :  
> tu dis à ton perso **quand commencer**, **quand s’arrêter**,  
> et il répète l’action sans jamais se fatiguer. 🧠⚔️

---

# 🧪 Exercices (niveau gamer)

### 🕹️ Exercice 1
Affiche les niveaux de 1 à 10 avec une boucle `for`. 🧩

### 💀 Exercice 2
Affiche :  
> “Je combats l’ennemi numéro X”  
pour X allant de 1 à 5.

### 🧪 Exercice 3
Affiche :  
> “Je ramasse la potion numéro X”  
pour X allant de 1 à 3.

### 🏆 Exercice 4
Affiche :  
> “Je gagne la médaille numéro X”  
pour X allant de 1 à 4.

### 🧰 Exercice 5
Affiche :  
> “J’équipe l’objet numéro X.”  
pour X allant de 1 à 6.

### ⚙️ Exercice 6
Affiche tous les nombres pairs entre 2 et 10. (Indices : pense à `$i += 2`)

### 🔙 Exercice 7
Affiche les niveaux de 10 à 1 (compte à rebours). ⏳

### 🧮 Exercice 8
Affiche la **table de multiplication de 5** façon gamer :  
> “5 x 1 = 5 XP gagnés”, etc.

### 🏰 Exercice 9
Affiche :  
> “Je nettoie la zone numéro X”  
pour X allant de 1 à 3, puis affiche :  
> “Toutes les zones sont sécurisées !” 🏁

### 🧑‍🚀 Exercice 10
Affiche ton pseudo de jeu 5 fois 😎

---

# ✅ Solutions

```php
// 1
for ($i = 1; $i <= 10; $i++) {
    echo "Niveau $i<br>";
}

// 2
for ($i = 1; $i <= 5; $i++) {
    echo "Je combats l’ennemi numéro $i<br>";
}

// 3
for ($i = 1; $i <= 3; $i++) {
    echo "Je ramasse la potion numéro $i<br>";
}

// 4
for ($i = 1; $i <= 4; $i++) {
    echo "Je gagne la médaille numéro $i<br>";
}

// 5
for ($i = 1; $i <= 6; $i++) {
    echo "J’équipe l’objet numéro $i.<br>";
}

// 6
for ($i = 2; $i <= 10; $i += 2) {
    echo "$i<br>";
}

// 7
for ($i = 10; $i >= 1; $i--) {
    echo "$i<br>";
}

// 8
for ($i = 1; $i <= 10; $i++) {
    $xp = 5 * $i;
    echo "5 x $i = $xp XP gagnés<br>";
}

// 9
for ($i = 1; $i <= 3; $i++) {
    echo "Je nettoie la zone numéro $i<br>";
}
echo "Toutes les zones sont sécurisées !<br>";

// 10
for ($i = 1; $i <= 5; $i++) {
    echo "LaurentGamer<br>";
}
```