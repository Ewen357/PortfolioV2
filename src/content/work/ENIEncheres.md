---

title: ENI Enchères
publishDate: 2021-01-12 00:00:00
img: /assets/Enchères.svg
img_alt: Page d'accueil d'ENI Enchères
description: |
  L’association « Les objets sont nos amis » désire monter une plateforme web pour permettre 
  la cession d’objets de seconde main sans échanges financiers. La valeur des articles sera 
  déterminée par un système d’enchères basée sur un nombre de points. Les points sont 
  gagnés en vendant des objets, puis peuvent être utilisés pour acquérir d’autres objets.
tags:
  - Java EE
  - SQL
  - MVC
---
#### Contexte

En tant que premier projet réalisé dans le cadre de ma formation en Développeur Web & Web Mobile, notre équipe de trois personnes a conçu cette application en seulement deux semaines.

Nous avions pour objectif de créer une application web fonctionnelle conforme à un cahier des charges fourni par l'école. Cette application, développée en Java, JavaScript, HTML et CSS, offre aux utilisateurs la possibilité de mettre en vente des objets de seconde main via un système de vente aux enchères. De plus, elle intègre une monnaie virtuelle interne dédiée aux transactions effectuées au sein de l'application.

#### Technologies

Java, SQL, HTML, CSS, SQLServer, IDE Eclipse.

#### Maquettes

[Maquettes format PC](/assets/MaquettesDesktopEncheres.pdf)

[Maquettes format Mobile](/assets/MaquettesMobilesEncheres.pdf)

#### Diagrammes

[Diagramme état vente](/assets/DiagEtatVente.pdf)

[Diagramme de classe enchères](/assets/DiagClasseEncheres.pdf)

#### Itérations

##### Gestion des utilisateurs

■ En tant qu'utilisateur, je peux me connecter sur la plateforme Enchères.org avec un login (adresse mail ou pseudo) et un mot de passe.<br>
■ En tant qu’utilisateur, je peux m’inscrire sur la plateforme Enchères.org. Le pseudo doit être unique sur toute la plateforme, ainsi que l’email. Le pseudo n’accepte que des caractères alphanumériques. Si la création du profil est validée, l’utilisateur est dirigé vers la page d’accueil (liste des enchères). Un crédit initial de 100 points est alloué à la création du compte.<br>
■ En tant qu’utilisateur connecté, je peux me déconnecter. Je suis alors ramené vers la page d’accueil en mode déconnecté.
Afficher un profil	En tant qu’utilisateur, je peux afficher le profil d’un utilisateur. Le pseudo, nom, prénom, email, téléphone, rue, code postal, ville sont affichés.<br>
■ En tant qu’utilisateur, je peux modifier mes informations de profil : Pseudo, Nom, prénom, email, téléphone, rue, code postal, ville, et mot de passe.<br>
■ En tant qu’utilisateur, je peux supprimer mon compte. Dans ce cas je suis déconnecté et retourné à la page d’accueil.<br>
■ En tant qu'utilisateur, je peux choisir d'enregistrer mon login sur mon ordinateur pour ne pas avoir à le ressaisir à la connexion suivante.<br>
■ En tant qu'utilisateur, je peux faire une demande de ré-initialisation de mot de passe. La plateforme créé un lien vers un écran de saisie du nouveau mot de passe.<br>
■ En tant qu’utilisateur, je peux choisir la langue utilisée sur la plateforme. J’ai le choix entre français et anglais.<br>
■ A la date de fin d’enchère, un traitement batch calcule le prix de vente et notifie l’acheteur par mail.<br>
■ En tant qu’utilisateur, je peux acheter des crédits.<br>

##### Gestion des enchères

