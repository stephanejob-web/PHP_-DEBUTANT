# 🧱 Apprendre le PHP – Leçon du Maçon Débutant 👷‍♂️

Salut à toi, futur pro du code !  
Tu vas apprendre à parler à ton ordinateur **comme tu parlerais à ton apprenti** sur un chantier.  
PHP, c’est ton **apprenti numérique** : si tu lui expliques bien, il fait le travail à ta place.

---

## 1️⃣ Les variables – tes seaux de chantier 🪣

Une **variable**, c’est comme un **seau** dans lequel tu ranges quelque chose : du sable, du ciment ou un nombre.  
Tu écris toujours un `$` devant le nom de ta variable (comme si tu mettais ton nom sur ton seau).

Exemple :

```php
$nombre_de_briques = 120;
$nom_client = "Dupont";
```

👉 `$nombre_de_briques` = ton seau contient **120 briques**  
👉 `$nom_client` = ton seau contient **le mot “Dupont”**

Tu peux ensuite dire à ton apprenti (l’ordinateur) :

```php
echo $nom_client;
```

Et il te répondra :  
**Dupont**

---

## 2️⃣ Les conditions `if` et `else` – décider comme sur un chantier 🌦️

Une **condition**, c’est quand tu dois **prendre une décision**.

> “S’il pleut, je rentre à la maison. Sinon, je travaille.”

En PHP :

```php
$pluie = true;

if ($pluie) {
    echo "Je reste à la maison.";
} else {
    echo "Je vais sur le chantier.";
}
```

### ☔ Comprendre `true` et `false`

Imagine que tu demandes à ton apprenti :

> “Est-ce qu’il pleut ?”

- **`true`** → c’est comme s’il te disait **“Oui chef !”**  
- **`false`** → c’est comme s’il te disait **“Non chef !”**

En résumé :

| Mot | Signification |
|------|----------------|
| `true` | Oui, c’est vrai ✅ |
| `false` | Non, c’est faux ❌ |

Exemple :

```php
$pluie = false;

if ($pluie) {
    echo "Je reste à la maison.";
} else {
    echo "Je vais sur le chantier.";
}
```

💬 L’ordinateur lit :  
> “S’il pleut (faux), alors je ne fais pas ça… donc je fais le reste (else) : je vais sur le chantier.”

---

## 3️⃣ Les boucles – poser les briques une par une 🧱

Une **boucle**, c’est quand tu veux **répéter une action plusieurs fois**,  
comme quand tu poses **10 briques** l’une après l’autre.

Exemple :

```php
for ($i = 1; $i <= 10; $i++) {
    echo "Je pose la brique numéro $i<br>";
}
```

---

### 🔍 Décortiquons la phrase magique

`for ($i = 1; $i <= 10; $i++)`

C’est une phrase en trois parties :

| Partie | Explication |
|---------|--------------|
| `$i = 1` | Je **commence** à la brique numéro 1 |
| `$i <= 10` | Je **continue** tant que je n’ai pas posé la 10e brique |
| `$i++` | J’**avance d’une brique** à chaque tour |

---

### 🔹 1. `$i = 1` – Le départ

Tu dis à ton apprenti :  
> “Commence à la première brique.”

```php
$i = 1;
```

---

### 🔹 2. `$i <= 10` – La condition

Tu lui dis :  
> “Continue tant que tu n’as pas dépassé 10 briques.”

Quand `$i` devient 11 :  
> “Chef, j’ai fini !”

---

### 🔹 3. `$i++` – Le pas en avant

C’est ton **mouvement**.  
Chaque fois que tu poses une brique, tu avances d’une place.

`$i++` veut dire :  
> “Ajoute 1 à `$i`.”

🧠 Astuce :  
Le “++” c’est ton **petit pas** dans la rangée.  
Un “+” pour chaque pied.

---

### 💬 Ce que fait la boucle

```php
for ($i = 1; $i <= 10; $i++) {
    echo "Je pose la brique numéro $i<br>";
}
```

Affiche :

```
Je pose la brique numéro 1
Je pose la brique numéro 2
Je pose la brique numéro 3
...
Je pose la brique numéro 10
```

Quand il arrive à 11, il s’arrête.  
Mur terminé 🧱✅

---

## 4️⃣ Les fonctions – fabriquer ton propre outil 🔧

Une **fonction**, c’est comme un **outil** que tu fabriques une fois,  
et que tu peux **réutiliser** quand tu veux.

Exemple :  
> Tu fais un petit outil qui dit bonjour au chef.

```php
function direBonjour() {
    echo "Bonjour chef, prêt à travailler !";
}
```

Pour utiliser ton outil :

```php
direBonjour();
```

Résultat :

```
Bonjour chef, prêt à travailler !
```

---

## 5️⃣ Les fonctions avec paramètres – ton outil réglable 🔩

Tu sais déjà ce qu’est une fonction : un petit **outil** que tu fabriques et que tu peux réutiliser quand tu veux.

