# 🧱 Cours PHP pour Débutant – Les Conditions `if`, `else`, `elseif` 👷‍♂️

## 👋 Introduction

Sur un chantier, tu prends souvent des décisions :

> “S’il pleut, je ne travaille pas.”  
> “S’il fait beau, je travaille.”  
> “Et s’il fait trop froid, j’attends un peu.”

En PHP, on apprend à faire **la même chose** avec des mots simples :  
`if`, `else`, et `elseif`.

---

## 🧱 1️⃣ Le mot `if` veut dire “SI”

En PHP, `if` veut dire **“si”**.  
On s’en sert pour dire à l’ordinateur :
> “Si quelque chose est vrai, fais ça.”

Exemple :

```php
$pluie = true;

if ($pluie) {
    echo "Il pleut, je reste à la maison.";
}
```

### 💬 Explication :
- `$pluie = true;` veut dire **“oui, il pleut.”**
- `if ($pluie)` veut dire **“si c’est vrai qu’il pleut...”**
- Alors, l’ordinateur exécute ce qu’il y a entre les `{ }`.

Tu peux lire ce code comme une phrase :  
> “S’il pleut, alors je reste à la maison.”

---

## ☀️ 2️⃣ Le mot `else` veut dire “SINON”

Et s’il ne pleut pas ?  
Tu veux faire autre chose. C’est là que `else` sert.

```php
$pluie = false;

if ($pluie) {
    echo "Il pleut, je reste à la maison.";
} else {
    echo "Il ne pleut pas, je vais sur le chantier.";
}
```

### 💬 Ce que fait PHP :
- `$pluie = false` → non, il ne pleut pas.
- Le test `if ($pluie)` est **faux**.
- Donc PHP passe au `else` et affiche :  
  > “Il ne pleut pas, je vais sur le chantier.”

🧱 Comme toi :
> “S’il pleut → je rentre.”  
> “Sinon → je bosse.”

---

## 🌡️ 3️⃣ Le mot `elseif` veut dire “SINON SI”

Il y a parfois **plus de deux choix**.

> “S’il fait trop froid, j’arrête.”  
> “Sinon, s’il fait un peu froid, je fais attention.”  
> “Sinon, je travaille normalement.”

En PHP :
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

### 💬 Explication :
- `if` → premier test  
- `elseif` → deuxième test si le premier est faux  
- `else` → tout le reste

Lis-le comme une phrase :  
> “Si température < 0 → j’arrête.”  
> “Sinon si < 5 → je fais attention.”  
> “Sinon → je travaille.”

---

## ⚙️ 4️⃣ Les symboles de comparaison

| Signe | Signifie | Exemple | Lecture chantier |
|--------|-----------|-----------|------------------|
| `==` | est égal à | `$pluie == true` | “Il pleut ?” |
| `!=` | est différent de | `$pluie != true` | “Il ne pleut pas ?” |
| `<` | plus petit que | `$temperature < 5` | “Température en dessous de 5 ?” |
| `>` | plus grand que | `$surface > 10` | “Surface au-dessus de 10 ?” |
| `<=` | plus petit ou égal | `$prix <= 40` | “Prix de 40 ou moins ?” |
| `>=` | plus grand ou égal | `$briques >= 100` | “Assez de briques ?” |

---

## 🔩 5️⃣ Plusieurs conditions à la fois

Sur un chantier, tu peux dire :  
> “Je travaille **s’il ne pleut pas** et **si j’ai du ciment**.”

En PHP :
```php
$pluie = false;
$ciment = true;

if (!$pluie && $ciment) {
    echo "On peut travailler.";
} else {
    echo "Pas possible aujourd'hui.";
}
```

### 💬 Explications :
- `&&` veut dire **ET** → les deux doivent être vrais.  
- `||` veut dire **OU** → au moins un est vrai.  
- `!` veut dire **PAS** → `!$pluie` = “il ne pleut pas”.

🧱 Exemple concret :
> “Pas de pluie **ET** j’ai du ciment → je travaille.”  
> “Sinon → je reste.”

---

## 👷‍♂️ 6️⃣ Erreurs fréquentes

| Erreur | Pourquoi | Solution |
|---------|-----------|-----------|
| Utiliser `=` au lieu de `==` | `=` donne une valeur, `==` compare | Utilise `==` pour tester |
| Oublier les `{ }` | PHP ne sait plus quoi exécuter | Mets-les toujours après `if` et `else` |
| Oublier `;` | Chaque ligne se termine par un point-virgule | Relis ton code lentement |
| Code non aligné | On s’y perd vite | Aligne ton code, comme un mur droit 🧱 |

---

## 🧱 7️⃣ Exemple complet

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
1. “Il pleut ?” → non  
2. “Il fait froid ?” → oui → “Froid, on fait attention.”  
✅ PHP s’arrête là.

---

## 🧰 8️⃣ Résumé du chef

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

## 🧪 9️⃣ Exercices simples

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