■ En tant qu’utilisateur, je peux vendre un article sur la plateforme ENI-Enchères. Pour cela je donne les informations sur l’article vendu : nom, description et catégorie j’indique un prix de départ ( en points ), une date et une heure d’ouverture de l’enchère, une date et une heure de fin d’enchères et les modalités du retrait :  adresse (par défaut celle du vendeur).<br>
■ En tant qu’utilisateur non connecté, je peux lister les enchères en cours. Je peux filtrer ma recherche par catégorie, et par nom d’article (l’article est affiché si il contient le critère saisi) – Pour consulter le détail des enchères, l’utilisateur doit se connecter.<br>
■ En tant qu’utilisateur connecté, je peux lister les enchères en cours, les enchères auxquelles je participe, c’est à dire celles sur lesquelles j’ai fait au moins une offre, et mes enchères gagnées. Je peux aussi sélectionner mes ventes, non commencées, en-cours ou terminées.<br>
■ En tant qu’utilisateur, je peux faire une enchère sur un article si je propose un prix (en points) supérieur au tarif actuel et si mon compte de points ne devient pas négatif. Si l’enchère est possible, mon crédit de points est débité du montant proposé. Le meilleur enchérisseur précédent si il existe est re-crédité de son offre.<br>
■ En tant qu’enchérisseur, je deviens acquéreur si au terme de l’enchère j’ai proposé l’enchère la plus haute.<br>
■ Afficher le détail d’une enchère	En tant qu’utilisateur, je peux afficher le détail d’une enchère. Les informations sur l’article vendu sont affichés ( nom, description, meilleure offre, mise à prix, début et fin de l’enchère, adresse de retrait, vendeur. En fonction de l’état de la vente, et du rôle de l’utilisateur (vendeur ou acheteur), l’utilisateur peux seulement consulter les information, enchérir, ou modifier la vente (si il est le vendeur et que l’enchère n’a pas débuté).<br>
■ Modifier une vente	En tant que vendeur, je peux modifier les informations liées à ma vente tant que la date de début d’enchère n’est pas arrivée.<br>
■ Annuler une vente	En tant que vendeur d’un article, je peux annuler cette vente tant que la date de début d’enchère n’est pas arrivée.<br>
■ Photo pour la vente	en tant que vendeur, je peux uploader une photo de l’article à vendre. Celle ci sera visible sur le détail de la vente.<br>
■ En tant que vendeur, je peux voir la liste des enchérisseurs de mes ventes. Les enchérisseurs sont triés en fonction du montant de leur dernière enchère par ordre décroissant.<br>

##### Navigation

■ Un click sur le logo du site ramène l’utilisateur sur la page principale (page de recherche d’articles) si celui-ci est connecté.<br>	
■ En tant qu’utilisateur, je peux rafraîchir la page courante ou revenir sur la page précédente en utilisant le bouton « back » du navigateur.<br>
■ Sur la page permettant de lister les enchères suivant des critères de recherche, j’affiche un nombre d’enchères maximum ( 6) et  j’accède  aux autres pages résultat par l’intermédiaire de liens numérotés.<br>

##### Responsive Web Design

■ Les fonctionnalités sont accessibles depuis un petit appareil de type smartphone connecté au web. Cf maquettes<br>

##### Sécurité

■ Sessions utilisateur de 5mn	L’utilisateur doit être déconnecté automatiquement après 5 minutes d’inactivité.<br>
■ Supprimer des comptes utilisateurs	En tant qu’administrateur, je peux supprimer des comptes utilisateurs.<br>
■ En tant qu’administrateur, je peux désactiver un compte utilisateur. Toutes les ventes proposées par cet utilisateur sont alors annulées, toutes les enchères faites par cet utilisateur sont elles aussi annulées, l’utilisateur ne peut pas créer de nouvelles ventes ou faire de nouvelles enchères.<br>
■ En tant que développeur ou support informatique, j’ai accès à des fichiers de logs côté serveur me permettant d’avoir des informations détaillées sur les éventuelles erreurs en production, et des informations de tracing plus précises en phase de recette et de développement.<br>
■ En tant qu’administrateur, je peux gérer, c’est à dire ajouter, supprimer, modifier les catégories d’articles.<br>

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
<img src="/assets/Enchères-Accueil.jpg" alt="Page d'Accueil" class="hover-zoom">
<img src="/assets/Enchères-Connexion.jpg" alt="Page de connexion" class="hover-zoom">
<img src="/assets/Enchères-ModifierProfil.jpg" alt="Page de modification de profil" class="hover-zoom">
<img src="/assets/Enchères-Vente.jpg" alt="Page de création d'une vente" class="hover-zoom">
</body>
</html>
