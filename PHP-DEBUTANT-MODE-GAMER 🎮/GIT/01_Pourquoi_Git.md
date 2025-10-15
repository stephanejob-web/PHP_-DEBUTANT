# 🎮 Leçon 01 : Ta première sauvegarde (ou pourquoi Git va te sauver la partie)

## Salut à toi, futur héros du code ! 🧙‍♂️🎮

Soyons honnêtes...

**T'as déjà perdu ta sauvegarde juste avant un boss ?**  
Genre... 3 heures de jeu, tu rates une esquive, et POUF 💥  
Ton perso respawn au tout début.

Ou pire encore...

**T'as déjà eu 50 versions du même jeu ?**
```
mon-jeu
mon-jeu-v2
mon-jeu-v2-final
mon-jeu-v2-final-VRAIMENT-FINAL
mon-jeu-v2-final-VRAIMENT-FINAL-cette-fois-cest-la-bonne
```
😭 **Assez !**

Aujourd’hui, on apprend à utiliser **Git**, ton **système de sauvegarde IRL**.  
Grâce à lui, tu ne perdras plus JAMAIS ta progression. 🧠💾

---

## 🧑‍🤝‍🧑 Bonus : Qui a fait quoi dans la guilde ?

Quand tu fais un **commit**, Git enregistre une **nouvelle sauvegarde** de ta partie, avec ton pseudo et tes exploits.

| Info | Exemple | Pourquoi c’est utile |
|------|----------|----------------------|
| 👤 **Ton pseudo** | JoueurKevin | Savoir qui a joué le tour |
| 📧 **Ton email** | kevin@rpg.com | Contacter le joueur si besoin |
| 📅 **La date et l’heure** | 12 oct 2025, 10h30 | Savoir quand le checkpoint a été créé |
| 💬 **Ton message** | “Boss du formulaire battu” | Savoir ce qui a été accompli |

**Exemple concret :**  
Si ton coéquipier demande :  
> “Qui a ajouté le formulaire magique ? C’était quand ?”

Tu tapes :
```bash
git log
```
Et Git répond :  
> “Ajout du formulaire - par Sophie le 10 octobre à 9h15”

**Résultat ?**
✅ Tout le monde sait qui a fait quoi  
✅ On peut rejouer une version stable  
✅ On suit la progression du projet  
✅ Si un bug apparaît, on sait d’où il vient  

---

## 🤔 Mais c’est quoi Git exactement ?

**Réponse rapide :**  
Git, c’est ton **système de sauvegarde universel**, ton **journal de quêtes du code**. 🕹️

Quand tu avances dans un jeu :  
- Checkpoint 1 : Niveau 1 terminé ✅  
- Checkpoint 2 : Arme magique obtenue ✅  
- Checkpoint 3 : Boss du château battu ✅  

Si le jeu plante au niveau 4, tu peux **revenir au dernier checkpoint stable**.

Git fait **exactement la même chose** avec ton code. 💾⚙️

---

## ⚠️ STOP ! Git ≠ Ctrl+S

Beaucoup de joueurs pensent :  
❌ “Git, c’est juste une sauvegarde automatique.”  
❌ “Je peux copier mon dossier sur une clé USB, non ?”  

🔥 **Faux !** Git, c’est un **vrai système de checkpoints**, pas une simple sauvegarde manuelle.

---

## 📖 L’histoire du joueur Kevin qui a tout cassé (et qui s’en est sorti grâce à Git)

### 🎮 Lundi matin - 9h00  
Kevin construit son jeu. Tout marche nickel.  
Il fait une sauvegarde :  
✅ “Niveau 1 - Page d’accueil OK”

### 🕓 Lundi après-midi - 14h00  
Il ajoute un nouveau niveau.  
✅ “Niveau 2 - Galerie déverrouillée”

### 🕙 Mardi matin - 10h00  
Il modifie le design (le skin du perso). Il bidouille un peu trop... 😬  

### 🕛 Mardi midi - 12h00  
💥 **CATASTROPHE !**  
Le jeu crash. Plus rien ne marche.

### 😱 Sans Git : Game Over  
Kevin devrait tout recommencer manuellement. 😭

### 😎 Avec Git : Respawn assuré  
Il ouvre son journal de quêtes :
```bash
git log --oneline
```
Il voit :
```
a1b2c3d Niveau 2 - Galerie déverrouillée
z9y8x7w Niveau 1 - Page d’accueil OK
```
Il tape :
```bash
git checkout z9y8x7w
```
💾 **BOOM !** Retour au niveau 1, tout refonctionne ! 🎯

---

## 🎯 Git, c’est quoi VRAIMENT ?

Git, c’est ton **système de jeu version code** :

### 1️⃣ Des checkpoints automatiques 📸  
Tu peux revenir à **n’importe quelle étape**.

### 2️⃣ Un historique complet de ta progression 📜  
Tu sais **qui a fait quoi**, **quand**, et **pourquoi**.

### 3️⃣ Un moyen de tester sans casser ta partie 🧪  
Tu veux tester un nouveau pouvoir ? Crée une **branche parallèle**, sans toucher à ton monde principal.

