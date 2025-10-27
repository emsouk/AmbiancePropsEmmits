# 🪄 AmbiancePropsEmmits

![Vue.js](https://img.shields.io/badge/Vue.js-3.x-brightgreen?logo=vue.js)
![Vite](https://img.shields.io/badge/Vite-5.x-646CFF?logo=vite&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-blue)
![Status](https://img.shields.io/badge/status-Active-success)

---

### 🧩 Projet Vue 3 – Communication entre composants (Props & Emits)

**AmbiancePropsEmmits** est un mini-projet réalisé avec **Vue 3** qui illustre la communication entre composants à l’aide des **props** (transmission descendante de données) et des **events** (remontée d’informations vers le parent).  

Ce projet a été développé dans un but **pédagogique**, afin de comprendre les échanges de données dans une application Vue en utilisant la **Composition API**.

---

## 🏗️ Structure du projet

Le projet est constitué de **trois composants principaux** :

### 🟨 `Parent.vue`
- Gère les données utilisateur (`name`, `age`)
- Centralise la logique et affiche les données
- Transmet les infos au composant `ActiveUser`

### 🟪 `ActiveUser.vue`
- Reçoit les données via les **props**
- Affiche les informations envoyées par le parent

### 🟦 `UserData.vue`
- Contient un **formulaire** pour modifier le nom et l’âge
- Émet un **événement** `set-data` au parent avec les nouvelles valeurs

---

## ⚙️ Fonctionnement

1. Les données initiales (`name: "Emilie"`, `age: 30`) sont définies dans le **parent**.  
2. L’utilisateur saisit de nouvelles valeurs dans le **formulaire** (composant `UserData`).  
3. Lors de la soumission, un **événement `set-data`** est émis avec ces valeurs.  
4. Le **parent** met à jour l’objet `user`, qui est transmis automatiquement à `ActiveUser`.  
5. Grâce à la réactivité de Vue, les données s’affichent instantanément.

---

## 🧠 Concepts Vue 3 mis en pratique

| 🧩 Concept | 💬 Description |
|-------------|----------------|
| `ref()` | Crée des données réactives |
| `defineProps()` | Reçoit les données depuis le parent |
| `defineEmits()` | Émet des événements vers le parent |
| `v-model` | Liaison bidirectionnelle entre input et variable |
| `@submit.prevent` | Empêche le rechargement de la page |
| **Composition API** | Syntaxe moderne, claire et modulaire |

---

## 🪶 Technologies utilisées

- ⚡ **Vue 3**
- 🚀 **Vite**
- 🎨 **Tailwind CSS** + **DaisyUI**
- 💡 **JavaScript (Composition API)**

---

## 🧰 Installation & Exécution

```bash
# Cloner le dépôt
git clone https://github.com/emsouk/AmbiancePropsEmmits.git

# Se déplacer dans le dossier
cd AmbiancePropsEmmits

# Installer les dépendances
npm install

# Lancer le serveur de développement
npm run dev
