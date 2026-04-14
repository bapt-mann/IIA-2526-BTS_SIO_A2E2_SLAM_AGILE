# 🧦 Projet Chaussettes Perdues 🧦

## Epic 1 : Mise en place du projet

### User Story 1 : Initialiser le projet Symfony
**En tant que** développeur  
**Je veux** créer le projet Symfony  
**Afin de** démarrer le développement  

#### ✅ DoR
- Version de Symfony choisie  
- Environnement prêt (PHP, Composer)  
- Accès à GitHub disponible  
- Structure du projet connue  

#### ✅ DoD
- Projet Symfony installé  
- Projet lancé en local sans erreur  
- Repo GitHub créé et lié  
- Premier commit effectué  

---

### User Story 2 : Mise en place de la BDD
**En tant que** développeur  
**Je veux** configurer la base de données  

#### ✅ DoR
- SGBD choisi (MySQL)  
- Accès BDD configuré  
- Schéma global identifié (Utilisateur, Chaussette)  
- Fichier `.env` prêt à être configuré  

#### ✅ DoD
- Base créée  
- Connexion Symfony ↔ BDD OK  
- Migrations fonctionnelles  
- Test de connexion validé  

---
---

## Epic 2 : Gestion des utilisateurs

### User Story 3 : Connexion Utilisateur
**En tant que** utilisateur  
**Je veux** me connecter avec un username  

#### ✅ DoR
- Champ username défini  
- Comportement défini :
  - username existant → connexion  
  - inexistant → création ou erreur  
- Gestion de session prévue  

#### ✅ DoD
- Champ username fonctionnel  
- Connexion possible  
- Session utilisateur active  
- Gestion des erreurs OK  

---
---

## Epic 3 : CRUD Chaussette

### User Story 4 : Créer une chaussette
**En tant que** utilisateur  
**Je veux** enregistrer une chaussette perdue  

#### ✅ DoR
- Champs définis :
  - taille, couleur(s), type, marque, commentaire, statut  
- Liste des types définie (+ “autre”)  
- Relation utilisateur ↔ chaussette définie  
- Formulaire identifié  
- Règle : utilisateur connecté requis  

#### ✅ DoD
- Formulaire fonctionnel  
- Données enregistrées en BDD  
- Multi-couleurs fonctionnel  
- Type “autre” fonctionnel  
- Lien utilisateur OK  
- Message de confirmation affiché  

---

### User Story 5 : Voir toutes les chaussettes
**En tant que** utilisateur  
**Je veux** voir toutes les chaussettes  

#### ✅ DoR
- Champs à afficher définis  
- Page liste identifiée  
- Source de données (BDD) définie  

#### ✅ DoD
- Liste affichée correctement  
- Données récupérées depuis BDD  
- Aucun crash si liste vide  
- Affichage lisible  

---

### User Story 6 : Voir mes chaussettes
**En tant que** utilisateur  
**Je veux** voir mes chaussettes  

#### ✅ DoR
- Filtre par utilisateur défini  
- Notion d’utilisateur connecté définie  
- Page dédiée prévue  

#### ✅ DoD
- Affichage uniquement des chaussettes du user  
- Vérification connexion OK  
- Message si aucune donnée  

---

### User Story 7 : Modifier une chaussette
**En tant que** utilisateur  
**Je veux** modifier mes chaussettes  

#### ✅ DoR
- Champs modifiables définis  
- Règle : propriétaire uniquement  
- Formulaire d’édition prévu  

#### ✅ DoD
- Modification fonctionnelle  
- Vérification propriétaire OK  
- Mise à jour en BDD  
- Message succès affiché  

---

### User Story 8 : Supprimer une chaussette
**En tant que** utilisateur  
**Je veux** supprimer mes chaussettes  

#### ✅ DoR
- Règle : propriétaire uniquement  
- Action (bouton supprimer) définie  
- Confirmation utilisateur prévue  

#### ✅ DoD
- Suppression fonctionnelle  
- Vérification propriétaire OK  
- Donnée supprimée en BDD  
- Message de confirmation affiché  

---
---

## Epic 4 : Tri et filtre

### User Story 9 : Filtrer les chaussettes
**En tant que** utilisateur  
**Je veux** filtrer les chaussettes perdues  

#### ✅ DoR
- Champs filtrables définis :
  - taille, couleur, type, marque, statut  
- Formulaire de filtre conçu  
- Logique de requête définie  

#### ✅ DoD
- Formulaire fonctionnel  
- Résultats filtrés correctement  
- Gestion des cas sans résultat  
- Performance acceptable  

---

### User Story 10 : Trier les chaussettes
**En tant que** utilisateur  
**Je veux** trier les chaussettes perdues  

✅ DoR
Champs triables définis (ex : date)
Ordres définis (ASC/DESC)
UI de sélection prévue
✅ DoD
Tri fonctionnel
Ordre respecté
Aucun bug sur affichage

---
---

## Epic 5 : Pages spécifiques

### User Story 11 : Page chaussettes en couple
**En tant que** utilisateur  
**Je veux** voir les chaussettes en couple  

#### ✅ DoR
- Statut “couple” défini en BDD  
- Filtre associé défini  
- Page dédiée prévue  

#### ✅ DoD
- Affichage uniquement des chaussettes en couple  
- Données correctes  
- Message si aucune  

---

### User Story 12 : Page chaussettes célibataires
**En tant que** utilisateur  
**Je veux** voir les chaussettes seules  

#### ✅ DoR
- Statut “célibataire” défini  
- Filtre associé défini  
- Page dédiée prévue  

#### ✅ DoD
- Affichage uniquement des chaussettes seules  
- Données correctes  
- Message si aucune  

---
---

## Epic 6 : Interface utilisateur

### User Story 13 : Interface responsive
**En tant que** utilisateur  
**Je veux** utiliser le site sur mobile  

#### ✅ DoR
- Breakpoints définis (mobile/tablette)  
- Pages principales identifiées  
- Contraintes UX connues  

#### ✅ DoD
- Site responsive  
- Navigation fluide  
- Aucun débordement visuel  
- Lisibilité correcte sur mobile  