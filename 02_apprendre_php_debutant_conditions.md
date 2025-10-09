# 🧱 Cours PHP Débutant – Comprendre `true`, `false` et les Conditions `if`, `else`, `elseif` 👷‍♂️💡

---

## 👋 Introduction

Sur un chantier, tu prends des décisions tous les jours :  

> “S’il pleut, je ne travaille pas.”  
> “S’il fait beau, je travaille.”  
> “Et s’il fait trop froid, j’attends un peu.”

Eh bien en PHP, c’est **pareil** !  
Tu apprends à faire réfléchir ton ordinateur avec des **“oui”** et des **“non”**.

Et ces deux petits mots magiques sont :

```php
true  // oui, c’est vrai ✅
false // non, c’est faux ❌
```

---

## 💡 1️⃣ `true` et `false` – les interrupteurs du code

### ⚙️ Imagine ton chantier
Tu as un **interrupteur** dans ta cabane :

| Position | Valeur | Signification |
|-----------|---------|----------------|
| 🔆 Allumé | `true` | Oui, c’est vrai ✅ |
| 🌑 Éteint | `false` | Non, c’est faux ❌ |

Ton ordinateur ne connaît pas les “peut-être” 😅  
Pour lui, **tout est soit vrai, soit faux**.  
C’est un peu comme ton niveau à bulle : il est **droit** ✅ ou **pas droit** ❌ — y’a pas d’entre-deux.

---

## 🌦️ Exemple concret

```php
$pluie = true;
```

💬 Ça veut dire : “Oui, il pleut.”

```php
$pluie = false;
```

💬 Ça veut dire : “Non, il ne pleut pas.”

---

## 🧱 2️⃣ Le mot `if` veut dire “SI”

> “Si quelque chose est vrai, fais ça.”

```php
$pluie = true;

if ($pluie) {
    echo "Il pleut, je reste à la maison.";
}
```

💬 Lis-le comme une phrase :
> “S’il pleut, alors je reste à la maison.”

---

## ☀️ 3️⃣ Le mot `else` veut dire “SINON”

Et s’il ne pleut pas ? On fait autre chose.

```php
$pluie = false;

if ($pluie) {
    echo "Il pleut, je reste à la maison.";
} else {
    echo "Il ne pleut pas, je vais sur le chantier.";
}
```

💬 PHP regarde :
- `$pluie = false` → faux ❌  
- donc il passe au `else` → “Il ne pleut pas, je vais sur le chantier.”

---

## 🌡️ 4️⃣ Le mot `elseif` veut dire “SINON SI”

Parfois il y a **plusieurs situations possibles** :

> “S’il fait trop froid, j’arrête.”  
> “Sinon s’il fait un peu froid, je fais attention.”  
> “Sinon, je bosse.”

```php
$temperature = 3;

if ($temperature < 0) {
    echo "Trop froid, on arrête.";
} elseif ($temperature < 5) {
    echo "Froid, on fait attention.";
} else {
    echo "Bonne température, on peut travailler.";
}
```

💬 PHP lit :
> “Si < 0 → j’arrête.”  
> “Sinon si < 5 → je fais attention.”  
> “Sinon → je bosse.”

---

## ⚙️ 5️⃣ Les symboles de comparaison

| Signe | Signifie | Exemple | Lecture chantier |
|--------|-----------|-----------|------------------|
| `==` | est égal à | `$pluie == true` | “Il pleut ?” |
| `!=` | est différent de | `$pluie != true` | “Il ne pleut pas ?” |
| `<` | plus petit que | `$temperature < 5` | “Température en dessous de 5 ?” |
| `>` | plus grand que | `$surface > 10` | “Surface au-dessus de 10 ?” |
| `<=` | plus petit ou égal | `$prix <= 40` | “Prix de 40 ou moins ?” |
| `>=` | plus grand ou égal | `$briques >= 100` | “Assez de briques ?” |

---

## 🔩 6️⃣ Plusieurs conditions à la fois

> “Je travaille s’il **ne pleut pas** ET si **j’ai du ciment**.”

```php
$pluie = false;
$ciment = true;

if (!$pluie && $ciment) {
    echo "On peut travailler.";
} else {
    echo "Pas possible aujourd'hui.";
}
```

