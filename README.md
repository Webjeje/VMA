

# Calculateur multi-tests VMA – WebApp

## 📖 Mode d’emploi

Cette application permet de réaliser différents tests d’endurance progressive (Luc Léger, VAMEVAL, Universitaire, etc.) et de calculer automatiquement la VMA (Vitesse Maximale Aérobie) ainsi que la VO₂max. Elle s’utilise en ligne, directement depuis un navigateur, sans installation.

### 1. Démarrage

* Ouvrir l’application :
  [Calculateur VMA en ligne](https://www.webjeje.com/online/webapp/leger/leger.html)
* Choisir un protocole prédéfini dans la liste déroulante (Luc Léger, VAMEVAL, Universitaire) ou sélectionner **Personnalisé** pour définir vos propres paramètres.

### 2. Réglages disponibles

* **Vitesse initiale (km/h)** : vitesse de départ du test.
* **Incrémentation (km/h)** : augmentation de la vitesse à chaque palier.
* **Durée du palier (secondes)** : durée de chaque palier.
* **Distance entre repères (m)** : distance entre les cônes ou repères.
* Bouton **Mettre à jour les paramètres** : génère le tableau des temps de passage selon vos choix.

### 3. Déroulement du test

* **Start** : lance le chronomètre et masque les réglages.
* **Stop** : arrête le test et demande le poids de l’élève/sportif pour calculer les résultats.
* **Reset** : remet le test à zéro et réaffiche les réglages.

Pendant le test :

* Un **bip numérique** est émis à chaque temps de passage.
* Le chronomètre est synchronisé avec le tableau des paliers.
* Le mode **Focus** affiche uniquement le palier et le temps en cours.
* Le mode **Tout** affiche l’intégralité du tableau, avec la ligne active mise en avant.

### 4. Résultats

À l’arrêt du test (**Stop**) :

* **VMA** : vitesse maximale atteinte (calculée avec crédit partiel dans le palier si interrompu avant la fin).
* **VO₂max relative** : exprimée en ml/kg/min (formule : VMA × 3,5).
* **VO₂max absolue** : exprimée en L/min (ajustée en fonction du poids).

Les résultats apparaissent directement sous les paramètres.

---

## 🔧 Analyse technique

### Technologies utilisées

* **HTML5 / CSS3** pour la structure et le design.
* **JavaScript Vanilla** pour la logique du chronomètre, le calcul des temps de passage et les résultats.
* **Web Audio API** pour générer un bip numérique à chaque repère, sans fichier externe.

### Fonctionnalités principales

1. **Chronomètre synchronisé** :

   * Gestion du temps écoulé en secondes.
   * Comparaison en direct avec les temps de passage calculés.

2. **Tableau dynamique des paliers** :

   * Généré automatiquement selon les paramètres ou le protocole sélectionné.
   * Mise en surbrillance du temps atteint et prévisualisation du temps suivant.
   * Mode “Focus” (HUD simplifié) et mode “Tout” (tableau complet avec scroll auto).

3. **Résultats automatiques** :

   * Détermination du dernier palier atteint.
   * Crédit partiel intégré si le test s’arrête avant la fin du palier.
   * Conversion directe en VO₂max relative et absolue.

4. **UI/UX optimisée** :

   * Mode sombre, responsive (PC, tablette, smartphone).
   * Inputs agrandis ×3 pour une meilleure lisibilité.
   * Boutons uniformisés (radius 2px).
   * Soft pulse (animation douce) lors du changement de palier.

### Protocoles intégrés

* **Luc Léger (20 m)** : départ à 8 km/h, +0.5 km/h/min, repères 20 m.
* **VAMEVAL (50 m)** : départ à 8 km/h, +0.5 km/h/min, repères 50 m.
* **Universitaire (20 m)** : départ à 8 km/h, +1 km/h/120 s, repères 20 m.
* **Personnalisé** : libre configuration.

### Avantages par rapport aux supports classiques

* Plus besoin de **tableaux de correspondance papier**.
* Pas d’**installations complexes** pour caler les vitesses.
* Visualisation claire, bip sonore intégré, résultats immédiats.

---

## 🚀 Installation / Usage

* Application 100 % web : fonctionne directement depuis un navigateur récent (Chrome, Edge, Firefox, Safari).
* Aucun cookie, aucune donnée personnelle enregistrée.
* Fonctionne hors ligne après premier chargement (PWA possible).