### 4️⃣ Un jeu coopératif 👥  
Chaque joueur sauvegarde ses progrès. Si quelqu’un fait un bug, on sait qui, quand et pourquoi — et on peut rollback sans ragequit.

---

## 🎮 L’analogie du joueur pro

| En jeu vidéo | Avec Git |
|---------------|-----------|
| 📸 **Faire une sauvegarde** | `git commit` |
| 📋 **Voir ton historique de parties** | `git log` |
| ⏪ **Charger une ancienne sauvegarde** | `git checkout` |
| 🧪 **Tester un nouveau build** | `git branch` |
| 🔀 **Fusionner deux versions** | `git merge` |

**Tu vois ? Git, c’est littéralement ton système de sauvegarde de code. 💾**

---

## 🚀 OK, passons à la pratique !

Maintenant que tu sais **pourquoi Git est vital**, on va apprendre à **l’utiliser comme un gamer pro.**

---

### 🎯 Les 3 gestes de base du joueur

Pour créer un checkpoint dans ton aventure, tu fais **3 moves** :

---

### 1️⃣ `git init` → Crée ton monde

```bash
git init
```
**En clair :** “Je démarre une nouvelle partie.”  
Git crée ton univers, prêt à recevoir tes sauvegardes.

---

### 2️⃣ `git add` → Choisis ce que tu veux sauvegarder

```bash
git add index.html
```
Ou pour tout sauvegarder d’un coup :
```bash
git add .
```
**En clair :** “Je sélectionne les éléments à sauvegarder.”  
💡 **Astuce :** ne sauvegarde pas le bazar, choisis ce qui compte.

---

### 3️⃣ `git commit` → Crée ta sauvegarde avec un message

```bash
git commit -m "Premier checkpoint - Base du jeu posée"
```
**En clair :** “Je prends une capture de mon monde avec un titre.”  
C’est ton checkpoint officiel ! 🏁

---

## 💾 Exemple complet pas à pas

Tu veux construire ton premier jeu (ou ton site) ? Voici ton tuto :

### 1️⃣ Crée ton terrain de jeu
```bash
mkdir mon-jeu
cd mon-jeu
```

### 2️⃣ Initialise Git
```bash
git init
```

### 3️⃣ Crée ton premier fichier
```bash
echo "<h1>Bienvenue dans mon jeu !</h1>" > index.html
```

### 4️⃣ Prépare la sauvegarde
```bash
git add index.html
```

### 5️⃣ Crée ton premier checkpoint
```bash
git commit -m "Premier niveau - Page d’accueil créée"
```

🎉 Bravo, tu viens de créer ta **première sauvegarde Git** !  

---

## 🔁 Le cycle du gamer pro

```
1. Tu gagnes de l’XP (tu codes)  
        ↓  
2. git add . (tu prépares la sauvegarde)  
        ↓  
3. git commit -m "message" (tu crées le checkpoint)  
        ↓  
4. Continue l’aventure ! 🔁  
```

---

## 🧾 Les messages de commit : ton journal de quêtes

### ✅ Bons messages :
```bash
git commit -m "Boss du formulaire battu"
git commit -m "Niveau 2 terminé - Galerie ajoutée"
git commit -m "Nouveau skin du site équipé"
```
### ❌ Mauvais messages :
```bash
git commit -m "update"
git commit -m "test"
git commit -m "ça avance"
```

> Ces messages, c’est comme sauvegarder “partie1”, “partie2” sans savoir où t’en es. 😩

---

## 🎮 Exercice : à toi de jouer !

**Mission :** Crée ta **première sauvegarde Git** 🧠

1️⃣ Crée un dossier `mon-portfolio`  
2️⃣ Entre dedans avec `cd mon-portfolio`  
3️⃣ Initialise Git : `git init`  
4️⃣ Crée un fichier `index.html` avec ton pseudo dedans  
5️⃣ Ajoute-le avec `git add index.html`  
6️⃣ Crée ton checkpoint :  
```bash
git commit -m "Premier checkpoint - page d’accueil prête"
```

🎯 **GG !** Tu viens de poser ton premier checkpoint Git comme un vrai gamer. 💾

---

## 🗝️ Antisèche du joueur Git

| Commande | Ce qu’elle fait | Version gamer |
|-----------|----------------|----------------|
| `git init` | Démarre un projet | Crée une **nouvelle partie** |
| `git add .` | Prépare les fichiers | Sélectionne ce que tu veux **sauvegarder** |
| `git commit -m ""` | Sauvegarde ton code | Crée un **checkpoint** |
| `git log` | Voir l’historique | Ouvre ton **journal de quêtes** |
| `git checkout` | Revenir à une version | **Respawn** à une sauvegarde stable |

---

## 💬 Citation du jour

> “Chaque commit est un checkpoint dans ton aventure.  
> Sauvegarde souvent, documente bien, et tu ne perdras jamais ta progression.”  
> — Le Maître du Code 🎮

---

## 🚀 La suite au prochain niveau...

Dans la **Leçon 02**, tu apprendras à :  
🕰️ Consulter tes anciennes sauvegardes  
🔍 Voir ce qui a changé entre deux checkpoints  
⏪ Revenir en arrière sans perdre ton loot  

**Prépare ton clavier, héros : la partie ne fait que commencer ! ⚔️**