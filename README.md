# Projet E-Commerce 🛒

Ce projet d'e-commerce est une plateforme en ligne permettant aux utilisateurs de parcourir et d'acheter des produits, tout en offrant des outils de gestion pour les administrateurs via un back-office dédié.

---

## 📋 Fonctionnalités principales

### Partie Front-Office
1. **Parcourir les produits** :
   - Visualisation des produits disponibles par catégories :
     - Fruits
     - Produits laitiers
     - TV
     - Cosmétiques/Maquillage
     - Légumes

2. **Gestion des utilisateurs** :
   - Les utilisateurs doivent se connecter pour acheter ou ajouter des produits dans leur panier.

3. **Panier d'achat** :
   - Ajouter des produits au panier.
   - Modifier les quantités des produits.
   - Valider une commande.

---

### Partie Back-Office
1. **Gestion des utilisateurs** :
   - Ajouter, modifier ou supprimer des utilisateurs.
   - Connexion sécurisée pour les administrateurs.

2. **Gestion des produits** :
   - Ajouter de nouveaux produits avec leurs détails.
   - Modifier ou supprimer les produits existants.

3. **Gestion des catégories** :
   - Ajouter, modifier ou supprimer des catégories.

4. **Gestion des commandes** :
   - Valider les commandes des utilisateurs.
   - Suivi des commandes passées.

5. **Administrateur** :
   - Interface dédiée pour la gestion complète du site.

---

## 📂 Structure des tables de la base de données

1. **`categorie`** :
   - Contient les catégories de produits (e.g., Fruits, Produits laitiers, TV, Cosmétiques/Maquillage, Légumes).

2. **`commande`** :
   - Structure :
     - `id` : Identifiant unique de la commande.
     - `id_client` : Référence au client ayant passé la commande.
     - `total` : Montant total de la commande.
     - `valide` : Statut de la commande (validée ou non).
     - `date_creation` : Date de création de la commande.

3. **`ligne_commande`** :
   - Structure :
     - `id` : Identifiant unique.
     - `id_produit` : Référence au produit commandé.
     - `id_commande` : Référence à la commande associée.
     - `prix` : Prix unitaire du produit.
     - `quantite` : Quantité commandée.
     - `total` : Montant total pour cet article.

4. **`produit`** :
   - Contient les informations sur les produits (nom, prix, description, catégorie, etc.).

5. **`utilisateur`** :
   - Contient les données des utilisateurs (nom, email, mot de passe, rôle, etc.).

---

## 🚀 Installation et configuration

### Prérequis
- Serveur local (XAMPP, WAMP, etc.).
- PHP 7.4 ou plus récent.
- MySQL pour la gestion de la base de données.
