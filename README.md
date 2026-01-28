# Rheos FlowChart - Outil de diagramme simplifie

Un outil de creation de diagrammes et flowcharts intuitif, entierement en HTML/CSS/JavaScript, sans dependances serveur.

## Fonctionnalites

### Creation de cartes

| Methode | Action |
|---------|--------|
| Double-clic | Cree une carte a l'emplacement du curseur |
| Bouton "+" flottant | Cree une carte au centre de l'ecran |
| Bouton "Nouvelle carte" | Cree une carte au centre de l'ecran |
| Touche Tab | Cree une carte enfant connectee a la carte selectionnee |

### Structure d'une carte

Chaque carte peut contenir :
- **1 titre** : editable directement en cliquant dessus
- **1 categorie** : optionnelle, definit la couleur de fond
- **Zones de texte** : grille configurable (ex: 2x3 = 6 zones)
- **Connexions** : liens de filiation avec d'autres cartes

### Manipulation des cartes

- **Deplacer** : cliquer-glisser sur la carte
- **Redimensionner** : cliquer-glisser sur le coin inferieur droit
- **Modifier** : cliquer sur l'icone crayon (au survol)
- **Supprimer** : cliquer sur l'icone X ou touche Suppr
- **Categorie** : cliquer sur l'icone roue crantee (au survol)

### Systeme de categories

Les categories permettent d'organiser visuellement les cartes :
- Chaque categorie a un **nom** et une **couleur**
- La couleur devient le fond de l'en-tete de la carte
- Le texte s'adapte automatiquement (noir ou blanc) pour rester lisible
- Un badge affiche le nom de la categorie dans l'en-tete

**Gestion des categories :**
- Bouton "Categories" dans la barre d'outils pour gerer toutes les categories
- Icone roue crantee sur chaque carte pour assigner/creer une categorie

### Connexions entre cartes

Pour creer une connexion :
1. Survoler une carte pour voir les points de connexion (ronds roses)
2. Cliquer-glisser depuis un point vers une autre carte
3. Relacher sur la carte cible

**Direction des fleches :**
- Cliquer sur une connexion pour ouvrir le menu de direction
- Choix : vers la cible (→), vers la source (←), bidirectionnel (↔)
- Option de suppression de la connexion

### Raccourcis clavier

| Touche | Action |
|--------|--------|
| Double-clic | Nouvelle carte a cet emplacement |
| Tab | Nouvelle carte enfant (avec connexion) |
| Suppr | Supprimer la carte selectionnee |
| Escape | Annuler / Fermer les modales |

## Sauvegarde et export

### Sauvegarde automatique
L'espace de travail est automatiquement sauvegarde dans le navigateur (localStorage). Vos donnees sont conservees entre les sessions.

### Export/Import JSON
- **Sauvegarder** : exporte un fichier `.json` contenant tout l'espace de travail
- **Charger** : importe un fichier `.json` precedemment sauvegarde

### Export PDF
Le bouton "Export PDF" genere un fichier PDF contenant :
- Toutes les cartes visibles
- Les connexions entre cartes
- Les couleurs et styles

Ideal pour l'impression ou le partage.

## Installation

Aucune installation requise. Ouvrir simplement `index.html` dans un navigateur moderne.

### Navigateurs supportes
- Chrome (recommande)
- Firefox
- Edge
- Safari

## Dependances externes (CDN)

- [html2canvas](https://html2canvas.hertzen.com/) - Capture d'ecran pour l'export PDF
- [jsPDF](https://github.com/parallax/jsPDF) - Generation de fichiers PDF

## Interface

```
+------------------------------------------------------------------+
|  FlowChart  |  + Nouvelle carte  |  Categories  |  Export PDF   |
+------------------------------------------------------------------+
|                                                                  |
|     +------------------+          +------------------+           |
|     | Titre carte      |          | Titre carte      |          |
|     | [Categorie]      |--------->| [Categorie]      |          |
|     |------------------|          |------------------|           |
|     | Zone texte 1     |          | Zone texte 1     |          |
|     | Zone texte 2     |          | Zone texte 2     |          |
|     +------------------+          +------------------+           |
|                                                                  |
|                                                          [+]    |
+------------------------------------------------------------------+
```

## Conseils d'utilisation

1. **Commencez par les categories** : definissez vos categories avant de creer les cartes pour une meilleure organisation visuelle.

2. **Utilisez Tab** : pour creer rapidement des hierarchies de cartes connectees.

3. **Sauvegardez regulierement** : bien que la sauvegarde automatique soit active, exportez votre travail en JSON pour avoir une copie de securite.

4. **Zoomez pour l'export** : l'export PDF capture la zone contenant les cartes, assurez-vous que tout est visible.

## Licence

Libre d'utilisation.
