# 🧱 Cours PHP pour Débutant – Les Tableaux Associatifs (Clés / Valeurs) 👷‍♂️

---

## 🚨 Pourquoi les tableaux sont très importants

Avant tout, arrêtons-nous un instant 👋  
Ce que tu vas apprendre ici, c’est **l’un des concepts les plus importants** de tout le PHP (et même de la programmation en général).

> Les **tableaux** sont **le cœur du code** :  
> c’est la façon de **ranger, organiser et retrouver les informations**.

Sur un chantier, tu ranges ton matériel dans des boîtes :
- une boîte pour les outils de maçonnerie,  
- une autre pour les outils de mesure,  
- une autre pour les produits (ciment, sable…).

En PHP, c’est pareil :  
➡️ Un **tableau**, c’est comme une **caisse de rangement** pour les données.

Si tu apprends à bien les utiliser :
- tu pourras **gérer plusieurs choses à la fois**,  
- **organiser** tes données sans t’y perdre,  
- et **automatiser** des calculs ou des affichages sans tout écrire à la main.

> Sans tableaux, tu devrais créer une variable pour chaque chose.  
> Avec un tableau, tu peux tout ranger au même endroit.

💬 En résumé :
> **Savoir utiliser les tableaux, c’est comme savoir utiliser tes caisses à outils.**
> Si elles sont bien rangées, ton chantier (ton code) devient simple et efficace.

---

## 👋 Introduction

Tu te souviens des **tableaux simples** ?  
C’était comme une **étagère** où chaque case avait un **numéro** :

```php
$outils = ["truelle", "niveau", "mètre"];
```

| Numéro de case (index) | Outil |
|------------------------|--------|
| 0 | truelle |
| 1 | niveau |
| 2 | mètre |

Tu devais dire à l’ordinateur :
```php
echo $outils[1];
```
Et il répondait :
```
niveau
```

Mais ce n’est pas toujours pratique, car tu dois te souvenir du **numéro** de chaque case.

---

## 🧱 Maintenant, on passe au niveau supérieur

Sur ton chantier, tu ne dis pas :
> “Apporte-moi l’outil numéro 2.”

Tu dis :
> “Apporte-moi la truelle de maçon.”  
> “Passe-moi le niveau à bulle.”

C’est exactement ce qu’on appelle un **tableau associatif** :  
au lieu d’avoir un **numéro**, chaque case a **un nom** clair.

---

## 🧰 1️⃣ Créer un tableau associatif

```php
$outils = [
    "maçonnerie" => "truelle",
    "mesure" => "niveau à bulle",
    "traçage" => "cordeau"
];
```

💬 Lis-le comme ceci :
> “Dans la boîte maçonnerie, j’ai une truelle.”

| Nom de la boîte (clé) | Contenu (valeur) |
|-----------------------|------------------|
| maçonnerie | truelle |
| mesure | niveau à bulle |
| traçage | cordeau |

---

## 🔁 2️⃣ Parcourir le tableau avec `foreach` (version simple)

Avant, ton tableau ressemblait à une liste :
```php
$outils = ["truelle", "niveau", "mètre"];
foreach ($outils as $outil) {
    echo "J’utilise un $outil<br>";
}
```

💬 Ça veut dire :
> “Pour chaque outil dans la liste, affiche son nom.”

Résultat :
```
J’utilise un truelle  
J’utilise un niveau  
J’utilise un mètre
```

---

## 🔁 3️⃣ Parcourir un tableau **avec des noms (clés)**

Maintenant, ton tableau a des **noms** :

```php
$outils = [
    "maçonnerie" => "truelle",
    "mesure" => "niveau à bulle",
    "traçage" => "cordeau"
];
```

Pour voir **le nom** et **le contenu**, tu écris :

```php
foreach ($outils as $categorie => $outil) {
    echo "Dans la catégorie $categorie, j’utilise un $outil<br>";
}
```

### 💬 Ce que ça veut dire, simplement :
> “Pour chaque boîte dans ma caisse,  
> dis-moi le **nom de la boîte** (la catégorie)  
> et **ce qu’il y a dedans** (l’outil).”

---

### 🧩 PHP fait ça dans sa tête :

| Étape | Nom de la boîte (clé) | Outil (valeur) |
|--------|------------------|----------------|
| 1️⃣ | maçonnerie | truelle |
| 2️⃣ | mesure | niveau à bulle |
| 3️⃣ | traçage | cordeau |

