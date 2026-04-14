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

#### 🎯 Critères d’acceptation
**Given** un environnement PHP + Composer installé
**When** le projet Symfony est créé
**Then** l’application se lance sans erreur en local
**Given** un repository GitHub vide
**When** le projet est push
**Then** le code est visible sur GitHub

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

#### 🎯 Critères d’acceptation

**Given** une base MySQL configurée
**When** Symfony est configuré avec la base
**Then** la connexion à la base fonctionne

**Given** une migration exécutée
**When** la base est créée
**Then** les tables sont visibles en base

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

#### 🎯 Critères d’acceptation

**Given** un username existant  
**When** l’utilisateur se connecte  
**Then** une session utilisateur est créée  

**Given** un username inexistant  
**When** l’utilisateur tente de se connecter  
**Then** un message d’erreur ou création est déclenché  

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

#### 🎯 Critères d’acceptation

**Given** un utilisateur connecté  
**When** il remplit le formulaire  
**Then** la chaussette est enregistrée en base  

**Given** plusieurs couleurs sélectionnées  
**When** la chaussette est créée  
**Then** toutes les couleurs sont sauvegardées  

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

#### 🎯 Critères d’acceptation

**Given** des chaussettes en base  
**When** l’utilisateur ouvre la page  
**Then** toutes les chaussettes sont affichées  

**Given** aucune chaussette  
**When** la page est ouverte  
**Then** un message “aucune donnée” est affiché  

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

#### 🎯 Critères d’acceptation

**Given** un utilisateur connecté  
**When** il ouvre la page “mes chaussettes”  
**Then** seules ses chaussettes sont affichées  

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

#### 🎯 Critères d’acceptation

**Given** une chaussette appartenant à l’utilisateur  
**When** il modifie la chaussette  
**Then** les modifications sont enregistrées en base  

**Given** une chaussette qui ne lui appartient pas  
**When** il tente de la modifier  
**Then** l’accès est refusé 

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


#### 🎯 Critères d’acceptation

**Given** une chaussette appartenant à l’utilisateur  
**When** il supprime la chaussette  
**Then** la chaussette est supprimée de la base  

**Given** une chaussette non autorisée  
**When** il tente de la supprimer  
**Then** l’action est bloquée

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

#### 🎯 Critères d’acceptation

**Given** plusieurs chaussettes en base  
**When** un filtre est appliqué (taille, couleur, type, marque, statut)  
**Then** seuls les résultats correspondants sont affichés  

**Given** aucun résultat  
**When** un filtre est appliqué  
**Then** un message “aucun résultat” est affiché  

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

#### 🎯 Critères d’acceptation

**Given** des chaussettes en base  
**When** un tri est appliqué (ASC ou DESC)  
**Then** les résultats sont affichés dans le bon ordre  

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

#### 🎯 Critères d’acceptation

**Given** des chaussettes avec statut “couple”  
**When** la page est ouverte  
**Then** seules les chaussettes en couple sont affichées 

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

#### 🎯 Critères d’acceptation

**Given** des chaussettes avec statut “célibataire”  
**When** la page est ouverte  
**Then** seules les chaussettes célibataires sont affichées  

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

#### 🎯 Critères d’acceptation

**Given** un écran mobile  
**When** l’utilisateur navigue sur le site  
**Then** l’affichage s’adapte correctement  

**Given** un écran tablette  
**When** la page est affichée  
**Then** aucun élément ne déborde  