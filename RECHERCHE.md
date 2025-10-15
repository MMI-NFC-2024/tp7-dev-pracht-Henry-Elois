# Fonctionnalité de recherche - Page Carte

## Nouvelles fonctionnalités ajoutées

### 🔍 Barre de recherche

- **Emplacement** : Au-dessus de la liste des établissements
- **Fonctionnalité** : Recherche en temps réel avec debouncing (300ms)
- **Recherche par** :
  - Nom de l'établissement
  - Ville/localisation

### ✨ Fonctionnalités interactives

#### Recherche en temps réel

- Tape le nom d'un établissement ou d'une ville
- Les résultats se filtrent automatiquement
- Les marqueurs sur la carte se cachent/affichent selon les résultats

#### Bouton d'effacement

- Apparaît automatiquement quand du texte est saisi
- Efface la recherche et restaure tous les établissements
- Accessible au clavier

#### Compteur de résultats

- Affiche le nombre d'établissements trouvés
- Format : "X sur Y établissements" ou "Y établissements" si tous affichés

#### Navigation au clavier

- **Échap** : Efface la recherche
- **Flèche bas** : Navigue vers le premier résultat
- **Tab** : Navigation standard

### 🎯 Fonctionnalités d'accessibilité

#### Structure sémantique

- Label approprié pour le champ de recherche
- Description avec `aria-describedby`
- Liste mise à jour avec `aria-live="polite"`

#### Gestion des états vides

- Message informatif quand aucun résultat n'est trouvé
- Icône et texte explicatifs

#### Focus et navigation

- Gestion du focus lors de l'effacement
- Navigation fluide entre les éléments

### 🗺️ Intégration avec la carte

#### Marqueurs dynamiques

- Les marqueurs se cachent/affichent selon la recherche
- Tous les marqueurs sont restaurés lors de l'effacement
- Performance optimisée (ajout/suppression de layers)

#### Informations contextuelles

- Zone d'information mise à jour selon la recherche
- Affichage du terme recherché et nombre de résultats

### 💡 Utilisation

1. **Recherche simple** : Tapez "Paris" pour voir tous les établissements parisiens
2. **Recherche précise** : Tapez "UNIVERSITE PARIS" pour des résultats plus ciblés
3. **Effacement rapide** : Cliquez sur ❌ ou appuyez sur Échap
4. **Navigation** : Utilisez Tab et les flèches pour naviguer

### 🔧 Détails techniques

#### Algorithme de recherche

- Normalisation en minuscules
- Recherche par inclusion (contains)
- Recherche dans le nom ET la ville extraite

#### Performance

- Debouncing pour éviter les recherches excessives
- Gestion efficace des marqueurs Leaflet
- Mise à jour DOM optimisée

#### Responsive

- Interface adaptée aux mobiles
- Icônes SVG intégrées
- Classes Tailwind pour le responsive design

## Classes Tailwind utilisées

### Champ de recherche

- `w-full px-4 py-2 pl-10 pr-4` : Taille et padding
- `focus:ring-2 focus:ring-blue-500` : Focus states
- `border border-gray-300 rounded-lg` : Bordures et coins

### Boutons et icônes

- `absolute inset-y-0` : Positionnement absolu
- `flex items-center` : Centrage des icônes
- `hover:text-gray-600` : États de survol

### État vide

- `text-center py-8 text-gray-500` : Centrage et couleur
- `w-12 h-12 mx-auto mb-4` : Taille et espacement de l'icône

Cette implémentation respecte les standards d'accessibilité WCAG 2.1 et offre une expérience utilisateur fluide et intuitive.
