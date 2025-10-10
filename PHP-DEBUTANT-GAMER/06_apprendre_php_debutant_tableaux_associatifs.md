# 🎮 Cours PHP pour Débutant – Les Tableaux Associatifs (Clés / Valeurs) 🗝️🎒

---

## 🚨 Pourquoi les tableaux sont vitaux pour un gamer

Les **tableaux** sont au code ce que l’**inventaire** est à un RPG :  
la manière d’**organiser, retrouver et utiliser** toutes tes ressources sans te perdre.

> Sans tableaux, tu aurais une variable par objet.  
> Avec un tableau, tu ranges **tout au même endroit** — propre et efficace.

Si tu maîtrises ça, tu pourras :  
- gérer **plein d’infos** (stats, loot, quêtes) d’un coup,  
- **organiser** tes données comme un inventaire trié,  
- **automatiser** des affichages/calculs sans copier-coller.

---

## 👋 Introduction

Tu connais les **tableaux simples** (indexés) : une **liste** numérotée 0, 1, 2…

```php
$inventaire = ["épée", "bouclier", "potion"];
```

| Slot (index) | Objet |
|--------------|-------|
| 0 | épée |
| 1 | bouclier |
| 2 | potion |

Pour afficher :
```php
echo $inventaire[1]; // bouclier
```

Mais se souvenir des **numéros** de slots, c’est pas toujours fun…

---

## ⚡ Passons au niveau supérieur : les **tableaux associatifs**

Dans un jeu, tu ne dis pas : “Donne-moi l’objet **slot 2**.”  
Tu dis : “Donne-moi ma **potion de soin**.”

Un **tableau associatif**, c’est un inventaire **par étiquettes** :  
chaque case a un **nom (clé)** au lieu d’un numéro.

---

## 🧰 1️⃣ Créer un tableau associatif

```php
$stuff = [
    "arme" => "épée légendaire",
    "defense" => "bouclier de fer",
    "soin" => "potion"
];
```

Lis-le comme :  
> “Dans la case **arme**, j’ai **épée légendaire**.”

| Clé (nom de case) | Valeur (contenu) |
|-------------------|------------------|
| arme | épée légendaire |
| defense | bouclier de fer |
| soin | potion |

---

## 🔁 2️⃣ Parcourir un tableau associatif avec `foreach`

```php
foreach ($stuff as $categorie => $objet) {
    echo "Dans $categorie, j’utilise $objet<br>";
}
```

Ce que PHP fait :  
- `$categorie` reçoit la **clé** (arme/defense/soin)  
- `$objet` reçoit la **valeur** (épée, bouclier, potion)

Affichage (exemple) :
```
Dans arme, j’utilise épée légendaire
Dans defense, j’utilise bouclier de fer
Dans soin, j’utilise potion
```

---

## 🏷️ 3️⃣ Comprendre la flèche `=>`

On la lit comme :  
> “**clé** ⇒ **valeur**”  
> “**soin** ⇒ **potion**” (= dans la case ‘soin’, tu ranges ‘potion’).

---

## 🛠️ 4️⃣ Accéder / Ajouter / Modifier

### Accéder à un élément par sa **clé**
```php
echo $stuff["arme"]; // épée légendaire
```

### Ajouter un nouvel élément
```php
$stuff["anneau"] = "anneau magique";
```

### Modifier un élément existant
```php
$stuff["soin"] = "méga potion";
```

---

## 📊 5️⃣ Compter les éléments avec `count()`
```php
echo count($stuff); // 4 si tu as ajouté l'anneau
```

---

## 🧪 6️⃣ Exemple complet (mini-RPG)

```php
$stuff = [
    "arme" => "épée légendaire",
    "defense" => "bouclier de fer",
    "soin" => "potion"
];

// J'obtiens un artefact
$stuff["anneau"] = "anneau magique";

// J'améliore ma potion
$stuff["soin"] = "méga potion";

// J'affiche mon inventaire détaillé
foreach ($stuff as $slot => $objet) {
    echo ucfirst($slot) . " : $objet<br>";
}

// Nombre total de slots
echo "Slots utilisés : " . count($stuff);
```

Résultat (exemple) :
```
Arme : épée légendaire
Defense : bouclier de fer
Soin : méga potion
Anneau : anneau magique
Slots utilisés : 4
```

