# 🧱 Exercices PHP – Pratique pour le Maçon Débutant 👷‍♂️

Ces exercices t’aideront à bien comprendre chaque notion du cours.  
Prends ton temps, et fais-les dans l’ordre.  
Chaque petit bout de code doit être tapé dans un fichier `.php` (ex : `exercice1.php`), puis ouvert dans ton navigateur avec XAMPP ou WAMP.

---

## 🔹 Exercice 1 – Présente-toi

**But :** utiliser les variables.

Crée trois variables :
- `$nom` → ton prénom,
- `$metier` → ton ancien métier,
- `$ville` → la ville où tu travailles.

Affiche une phrase avec `echo` :

> “Je m’appelle [nom], j’étais [métier] et je travaillais à [ville].”

💡 *Indice : utilise les points `.` pour coller les mots si besoin.*

---

## 🔹 Exercice 2 – Le temps de travail

**But :** apprendre les conditions `if` et `else`.

Crée une variable `$pluie = true;`

Si `$pluie` est vraie, affiche :  
> “Il pleut, je reste à la maison.”

Sinon, affiche :  
> “Pas de pluie, je pars travailler sur le chantier.”

💡 *Rappelle-toi : `true` = oui, `false` = non.*

---

## 🔹 Exercice 3 – Température du chantier

**But :** conditions avec comparaison.

Crée une variable `$temperature = 3;`

Si la température est inférieure à 5, affiche :  
> “Il fait trop froid pour couler le béton.”

Sinon, affiche :  
> “La température est bonne, on peut travailler.”

💡 *Tu peux utiliser `<` pour “plus petit que”.*

---

## 🔹 Exercice 4 – Calcul de la surface d’un mur

**But :** utiliser les variables et le calcul.

Crée deux variables :
```php
$longueur = 5;
$hauteur = 2.5;
```

Calcule la surface (`$surface = $longueur * $hauteur;`)  
et affiche :

> “La surface du mur est de [résultat] m².”

💡 *Pense à bien utiliser `*` pour la multiplication.*

---

## 🔹 Exercice 5 – Poser les briques

**But :** apprendre la boucle `for`.

Affiche :

```
Je pose la brique numéro 1
Je pose la brique numéro 2
...
Je pose la brique numéro 10
```

💡 *Commence à 1 et termine à 10.*

---

## 🔹 Exercice 6 – Les sacs de ciment

**But :** créer une fonction simple.

Crée une fonction `afficherSacs()` qui affiche :  
> “J’ai besoin de 5 sacs de ciment pour ce mur.”

Appelle la fonction 1 fois.

💡 *Aucune variable nécessaire, le but est juste d’utiliser `function` et `()`.*

---

## 🔹 Exercice 7 – Le devis du mur

**But :** fonction avec paramètres.

Crée une fonction `calculerDevis($surface, $prix_m2)`  
qui affiche le prix total du chantier (surface × prix).

Teste-la avec plusieurs valeurs :
- 10 m² à 40 €/m²  
- 20 m² à 35 €/m²

💡 *Les nombres se passent entre parenthèses quand tu appelles la fonction.*

---

## 🔹 Exercice 8 – Liste de clients

**But :** découvrir la boucle `foreach`.

Crée un tableau :
```php
$clients = ["Dupont", "Martin", "Durand"];
```

Avec une boucle `foreach`, affiche :
> “J’appelle le client [nom].”

💡 *`foreach ($clients as $client)` te permet de parcourir la liste.*

---

## 🔹 Exercice 9 – Appel et devis

**But :** combiner fonction et `foreach`.

1. Crée un tableau :
   ```php
   $clients = ["Dupont", "Martin", "Durand"];
   ```
2. Crée une fonction `saluer($nom)` qui affiche :
   > “Bonjour $nom, votre devis est prêt.”
3. Utilise `foreach` pour appeler la fonction pour chaque client.

💡 *C’est ton premier “chantier complet” en PHP !*

---

## 🔹 Exercice 10 – Le mur parfait

**But :** tout réunir (variables, boucles, fonctions, conditions).

Crée un script qui :

1. Définit une longueur et une hauteur.  
2. Calcule la surface.  
3. Si la surface est inférieure à 5 m² → affiche “Petit mur.”  
   Sinon → affiche “Beau mur, bon travail !”  
4. Fais une boucle `for` qui affiche combien de briques tu poses.  
5. Termine par une fonction `feliciter()` qui affiche :
   > “Le mur est terminé, félicitations chef !”

💡 *Cet exercice rassemble tout ce que tu as appris.*

---

# ✅ Solutions des exercices

## Solution 1

```php
$nom = "Jean";
$metier = "maçon";
$ville = "Toulon";

echo "Je m'appelle $nom, j'étais $metier et je travaillais à $ville.";
```

---

## Solution 2

```php
$pluie = true;

if ($pluie) {
    echo "Il pleut, je reste à la maison.";
} else {
    echo "Pas de pluie, je pars travailler sur le chantier.";
}
```

---

## Solution 3

```php
$temperature = 3;

if ($temperature < 5) {
    echo "Il fait trop froid pour couler le béton.";
} else {
    echo "La température est bonne, on peut travailler.";
}
```

---

## Solution 4

```php
$longueur = 5;
$hauteur = 2.5;

$surface = $longueur * $hauteur;
echo "La surface du mur est de $surface m².";
```

---

## Solution 5

```php
for ($i = 1; $i <= 10; $i++) {
    echo "Je pose la brique numéro $i<br>";
}
```

---

## Solution 6

```php
function afficherSacs() {
    echo "J’ai besoin de 5 sacs de ciment pour ce mur.";
}

afficherSacs();
```

---

## Solution 7

```php
function calculerDevis($surface, $prix_m2) {
    $total = $surface * $prix_m2;
    echo "Le devis est de $total euros.<br>";
}

calculerDevis(10, 40);
calculerDevis(20, 35);
```

---

## Solution 8

```php
$clients = ["Dupont", "Martin", "Durand"];

foreach ($clients as $client) {
    echo "J'appelle le client $client<br>";
}
```

---

## Solution 9

```php
$clients = ["Dupont", "Martin", "Durand"];

function saluer($nom) {
    echo "Bonjour $nom, votre devis est prêt.<br>";
}

foreach ($clients as $client) {
    saluer($client);
}
```

---

## Solution 10

```php
$longueur = 2;
$hauteur = 3;

$surface = $longueur * $hauteur;

if ($surface < 5) {
    echo "Petit mur.<br>";
} else {
    echo "Beau mur, bon travail !<br>";
}

for ($i = 1; $i <= 10; $i++) {
    echo "Je pose la brique numéro $i<br>";
}

function feliciter() {
    echo "Le mur est terminé, félicitations chef !";
}

feliciter();
```