💬  
- `&&` → **ET**  
- `||` → **OU**  
- `!` → **PAS**

---

## 🚧 7️⃣ Erreurs fréquentes

| Erreur | Pourquoi | Solution |
|---------|-----------|-----------|
| Utiliser `=` au lieu de `==` | `=` donne une valeur, `==` compare | Utilise `==` pour tester |
| Oublier les `{ }` | PHP ne sait plus quoi exécuter | Mets-les toujours |
| Oublier `;` | Chaque ligne se termine par un point-virgule | Sois précis |
| Code mal aligné | On s’y perd vite | Garde ton mur droit 🧱 |

---

## 💪 8️⃣ Exemple complet

```php
$pluie = false;
$temperature = 3;
$ciment = true;

if ($pluie) {
    echo "Il pleut, on reste.";
} elseif ($temperature < 5) {
    echo "Froid, on fait attention.";
} elseif (!$ciment) {
    echo "Pas de ciment, on attend la livraison.";
} else {
    echo "Tout est bon, on travaille !";
}
```

💬 Lecture :
> 1️⃣ “Il pleut ?” → non  
> 2️⃣ “Il fait froid ?” → oui → “Froid, on fait attention.”  
✅ PHP s’arrête là.

---

## 🧱 9️⃣ Résumé du chef

| Mot / Signe | Signifie | Exemple concret |
|--------------|-----------|------------------|
| `if` | Si c’est vrai | “S’il pleut” |
| `else` | Sinon | “Sinon je travaille” |
| `elseif` | Sinon si... | “Sinon, s’il fait froid” |
| `true` | Oui | “Oui, il pleut” |
| `false` | Non | “Non, il ne pleut pas” |
| `&&` | ET | “S’il fait beau **et** j’ai du ciment” |
| `||` | OU | “S’il pleut **ou** il fait froid” |
| `!` | PAS | “S’il **ne** pleut **pas**” |

---

## 🧪 🔟 Exercices simples

Fais ces petits exercices un par un.

### Exercice 1
```php
$casque = false;
```
➡️ Si `$casque` est vrai → “Tu es prêt.”  
Sinon → “Mets ton casque.”

---

### Exercice 2
```php
$temperature = 2;
```
➡️ Si `< 0` → “On arrête.”  
Sinon si `< 5` → “On fait attention.”  
Sinon → “Tout va bien.”

---

### Exercice 3
```php
$pluie = true;
$ciment = false;
```
➡️ Si pluie **ou** pas de ciment → “Pas possible.”  
Sinon → “On bosse.”

---

### Exercice 4
```php
$sacs = 7;
```
➡️ Si >= 10 → “Stock parfait.”  
Sinon si >= 5 → “Ça passe.”  
Sinon → “Pas assez de sacs.”

---

### Exercice 5
```php
$vent = false;
$pluie = false;
```
➡️ Si pluie ou vent → “On reporte.”  
Sinon → “On peut monter l’échafaudage.”

---

### Exercice 6
```php
$temperature = -1;
$pluie = false;
```
➡️ Si < 0 → “Gel, on stoppe.”  
Sinon si pluie = true → “On reporte.”  
Sinon → “Conditions OK.”

---

### Exercice 7
```php
$surface = 10;
$prix_m2 = 45;
```
➡️ Calcule `$total = $surface * $prix_m2;`  
Si > 500 → “Gros chantier.”  
Sinon → “Petit chantier.”

---

### Exercice 8
```php
$pluie = false;
$casque = true;
$gants = true;
```
➡️ Si pas de pluie **et** casque **et** gants → “Tu peux travailler.”  
Sinon → “Pas prêt.”

---

### Exercice 9
```php
$jour = "dimanche";
```
➡️ Si lundi → “Début de semaine.”  
Sinon si vendredi → “Fin de semaine.”  
Sinon si dimanche → “Repos du guerrier.”  
Sinon → “Journée normale.”

---

### Exercice 10
```php
$pluie = false;
$temperature = 8;
$ciment = true;
$casque = true;
```
➡️ Si pluie → “On reporte.”  
Sinon si < 5 → “Trop froid.”  
Sinon si pas de ciment → “Pas de ciment.”  
Sinon si pas de casque → “Pas de casque.”  
Sinon → “Tout est prêt, on attaque le chantier !”