Et il affiche :
```
Dans la catégorie maçonnerie, j’utilise un truelle  
Dans la catégorie mesure, j’utilise un niveau à bulle  
Dans la catégorie traçage, j’utilise un cordeau
```

---

## 🔎 Comprendre la flèche `=>`

Cette flèche lit comme une phrase :
> “La clé **maçonnerie** contient la valeur **truelle**.”

ou :
> “Dans la boîte **mesure**, il y a **un niveau à bulle**.”

---

## 🧱 En résumé simple

| Avant | Maintenant |
|--------|-------------|
| `$outils = ["truelle", "niveau"];` | `$outils = ["maçonnerie" => "truelle", "mesure" => "niveau"];` |
| `foreach ($outils as $outil)` | `foreach ($outils as $categorie => $outil)` |
| Juste la valeur | Nom + valeur |
| Lecture : “truelle” | Lecture : “Dans la catégorie maçonnerie, j’utilise un truelle” |

---

### 🧱 Phrase à retenir :
> Un **tableau**, c’est comme une **caisse de chantier**.  
> Chaque boîte a **un nom (clé)** et **un contenu (valeur)**.  
> Le `foreach` te permet de **regarder dans chaque boîte** sans tout ouvrir à la main.

---

# 🧪 Exercices (niveau débutant)

### Exercice 1
Crée un tableau `$materiaux` avec :  
- ciment → 8  
- sable → 6  
- gravier → 10  
et affiche le prix du ciment.

---

### Exercice 2
Ajoute `"brique" => 12` au tableau `$materiaux`.

---

### Exercice 3
Change le prix du sable à 7 et affiche à nouveau le tableau.

---

### Exercice 4
Crée un tableau `$clients` :  
- Dupont → “devis signé”  
- Martin → “en attente”  
- Durand → “terminé”  
et affiche chaque client et son état.

---

### Exercice 5
Ajoute un client “Bernard” → “nouveau”.

---

### Exercice 6
Crée un tableau `$outils` :  
- truelle → “maçonnerie”  
- scie → “béton cellulaire”  
- cordeau → “traçage”  
et affiche :
> “L’outil [nom] sert pour la [catégorie].”

---

### Exercice 7
Compte combien d’éléments contient ton tableau `$outils`.

---

### Exercice 8
Crée un tableau `$prix` :  
- ciment → 8  
- sable → 6  
- gravier → 10  
et calcule la somme totale des prix avec `foreach`.

---

### Exercice 9
Crée un tableau `$stock` :  
- briques → 120  
- sacs de ciment → 15  
- seaux → 8  
et affiche :
> “J’ai [nombre] [objet].”

---

### Exercice 10
Crée un tableau `$chantier` :  
- client → “Dupont”  
- surface → 80  
- prix_m2 → 40  
et affiche :
> “Le devis pour Dupont est de 3200 euros.”

---

## ✅ Solutions

```php
// 1
$materiaux = ["ciment" => 8, "sable" => 6, "gravier" => 10];
echo $materiaux["ciment"];

// 2
$materiaux["brique"] = 12;

// 3
$materiaux["sable"] = 7;
foreach ($materiaux as $nom => $prix) {
    echo "$nom coûte $prix euros<br>";
}

// 4
$clients = ["Dupont" => "devis signé", "Martin" => "en attente", "Durand" => "terminé"];
foreach ($clients as $nom => $etat) {
    echo "Client $nom : $etat<br>";
}

// 5
$clients["Bernard"] = "nouveau";

// 6
$outils = ["truelle" => "maçonnerie", "scie" => "béton cellulaire", "cordeau" => "traçage"];
foreach ($outils as $outil => $categorie) {
    echo "L’outil $outil sert pour la $categorie.<br>";
}

// 7
echo "Nombre d’outils : " . count($outils);

// 8
$prix = ["ciment" => 8, "sable" => 6, "gravier" => 10];
$total = 0;
foreach ($prix as $valeur) {
    $total += $valeur;
}
echo "Total : $total euros";

// 9
$stock = ["briques" => 120, "sacs de ciment" => 15, "seaux" => 8];
foreach ($stock as $objet => $quantite) {
    echo "J’ai $quantite $objet.<br>";
}

// 10
$chantier = ["client" => "Dupont", "surface" => 80, "prix_m2" => 40];
$total = $chantier["surface"] * $chantier["prix_m2"];
echo "Le devis pour " . $chantier["client"] . " est de $total euros.";
```
