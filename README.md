# Genelog - Projet Généalogie Familiale 🌳

## Description 
Genelog est un logiciel de gestion de généalogie familiale développé en **Python**.  
Il permet de **créer, visualiser et gérer** l’arbre généalogique d’une famille, développée avec **Interface graphique (Tkinter)** conviviale pour une visualisation claire et interactive.  
L’objectif est de fournir un outil **simple, intuitif et accessible**, même pour les utilisateurs non techniques.

---

## Contexte et objectifs 
- Centraliser les informations familiales (nom, prénom, date et lieu de naissance, liens familiaux...).  
- Représenter les relations familiales pour **préserver l’histoire familiale**.  
- Garantir la **sauvegarde et la confidentialité** des données.  
- Offrir une interface **claire et intuitive**.

---

## Fonctionnalités principales 
- Création, gestion et suppression de **comptes utilisateurs**.  
- Ajout, recherche et modification des **membres** de la famille.  
- Définition des **relations** : parents, enfants, conjoints.  
- Visualisation de l’arbre sous forme **textuelle ou graphique**.  
- **Sauvegarde** des données dans SQLite.  

### Problématiques à résoudre 
- Ergonomie et simplicité de l’interface graphique.  
- Organisation et gestion efficace des données.  
- Performance avec de grands arbres familiaux.  
- Sécurité et confidentialité des données.

---

## Fonctionnalités graphiques 
- Formulaire de **connexion** et création de compte.  
- **Boutons** pour ajouter, modifier ou rechercher un individu ou une famille.  
- Gestion des relations : parent, enfant, conjoint.  
- Affichage **graphique interactif** de l’arbre.  
- **Sauvegarde automatique** des données.

---


## Classes principales 

### Classe `Individu`
- Chaque membre de la famille.  
- **Attributs** : id, nom, prénom, sexe, date/lieu de naissance, occupation, décès, familles.  
- **Méthodes** : saisir conjoint/enfant, ajouter, modifier, afficher info/ascendants/descendants.

### Classe `Famille`
- Union entre deux individus et leurs enfants.  
- **Attributs** : id, date/lieu mariage, divorce, conjoints, enfants.  
- **Méthodes** : ajouter famille (première, par individu, par deux individus), modifier, afficher.

### Contraintes de validité ⚖️
- Date de décès ≥ date de naissance.  
- Date de mariage cohérente avec naissance/décès des conjoints.  
- L’enfant ne peut pas naître avant les parents.  
- Âge minimum pour mariage : 15 ans.  
- Unicité des identifiants.  
- Complétude des champs obligatoires.

---

## Processus d’utilisation 
1. **Connexion / Création de compte / Mot de passe oublié** 
2. **Page d’accueil** 
3. **Ajout d’un individu ou d’une famille**
4. **Recherche et modification**
5. **Déconnexion et suppression de généalogie** 

---

## Structure du projet

```text
PROJET_GENELOG
 |
 ├── __pycache__                
 ├── build                     
 ├── comptes                    # Données liées aux comptes utilisateurs
 ├── images                     # Ressources graphiques et photos des individus
 |
 ├── admin.db                   # Base de données SQLite
 ├── admin.py                   # Gestion de l’administration
 ├── ajouter_famille.py         # Ajout et gestion des familles
 ├── derby.log                  # Journal des erreurs de la base de données
 ├── famille.py                 # Logique métier des familles
 ├── genelog.py                 # Point d’entrée principal de l’application
 ├── genelog.spec               
 ├── icon.ico                   # Icône de l’application
 ├── individu.py                # Gestion des individus
 |
 ├── model.py                   # Modèle de données
 ├── rechercher.py              # Fonctionnalités de recherche
 └── rapport_genealogie.pdf     # Rapport final
```
---

### 📌 Remarque
- Le fichier **`genelog.py`** est le point d’entrée principal de l’application.  
- La base **`admin.db`** stocke toutes les informations généalogiques et utilisateurs.  
- La séparation entre **individu**, **famille** et **recherche** assure une architecture claire et maintenable.

---

## Aperçu

<p align="center">
  <img src="https://github.com/Fatimatou-DIALLO-87/Genelog/blob/master/genelog.gif" width="500">
</p>

## Informations de test 
- **Nom de la généalogie** : Diallo  
- **Mot de passe** : Fatima@123

---

## Perspectives d’évolution
- Exportation de l’arbre en **PDF** 
- Ajout de **photos et documents** pour chaque individu 
- Notes biographiques et documents familiaux 
- Version **multi-utilisateurs** avec base centralisée 

---
## Technologies utilisées 
- **Python** : logique et gestion des données.  
- **Tkinter** : interface graphique.  
- **SQLite** : stockage local et persistant.

---

## Auteurs 
- Diallo Fatimatou  
- Diallo Mamadou Talibe  
- Baldé Alpha Oumar  
- Baldé Mamadou Oury  

