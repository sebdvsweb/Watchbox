# 🎬 TP — WatchBox

## Présentation

Vous allez réaliser l'interface d'une plateforme de streaming appelée **WatchBox**.

L'objectif est de créer une page d'accueil présentant différentes séries, ainsi qu'une page permettant de consulter les informations détaillées d'une série.

Le projet doit avoir une apparence moderne, inspirée des plateformes de streaming. Le site devra notamment utiliser **Flexbox** pour organiser les différents éléments.

---

## 🎯 Objectifs

À la fin du TP, vous devez être capables d'utiliser :
- `display: flex`
- `flex-direction`
- `justify-content`
- `align-items`
- `flex-wrap`
- `align-self`

Vous devrez également être capables de :
- Créer une page HTML structurée.
- Utiliser des liens entre plusieurs pages.
- Organiser une interface avec Flexbox.
- Créer une mise en page responsive.
- Modifier l'apparence d'une page avec CSS.

---

## 📁 Organisation du projet

Votre projet devra respecter la structure suivante :

```text
watchbox/
│
├── index.html
├── serie.html
├── style.css
└── README.md
```

- **`index.html`** : Page d'accueil.
- **`serie.html`** : Page de présentation d'une série.
- **`style.css`** : Feuille de style CSS.
- **`README.md`** : Documentation du projet.

---

## 🏠 Étape 1 — Créer la page d'accueil

Créez une page `index.html`. Elle doit contenir :
- Un `header`
- Un logo
- Un menu de navigation
- Un bouton de connexion
- Une section présentant une série principale (hero)
- Une section présentant plusieurs séries
- Un `footer`

> **Note :** Le site doit avoir un fond noir et utiliser une palette de couleurs sombres.

---

## 🧭 Étape 2 — Le menu

Le `header` doit être organisé horizontalement. Vous devez utiliser Flexbox pour positionner les éléments de cette façon :

```text
LOGO                    MENU                    CONNEXION
```

Le logo doit se trouver à gauche et le bouton de connexion à droite.

### Contraintes
Le `header` doit obligatoirement utiliser :
- `display: flex`
- `align-items`
- `justify-content`

---

## ⭐ Étape 3 — La série principale

Créez une grande section mettant en valeur une série principale.

Elle doit contenir au minimum :
- Le nom de la série
- Sa note
- Son année de sortie
- Son âge conseillé
- Le nombre de saisons
- Une courte description
- Un bouton permettant d'accéder à la fiche de la série

Utilisez **Flexbox** pour organiser ces différents éléments.

---

## 🎞️ Étape 4 — Les cartes de séries

Créez une section contenant plusieurs séries sous forme de **cartes**.

Chaque carte peut contenir :
- Une affiche
- Le titre
- Le genre
- La note
- L'âge conseillé

### Exemple de structure de carte :
```text
┌──────────────┐
│              │
│   AFFICHE    │
│              │
├──────────────┤
│ Stranger     │
│ Things       │
│              │
│ ★ 4.8    16+ │
└──────────────┘
```

Les cartes doivent être disposées horizontalement. Lorsqu'il n'y a plus assez de place sur l'écran, elles doivent automatiquement passer à la ligne suivante.

> **Propriété obligatoire :** Utilisez `flex-wrap`.

---

## ↔️ Étape 5 — `justify-content`

Testez différentes valeurs pour la propriété `justify-content` :
- `flex-start`
- `center`
- `flex-end`
- `space-between`
- `space-around`
- `space-evenly`

Observez le résultat et choisissez la valeur qui convient le mieux à votre interface.

---

## ↕️ Étape 6 — `align-items`

Utilisez `align-items` pour modifier la position des éléments sur l'axe secondaire (transversal).

Testez les valeurs suivantes :
- `flex-start`
- `center`
- `flex-end`
- `stretch`

---

## 🔄 Étape 7 — `flex-direction`

Créez une section dans laquelle plusieurs éléments sont initialement disposés horizontalement.

1. Testez `flex-direction: row;`
2. Testez ensuite `flex-direction: column;`

Observez les changements d'alignement.

---

## 🎯 Étape 8 — `align-self`

Choisissez une carte de série spécifique (par exemple, votre série préférée).

Utilisez la propriété `align-self` pour modifier la position de cette seule carte, sans affecter le positionnement des autres cartes de la section.

---

## 🔗 Étape 9 — Créer la fiche d'une série

Créez une deuxième page nommée `serie.html`.

Cette page présente une série de manière plus détaillée et contient :
- Une affiche
- Le titre
- La note, l'année, l'âge conseillé et le nombre de saisons
- Une description complète
- Des boutons d'action (ex: *Lecture*, *Ajouter à ma liste*)
- Des informations complémentaires sur la série
- Une liste d'épisodes

---

## 🔙 Étape 10 — Relier les deux pages

Depuis la page d'accueil (`index.html`), l'utilisateur doit pouvoir cliquer sur une carte ou un bouton pour accéder à la fiche détaillée (`serie.html`) :

```html
<a href="serie.html">
  <!-- Élément cliquable -->
</a>
```

Assurez-vous d'ajouter également un moyen de retourner à la page d'accueil depuis `serie.html`.

---

## 📱 Étape 11 — Responsive Design

Votre site doit s'adapter aux écrans plus petits (smartphones, tablettes).

Sur un écran étroit :
- Le menu de navigation doit s'adapter.
- Les cartes doivent automatiquement passer à la ligne.
- La fiche de la série doit passer d'un affichage horizontal à un affichage vertical.
- Les boutons doivent rester facilement accessibles.
- Aucun contenu ne doit dépasser horizontalement de l'écran (pas de scroll horizontal indésirable).

Vous pouvez utiliser une media query CSS :
```css
@media screen and (max-width: 800px) {
  /* Vos règles CSS pour mobile/tablette */
}
```

---

## 🎨 Étape 12 — Personnalisation

Personnalisez le rendu visuel de votre application :
- Couleurs et dégradés
- Tailles de police et typographies
- Marges et espacements
- Images d'affiches et contenus
- Effets d'interaction au survol (`:hover`)

> ⚠️ **Attention :** Le fond général du site doit rester sombre/noir pour respecter le thème streaming.

---

## ⭐ Défi supplémentaire

Si vous avez terminé avant la fin de la séance, choisissez et implémentez une ou plusieurs fonctionnalités parmi les suivantes :

- [ ] Ajouter une troisième ligne de cartes de séries.
- [ ] Créer une deuxième page de fiche produit (ex: `serie2.html`).
- [ ] Ajouter une section « Top 10 ».
- [ ] Ajouter des badges sur les cartes (*Nouveau*, *Tendance*, etc.).
- [ ] Ajouter des animations et effets au survol des cartes.
- [ ] Créer un classement visuel des meilleures séries.