---

## 🧭 7️⃣ Quand utiliser associatif vs indexé ?

| Besoin | Tableau indexé | Tableau associatif |
|-------|------------------|--------------------|
| Liste ordonnée (loot, checkpoints) | ✅ | – |
| Accès par **nom** (stats, slots, paramètres) | – | ✅ |
| Lecture humaine (“PV”, “mana”, “attaque”) | – | ✅ |

---

## 🧩 8️⃣ Résumé gamer

| Code | Signification | Exemple |
|------|---------------|---------|
| `["clé" => "valeur"]` | Case nommée | `["soin" => "potion"]` |
| `$tab["clé"]` | Accéder par nom | `$stuff["arme"]` |
| `$tab["clé"] = x` | Ajouter/Modifier | `$stuff["anneau"] = "magique"` |
| `foreach ($t as $k => $v)` | Parcourt clé + valeur | `slot + objet` |
| `count($t)` | Nombre de cases | `count($stuff)` |

> Un **tableau associatif**, c’est ton **inventaire étiqueté**. Tu pioches par **nom**, pas par numéro. GG. 🏆

---

# 🧪 Exercices (niveau gamer)

### Exercice 1
Crée `$stats = ["pv" => 100, "mana" => 50, "attaque" => 20];`  
Affiche les **PV**.

---

### Exercice 2
Ajoute `"defense" => 15` à `$stats`.

---

### Exercice 3
Augmente `"mana"` à `80` et réaffiche toutes les stats.

---

### Exercice 4
Crée `$quetes = ["prologue" => "Réveiller le héros", "acte1" => "Trouver l’épée", "acte2" => "Sauver la ville"];`  
Affiche chaque **chapitre** et sa **description**.

---

### Exercice 5
Ajoute `"acte3" => "Vaincre le boss"`.

---

### Exercice 6
Crée `$skills = ["feu" => "Boule de feu", "glace" => "Éclat de givre", "foudre" => "Éclair"];`  
Affiche :  
> “La compétence [clé] lance [valeur].”

---

### Exercice 7
Compte le nombre de compétences dans `$skills`.

---

### Exercice 8
Crée `$prix = ["potion" => 25, "ether" => 30, "elixir" => 100];`  
Calcule la **somme totale** avec `foreach`.

---

### Exercice 9
Crée `$inventaire = ["or" => 250, "gemmes" => 3, "clés" => 2];`  
Affiche :  
> “Tu possèdes [nombre] [objet].”

---

### Exercice 10
Crée `$perso = ["nom" => "Link", "niveau" => 12, "classe" => "Héros"];`  
Affiche :
> “Le héros Link (niveau 12) part à l’aventure.”

---

## ✅ Solutions

```php
// 1
$stats = ["pv" => 100, "mana" => 50, "attaque" => 20];
echo $stats["pv"];

// 2
$stats["defense"] = 15;

// 3
$stats["mana"] = 80;
foreach ($stats as $k => $v) {
    echo ucfirst($k) . " : $v<br>";
}

// 4
$quetes = ["prologue" => "Réveiller le héros", "acte1" => "Trouver l’épée", "acte2" => "Sauver la ville"];
foreach ($quetes as $chap => $desc) {
    echo "Chapitre $chap : $desc<br>";
}

// 5
$quetes["acte3"] = "Vaincre le boss";

// 6
$skills = ["feu" => "Boule de feu", "glace" => "Éclat de givre", "foudre" => "Éclair"];
foreach ($skills as $elem => $sort) {
    echo "La compétence $elem lance $sort.<br>";
}

// 7
echo "Nombre de compétences : " . count($skills);

// 8
$prix = ["potion" => 25, "ether" => 30, "elixir" => 100];
$total = 0;
foreach ($prix as $val) { $total += $val; }
echo "Total boutique : $total or";

// 9
$inventaire = ["or" => 250, "gemmes" => 3, "clés" => 2];
foreach ($inventaire as $objet => $nb) {
    echo "Tu possèdes $nb $objet.<br>";
}

// 10
$perso = ["nom" => "Link", "niveau" => 12, "classe" => "Héros"];
echo "Le héros " . $perso["nom"] . " (niveau " . $perso["niveau"] . ") part à l’aventure.";
```