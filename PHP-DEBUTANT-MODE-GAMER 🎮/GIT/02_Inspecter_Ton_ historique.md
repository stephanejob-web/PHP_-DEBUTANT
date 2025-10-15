# 🕹️ Leçon 02 : Scanner ta base (status, log, diff)

## Salut explorateur du code ! 🧙‍♂️🔍

Dans la **Leçon 01**, tu as appris à **faire des sauvegardes** avec Git, ton système de checkpoints ultime.  
Cool ! Mais maintenant, tu te demandes sûrement :

🤔 "Euh... j’ai sauvegardé QUOI exactement ?"  
🤔 "Comment je vois toutes mes sauvegardes ?"  
🤔 "Comment je sais ce qui a changé depuis mon dernier checkpoint ?"

**Aujourd’hui, tu vas apprendre à :**
- Vérifier l’état actuel de ta base
- Consulter tout ton journal de quêtes
- Comparer ce que t’as modifié depuis la dernière sauvegarde

🎯 Bref : devenir un vrai **analyste du code** !

---

## ⚙️ Retour dans ta base

Imagine : t’es un commandant spatial.

**Chaque matin, tu veux savoir :**
1. **Où en est ta mission ?** → Ce qui a changé depuis hier → `git status`  
2. **L’historique complet** → Toutes les sauvegardes depuis le début → `git log`  
3. **Les différences entre deux versions** → Ce qui a été modifié → `git diff`

Voilà les **3 commandes de scan** que tout joueur pro doit maîtriser ! 💪

---

## 🔍 Commande 1 : `git status` (Scanner ton monde)

C’est **la commande la plus utilisée** du multivers du code.  
Tu vas la taper **1000 fois par session**.

```bash
git status
```

**En français :** “Git, montre-moi l’état actuel de ma base.”

**Analogie gamer :** C’est comme ouvrir ton menu de mission :  
- “Ah tiens, une quête a été modifiée”  
- “Oh, un nouvel item est apparu”  
- “Hmm… ce fichier n’a pas encore été validé par le système.”

---

### 🎯 À quoi ça sert ?

Ça t’indique :
- ✅ Les fichiers **modifiés** depuis ton dernier checkpoint  
- ✅ Ceux **prêts à être sauvegardés** (`git add`)  
- ✅ Les nouveaux fichiers que Git **ne connaît pas encore** (non suivis)

---

### 🧪 Exemple concret

Reprends ton projet `mon-site` (ta base principale).  
Ouvre le fichier `index.html` et ajoute :

```html
<p>Je suis un aventurier du code, prêt à gravir les niveaux !</p>
```

Ensuite, tape :

```bash
git status
```

**Git te répond :**

```
On branch main
Changes not staged for commit:
  modified:   index.html
```

**Traduction :**
> “Hé joueur ! Le fichier `index.html` a été modifié, mais t’as pas encore fait de checkpoint.”

---

### 💡 Les 3 états possibles dans ton inventaire

| État | Signification | Analogie jeu vidéo | Couleur |
|------|----------------|--------------------|----------|
| 🔴 **Modifié (non ajouté)** | Tu as modifié l’objet, mais pas sauvegardé | Un item modifié mais pas équipé | Rouge |
| 🟢 **Prêt à sauvegarder** | Tu as fait `git add` | Item prêt à être enregistré | Vert |
| ⚪ **Non suivi** | Git ne connaît pas ce fichier | Nouvel item ramassé, pas encore scanné | Rouge |

💬 **Astuce du joueur pro :** Tape `git status` **avant chaque commit** pour vérifier ton inventaire avant de sauvegarder.

---

## 📜 Commande 2 : `git log` (Le journal des quêtes)

Tu veux relire toutes tes aventures ? Tape :

```bash
git log
```

**En français :** “Montre-moi l’historique complet de mes exploits.”

**Analogie gamer :** C’est ton **journal de quêtes** : il garde la trace de tout ce que tu as accompli.

---

### 🧪 Exemple pratique

```bash
git log
```

Résultat :

```
commit a1b2c3d4e5f6g7h8i9j0
Author: PlayerOne <player@game.com>
Date:   Oct 12 2025 10:30

    Checkpoint 1 - Base principale construite

commit z9y8x7w6v5u4t3s2r1q0
Author: PlayerTwo <ally@team.com>
Date:   Oct 11 2025 18:10

    Checkpoint 0 - Fondation du projet
```

**Chaque commit = une sauvegarde réussie** 💾  
Avec :  
- 👤 Le joueur  
- ⏰ La date de la mission  
- 💬 Le titre de la quête accomplie

---

