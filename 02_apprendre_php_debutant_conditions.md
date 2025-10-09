# 🧱 Cours PHP Débutant – Comprendre `true`, `false`, `if`, `else`, `elseif`, et les conditions `&&` et `||` 👷‍♂️💡

---

## 👋 Introduction

Sur un chantier, tu dois souvent **prendre des décisions** :

> “S’il pleut, je reste à la maison.”  
> “S’il fait beau, je travaille.”  
> “Et s’il fait trop froid, j’attends un peu.”

Eh bien, en PHP, ton ordinateur apprend à faire pareil !  
Il réfléchit avec **oui** (`true`) et **non** (`false`).  

---

## 💡 1️⃣ `true` et `false` – les interrupteurs du code

Imagine ton chantier avec un interrupteur :

| Position | Valeur | Signification |
|-----------|---------|----------------|
| 🔆 Allumé | `true` | Oui, c’est vrai ✅ |
| 🌑 Éteint | `false` | Non, c’est faux ❌ |

Ton ordinateur ne comprend que deux états :  
**`true`** = oui, **`false`** = non.  

---

## 🌧️ Exemple concret

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
> “S’il pleut, je reste à la maison.”

---

## ☀️ 3️⃣ `else` veut dire “SINON”

Et s’il ne pleut pas ?

```php
$pluie = false;

if ($pluie) {
    echo "Il pleut, je reste à la maison.";
} else {
    echo "Il ne pleut pas, je vais sur le chantier.";
}
```

💬 PHP lit :
> “Est-ce qu’il pleut ? Non ❌  → Je vais sur le chantier.”

---

## 🌡️ 4️⃣ `elseif` veut dire “SINON SI”

Parfois, il y a **plusieurs cas possibles** :

> “S’il fait très froid, j’arrête.”  
> “Sinon, s’il fait un peu froid, je fais attention.”  
> “Sinon, je travaille.”

```php
$temperature = 3;

if ($temperature < 0) {
    echo "Trop froid, on arrête.";
} elseif ($temperature < 5) {
    echo "Froid, on fait attention.";
} else {
    echo "Bonne température, on travaille !";
}
```

💬 PHP lit :  
> “Si < 0 → j’arrête.”  
> “Sinon si < 5 → je fais attention.”  
> “Sinon → je bosse.”

---

## 🤝 5️⃣ Le `&&` veut dire **ET**

Le mot `&&` se lit **“et”**.  
Tu t’en sers quand tu veux que **deux choses soient vraies en même temps**.

> “Je peux monter le mur **si j’ai des briques ET du mortier**.”

```php
$briques = true;
$mortier = true;

if ($briques && $mortier) {
    echo "On peut monter le mur !";
} else {
    echo "Il manque quelque chose.";
}
```

| Situation | Résultat |
|------------|-----------|
| Briques ✅ et mortier ✅ | On travaille |
| Briques ✅ mais pas de mortier ❌ | Il manque du mortier |
| Pas de briques ❌ et mortier ✅ | Il manque les briques |
| Rien du tout ❌ | Rien ne va 😅 |

🧱 En clair :
> Avec **ET (`&&`)**, les **deux** doivent être vraies.

---

## 🔸 6️⃣ Le `||` veut dire **OU**

Le mot `||` se lit **“ou”**.  
Il sert quand **une seule condition suffit**.

> “Je reste à la maison **s’il pleut OU s’il y a du vent**.”

```php
$pluie = true;
$vent = false;

if ($pluie || $vent) {
    echo "On ne peut pas travailler aujourd'hui.";
} else {
    echo "Conditions parfaites, on bosse !";
}
```

| Situation | Résultat |
|------------|-----------|
| Il pleut | ✅ On arrête |
| Il y a du vent | ✅ On arrête |
| Il pleut et il y a du vent | ✅ On arrête |
| Pas de pluie et pas de vent | ❌ On bosse |

🧠 En clair :
> Avec **OU (`||`)**, **une seule** condition suffit.

---

## 👷‍♂️ 7️⃣ Autres exemples du chantier

### Exemple 1 :
> “Je mets ma veste **s’il pleut OU s’il fait froid**.”

```php
$pluie = false;
$froid = true;

if ($pluie || $froid) {
    echo "Je mets ma veste.";
} else {
    echo "Pas besoin de veste.";
}
```

### Exemple 2 :
> “Je fais une pause **si j’ai faim OU si je suis fatigué**.”

```php
$faim = true;
$fatigue = false;

if ($faim || $fatigue) {
    echo "On fait une pause !";
} else {
    echo "On continue à bosser.";
}
```

---

## 🧠 8️⃣ Résumé du chef

| Signe | Mot | Signifie | Exemple concret |
|--------|-----|-----------|----------------|
| `&&` | ET | Les deux conditions doivent être vraies | “J’ai des briques **et** du mortier.” |
| `||` | OU | Une seule condition suffit | “Il pleut **ou** il y a du vent.” |
| `if` | Si c’est vrai | “S’il pleut…” |
| `else` | Sinon | “Sinon, je bosse.” |
| `elseif` | Sinon si... | “Sinon, s’il fait froid…” |

---

## 🧰 Conseil du chef 👷‍♂️

🧠 Pour comprendre plus facilement :
- **Lis ton code comme une phrase.**
- **Remplace `&&` par “et” et `||` par “ou”.**
- Ne t’inquiète pas si ça paraît bizarre au début :  
  ➡️ Comme pour le français, plus tu pratiques, plus ça devient naturel !

---

## 🚀 Pour plus tard

Tu utiliseras ces conditions partout :  
dans des jeux 🎮, des sites web 🌐, ou même des applications mobiles 📱.  
C’est la **base de toute la logique informatique** 💪  
