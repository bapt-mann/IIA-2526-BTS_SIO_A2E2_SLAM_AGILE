### 🟢 Sprint 4 — Sprint de finition & excellence produit

# 🎯 Sprint Goal

        Transformer une application fonctionnelle en produit abouti, agréable et robuste :

        Offrir une expérience utilisateur fluide et intuitive
        Rendre l’application totalement responsive (mobile-first)
        Améliorer la qualité technique (clean code + performance)
        Sécuriser et fiabiliser les fonctionnalités
        Préparer une démonstration professionnelle

### 📱 1. Responsive & Mobile-first

            - Passage en logique mobile-first
            - Refonte des pages critiques :
            - Liste des chaussettes
            - Formulaire (UX tactile)
            - Ajout d’un menu burger
            - Optimisation des zones cliquables (UX mobile)
            Test sur :
            - mobile réel
            - simulateur navigateur

### 🎨 2. Expérience utilisateur

            - Ajoute de feedback instantané
                - loadin spinner
                - confirmation visuelle
            - Mise en place de flash messages dynamiques
            - Ajout de micro-interactions :
                - hover
                - transition
            - Simplification des parcours utilisateurs :
                - Moins de clics
                - actions plus visibles
            👉 Objectif : réduire la friction utilisateur

### 3. Performance & optimisation

            - Optimisation des requêtes Doctrine :
                - éviter les requêtes inutiles
                - jointures optimisées

            - Mise en cache simple (si possible)

            - Réduction du poids CSS/JS
            - Chargement plus rapide des pages

        👉 Objectif : application rapide et fluide

5. Sécurité & robustesse
   Vérification des accès :
   utilisateur propriétaire uniquement
   Protection des formulaires (CSRF)
   Validation des données (backend + frontend)
   Gestion des erreurs :
   pages propres
   messages clairs

👉 Objectif : application fiable et sécurisée

### 6. Tests & stabilisation

Tests manuels complets :
parcours utilisateur complet
Tests des cas limites :
liste vide
erreurs formulaire
Correction des bugs
Validation finale

👉 Objectif : zéro bug critique

### 🎬 7. Préparation démo & “effet wow”

Ajout de données réalistes (fixtures)
Scénario de démo préparé :
login
ajout chaussette
filtre
suppression
Vérification du timing démo
Nettoyage UI final

👉 Objectif : impressionner le jury

### 📅 Daily Meeting (version réaliste + pro)

# Jour 1

Audit UX + responsive
Début refonte mobile
❌ Problème : structure CSS peu adaptée → refonte nécessaire

# Jour 2

Responsive avancé
Menu mobile fonctionnel
❌ Problème : conflits CSS

# Jour 3

Amélioration UX (messages, feedback)
Ajout interactions
❌ Problème : incohérence visuelle entre pages

# Jour 4

Refactorisation code (services)
Nettoyage controllers
❌ Problème : régressions fonctionnelles

# Jour 5

Optimisation performances
Correction bugs critiques
❌ Problème : requêtes trop lentes

# Jour 6

Tests complets
Stabilisation
Correction finale

# Jour 7

Préparation démo
Nettoyage final
Répétition présentation

### 🔁 Sprint Retrospective

# 👍 Keep

Bonne progression technique
Amélioration visible de l’application
Meilleure organisation du code

# 👎 Drop

Manque d’anticipation du responsive
Refactorisation tardive

# 🚀 Try

Intégrer le responsive dès le début
Mettre en place des tests plus tôt
Adopter une architecture propre dès Sprint 2
