# Améliorations d'accessibilité pour la page carte

## Améliorations implémentées

### 1. Structure sémantique

- ✅ Ajout d'éléments `<main>`, `<header>`, `<section>` pour une structure claire
- ✅ Hiérarchie de titres logique (h1 → h2 → h3)
- ✅ Utilisation d'attributs ARIA appropriés (`aria-label`, `aria-labelledby`, `aria-live`)

### 2. Navigation au clavier

- ✅ La carte est navigable au clavier (tabindex="0")
- ✅ Support des flèches directionnelles pour la navigation sur la carte
- ✅ Touche Échap pour fermer les popups
- ✅ Navigation dans la liste des établissements avec Tab/Shift+Tab
- ✅ Activation des éléments avec Entrée et Espace

### 3. Lecteurs d'écran

- ✅ Descriptions textuelles alternatives pour la carte (`role="img"`, `aria-label`)
- ✅ Zone d'informations en direct (`aria-live="polite"`) pour les mises à jour
- ✅ Titres masqués visuellement mais accessibles aux lecteurs d'écran (`.sr-only`)
- ✅ Labels descriptifs pour tous les éléments interactifs

### 4. Contraste et visibilité

- ✅ Contrastes de couleurs améliorés
- ✅ Indicateurs de focus visibles et distincts
- ✅ Support du mode contraste élevé (`@media (prefers-contrast: high)`)

### 5. Responsive et préférences utilisateur

- ✅ Design responsive pour mobile
- ✅ Respect de la préférence de mouvement réduit (`prefers-reduced-motion`)
- ✅ Adaptation à différentes tailles d'écran

### 6. Contenu alternatif

- ✅ Liste textuelle des établissements comme alternative à la carte
- ✅ Informations détaillées dans les popups avec structure HTML sémantique
- ✅ Coordonnées géographiques affichées pour context

### 7. Langue et localisation

- ✅ Déclaration de la langue française (`lang="fr"`)
- ✅ Titre de page descriptif
- ✅ Textes en français et descriptions claires

## Tests recommandés

### Tests manuels

1. **Navigation au clavier uniquement** : Testez toute la page sans souris
2. **Lecteur d'écran** : Utilisez NVDA, JAWS ou Voice Over
3. **Zoom** : Testez jusqu'à 200% de zoom
4. **Contraste élevé** : Activez le mode contraste élevé de Windows

### Tests automatisés

- Utilisez des outils comme axe-core, WAVE ou Lighthouse
- Vérifiez les standards WCAG 2.1 AA

## Conformité WCAG 2.1

Cette implémentation vise le niveau AA et couvre :

- ✅ 1.1.1 Contenu non textuel
- ✅ 1.3.1 Information et relations
- ✅ 1.4.3 Contraste (minimum)
- ✅ 2.1.1 Clavier
- ✅ 2.1.2 Pas de piège au clavier
- ✅ 2.4.1 Contournement de blocs
- ✅ 2.4.2 Titre de page
- ✅ 2.4.3 Parcours du focus
- ✅ 2.4.6 En-têtes et étiquettes
- ✅ 3.1.1 Langue de la page
- ✅ 4.1.2 Nom, rôle et valeur

## Améliorations futures possibles

1. **Recherche et filtrage** : Ajouter une fonction de recherche d'établissements
2. **Raccourcis clavier** : Implémenter des raccourcis pour les actions courantes
3. **Mode sombre** : Support du mode sombre système
4. **Géolocalisation** : Option pour centrer sur la position de l'utilisateur
5. **Export** : Permettre l'export de la liste en format accessible (CSV, PDF)