### 🎨 Rendre `git log` plus lisible

```bash
git log --oneline
```

**Résultat :**

```
a1b2c3d PlayerOne - Base principale construite
z9y8x7w PlayerTwo - Fondation du projet
```

💡 **Pro tip :** plus propre, plus lisible, parfait pour ton tableau de mission. 😎

---

### 🧭 Autres filtres utiles

```bash
git log --oneline --graph
```
> Affiche une **mini-carte du monde** avec les différentes branches de ton projet (comme les timelines parallèles dans un RPG).

```bash
git log --oneline -5
```
> Montre seulement les **5 dernières quêtes accomplies**.

```bash
git log --author="PlayerOne"
```
> Filtre les quêtes par joueur. Pratique pour voir qui a fait quoi dans la guilde.

---

## 🧩 Commande 3 : `git diff` (Comparer deux sauvegardes)

Tu veux voir **ce qui a changé depuis ton dernier checkpoint** ? Tape :

```bash
git diff
```

**En français :** “Montre-moi les différences entre ma version actuelle et la dernière sauvegarde.”

**Analogie gamer :** C’est comme comparer deux versions de ton équipement :
- Hier : Épée en fer ⚔️  
- Aujourd’hui : Épée en acier ⚔️✨  
→ **Différence : amélioration de +10 dégâts !**

---

### 🧪 Exemple pratique

```bash
git diff
```

Résultat :

```diff
diff --git a/index.html b/index.html
--- a/index.html
+++ b/index.html
@@ -1 +1,2 @@
 <h1>Bienvenue dans ma base !</h1>
+<p>Je suis un aventurier du code, prêt à gravir les niveaux !</p>
```

**Traduction :**
- 🔴 Lignes supprimées = éléments perdus
- 🟢 Lignes ajoutées = nouveaux bonus ou améliorations

Tu viens littéralement de **booster ton fichier** ! ⚡

---

### 💡 Variantes utiles

```bash
git diff --staged
```
> Montre les fichiers **prêts à être sauvegardés**.

```bash
git diff HEAD
```
> Compare **toutes les modifications** depuis ton dernier checkpoint.

---

## 🎮 Exercice : À toi de jouer !

**Mission : Analyse ton projet comme un pro hacker !**

1. Ouvre ton projet `mon-portfolio`
2. Modifie `index.html` (ajoute une phrase ou un emoji 👾)
3. Tape `git status` → vois le changement (en rouge)
4. Tape `git diff` → compare avant/après
5. Fais `git add index.html`
6. Tape `git status` → le fichier devient vert !
7. Fais `git commit -m "Ajout d’un paragraphe badass"`
8. Tape `git log --oneline` → vérifie ton nouveau checkpoint !

✅ Bravo, tu viens de devenir un **analyste du code niveau 2** !

---

## 🔑 Antisèche : Les outils d’analyse du gamer

| Commande | Ce qu’elle fait | Analogie gamer | Quand l’utiliser |
|----------|-----------------|----------------|------------------|
| `git status` | Scanner l’état actuel | Regarder ton inventaire | Avant chaque sauvegarde |
| `git log` | Historique complet | Journal de quêtes | Pour retracer ton aventure |
| `git log --oneline` | Vue rapide | Mini-carte des missions | Quand tu veux un aperçu rapide |
| `git log --author="PlayerOne"` | Filtrer par joueur | Voir les actions d’un membre | Pour le travail d’équipe |
| `git diff` | Voir les changements | Comparer deux builds | Avant `git add` |
| `git diff --staged` | Voir ce qui est prêt | Liste d’items à sauvegarder | Avant `git commit` |

---

## 🧠 Le cycle du joueur pro

```
1. Tu codes ton niveau
        ↓
2. git status (scan rapide)
        ↓
3. git diff (analyse des modifs)
        ↓
4. git add . (prépare la sauvegarde)
        ↓
5. git commit -m "..." (checkpoint créé)
        ↓
6. git log --oneline (vérifie ton journal)
        ↓
7. Repars en mission ! 🔁
```

---

## 💬 Citation du jour

> “Un bon joueur sauvegarde souvent.  
> Un pro analyse ses changements avant chaque combat.”  
> — Le Maître du Code 🎮

---

## 🚀 Prochaine mission…

Dans la **Leçon 03**, tu vas apprendre à :  
- 🌿 Créer des **timelines parallèles** (les branches)  
- 🧬 Fusionner des univers alternatifs (merge)  
- 🧠 Comprendre comment les pros bossent à plusieurs sans casser le jeu  

**Prépare ton pad. On passe en mode multivers ! ⚔️**