Mais maintenant, on va rendre ton outil **réglable**, comme ton **mètre de chantier** que tu peux ouvrir ou fermer selon la longueur à mesurer.

---

### 🔹 Exemple 1 – dire bonjour à un client

```php
function direBonjour($nom_client) {
    echo "Bonjour $nom_client, prêt pour le chantier ?<br>";
}

direBonjour("Dupont");
direBonjour("Martin");
```

🧱 Résultat :

```
Bonjour Dupont, prêt pour le chantier ?
Bonjour Martin, prêt pour le chantier ?
```

---

### 💬 Explication claire

Une **fonction**, c’est une **petite machine de travail**.

Le **paramètre**, c’est ce que tu lui **donnes à mesurer ou à utiliser**.

Ici, le paramètre est `$nom_client`.  
Quand tu appelles la fonction, tu lui donnes le nom du client à saluer :

```php
direBonjour("Dupont");
```

➡️ L’ordinateur remplace `$nom_client` par `"Dupont"`  
et affiche :  
**Bonjour Dupont, prêt pour le chantier ?**

Puis quand tu fais :

```php
direBonjour("Martin");
```

il recommence, cette fois avec “Martin”.

C’est comme ton **mètre** : tu lui ouvres la longueur que tu veux mesurer.  
Le mètre (la fonction) est le même, mais **la valeur change** à chaque fois.

---

### 🔹 Exemple 2 – calculer le prix d’un mur

Tu veux faire une petite **fonction pratique** pour calculer le prix d’un mur selon la surface et le prix du mètre carré.

```php
function calculerPrix($surface, $prix_m2) {
    $total = $surface * $prix_m2;
    echo "Le prix du mur est de $total euros.<br>";
}

calculerPrix(10, 40);
calculerPrix(20, 35);
```

🧮 Résultat :

```
Le prix du mur est de 400 euros.
Le prix du mur est de 700 euros.
```

---

### 💬 Explication du chef

| Élément | Ce que c’est sur le chantier |
|----------|------------------------------|
| `$surface` | la taille du mur à construire |
| `$prix_m2` | le prix du mètre carré |
| `$total = $surface * $prix_m2` | le calcul du devis |
| `calculerPrix(10, 40)` | tu demandes le devis d’un mur de 10 m² à 40 €/m² |

🧱 Le grand intérêt des **paramètres**, c’est que ton outil s’adapte à chaque mur, sans tout réécrire.  
Tu changes juste les chiffres.

---

## 6️⃣ La boucle `foreach` – faire le tour de ta liste de clients 🔁

Tu as compris la boucle `for` (faire quelque chose plusieurs fois).  
Maintenant, imagine que tu as **une liste de clients** à rappeler ou à facturer.  
Tu veux faire la même action pour **chacun d’eux**.

C’est là que la boucle **`foreach`** est parfaite.

---

### 🔹 Exemple : appeler chaque client 📞

```php
$clients = ["Dupont", "Martin", "Durand"];

foreach ($clients as $client) {
    echo "J'appelle le client $client<br>";
}
```

🧱 Résultat :

```
J'appelle le client Dupont
J'appelle le client Martin
J'appelle le client Durand
```

---

### 💬 Explication simple

Tu dis à ton apprenti :
> “Voici une liste de clients.  
> Prends-les **un par un**, et fais la même action pour chacun.”

- `$clients` → c’est ta **liste** (comme une feuille avec les noms).  
- `foreach` → veut dire **“pour chaque élément de la liste”**.  
- `$client` → c’est **le nom du client actuel**, qui change à chaque tour.

L’ordinateur fait :
1. `$client = "Dupont"` → affiche “J'appelle le client Dupont”  
2. `$client = "Martin"` → affiche “J'appelle le client Martin”  
3. `$client = "Durand"` → affiche “J'appelle le client Durand”  
Puis il s’arrête. ✅

---

### 🧱 Comparaison des deux boucles

| Boucle | Ce qu’elle fait | Exemple sur le chantier |
|--------|------------------|--------------------------|
| `for` | Répète une action un **nombre précis de fois** | Poser 10 briques |
| `foreach` | Répète une action pour **chaque élément d’une liste** | Appeler chaque client |

---

## 7️⃣ Résumé du chef 👷‍♂️

| Ce que tu apprends | Ce que ça veut dire sur un chantier |
|--------------------|------------------------------------|
| `$variable` | ton seau où tu ranges un nombre ou un mot |
| `if / else` | décider selon la météo ou la situation |
| `true / false` | oui ou non |
| `for` | répéter une action un certain nombre de fois |
| `foreach` | faire une action pour chaque élément d’une liste |
| `function` | ton outil que tu fabriques |
| `paramètre` | la donnée que tu donnes à ton outil pour qu’il travaille bien |

---

## 🚧 Leçon terminée !

Bravo 👏  
Tu connais maintenant :
- les **variables** (tes seaux),
- les **conditions** (tes décisions),
- les **boucles** (tes répétitions),
- et les **fonctions** (tes outils).

Tu es prêt à t’exercer sur de vrais petits chantiers de code PHP ! 🧱💻
