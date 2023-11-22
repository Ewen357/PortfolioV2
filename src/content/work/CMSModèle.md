---
title: Site modèle e-commerce
publishDate: 2023-05-05 00:00:00
img: /assets/AtoutGraph-logo.jpg
img_alt: Projet de stage
description: |
  Développer un site modèle e-commerce avec gestion de contenu graçe au Framework Symfony
tags:
  - Stage
  - Symfony
  - Ecommerce
---
#### Contexte
Dans le cadre d'une réorganisation du pôle de développement web suite au départ d'une partie de l'équipe, nous avons entrepris un projet visant à créer un modèle de CMS en PHP/Symfony en se basant sur le modèle déjà existant. 

Cette initiative est motivée par plusieurs problématiques rencontrées avec le modèle existant en PHP natif, notamment la difficulté de coder en équipe, le manque de structure du code, la complexité de la maintenance de l'évolutivité et beaucoup de bugs.

#### Technologies

PHP, HTML, CSS, Javascript, IDE VisualStudio, PHPMyAdmin.

#### Maquettes

[Maquettes format PC et Mobile](/assets/CMS-Maquettes.pdf)


#### Diagrammes

[Diagrammes](/assets/CMS-Diagramme.pdf)


#### Itérations

##### Les membres
■ Création de notre première entité : User().<br>
■ Création de notre formulaire d'inscription.<br>
■ Sauvegarder les informations du formulaire en base de donnée.<br>
■ Encodage des mots de passe de nos utilisateurs.<br>
■ Création de notre formulaire de login.<br>
■ Les vues privées : L'espace membre de l'utilisateur.<br>
■ Création de la mécanique de mot de passe oublié.<br>

##### Gestion de contenu
■ Installation, configuration et mapping de EasyAdmin avec l'entité User().<br>
■ Création de l'entité Category() pour organiser nos produits.<br>
■ Mapping de l'entité Category() dans EasyAdmin.<br>
■ Création de l'entité Product().<br>
■ Mapping de l'entité Product() dans EasyAdmin.<br>
■ Création des produits dans le backoffice.<br>
■ Création des vues pour afficher nos produits à nos utilisateurs.<br>
Ajouter une fonctionnalité de gestion du header depuis le backoffice.<br>

##### Navigation
■ Création d'une barre de filtre produit pour faciliter la navigation.<br>
■ Mettre des produits à la une pour les afficher sur la homepage.<br>

##### Panier
■ Création du panier et de notre classe Cart().<br>
■ Création de la vue récapitulatif panier avant l'entrée en tunnel d'achat.<br>
■ Ajout, diminution et suppression de produit dans panier.<br>

##### Commande
■ Création de l'entité Address() pour les adresses de nos utilisateurs.<br>
■ Ajouter, modifier, supprimer une adresse depuis l'espace membre de l'utilisateur.<br>
■ Création de l'entité Carrier() pour stocker nos transporteurs.<br>
■ Création de l'entité Order() et OrderDetails().<br>
■ Afficher les commandes dans l'espace membre de nos utilisateurs.<br>
■ Tunnel d'achat : Choix de l'adresse de livraison.<br>
■ Tunnel d'achat : Choix du transporteur.<br>
■ Tunnel d'achat : Sommaire de la commande et ajout de style.<br>
■ Tunnel d'achat : Stocker les informations de la commande en base.<br>

##### Paiement
■ Installation de Stripe dans notre projet graçe à l'API.<br>
■ Intégration de Stripe dans notre tunnel d'achat.<br>
■ Ajout de la livraison dans les informations envoyées à Stripe.<br>
■ Création des vues "Merci pour votre commande" / "Echec de paiement".<br>

##### Mail
■ Intégration de la librairie Mailjet dans notre projet Symfony.<br>

##### Sécurité
■ Sécuriser l'accès à notre backoffice pour les administrateurs.<br>

##### Test
■ Test unitaire de l'entitée Product.<br>
■ Test Fonctionnel du fichier "CartController.php", méthode d’ajout d’un produit au panier "add()".<br>

##### Dev
■ Mise en place de commandes personnalisés.<br>
■ Mise en place de fixtures.<br>

##### Prod
■ Mise en production du site.<br>

#### Rendu visuel	

<!DOCTYPE html>
<html>
<head>
<style>
  .hover-zoom {
    transition: transform 0.3s;
  }

  .hover-zoom:hover {
    transform: scale(2);
    position: relative;
    z-index: 1;
  }
</style>
</head>
<body>
<img src="/assets/CMS-Accueil.jpg" alt="Page d'Accueil" class="hover-zoom">
<img src="/assets/CMS-MonCompte.jpg" alt="Mon compte" class="hover-zoom">
<img src="/assets/CMS-Produits.jpg" alt="Les produits" class="hover-zoom">
<img src="/assets/CMS-Admin.jpg" alt="Gestion du contenu" class="hover-zoom">
</body>
</html>
 