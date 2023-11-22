---
title: BDENI
publishDate: 2023-02-02 00:00:00
img: /assets/logoBDENI.jpg
img_alt: Logo BDENI
description: |
  Monter une plateforme web destinée aux stagiaires en formation ainsi qu aux 
  anciens stagiaires et permettant l’organisation de sorties sur le temps hors formation.
tags:
  - Symfony
  - PHP
  - MVC

---
#### Contexte

En tant que second projet réalisé dans le cadre de ma formation en Développeur Web & Web Mobile, notre équipe de trois personnes a conçu cette application en seulement deux semaines.

Notre objectif était de concevoir une application web fonctionnelle en accord avec les directives établies par l'école. Cette application, construite en utilisant les langages PHP, JavaScript, HTML, et CSS, avec l'utilisation du framework Symfony, permet aux utilisateurs de planifier des activités en dehors de leurs heures de formation.

#### Technologies

PHP, HTML, CSS, Javascript, IDE PHPStorm,PHPMyAdmin.

#### Maquettes

[Maquettes format PC](/assets/SortiesDesktop.pdf)

[Maquettes format Mobile](/assets/SortiesSmartphone.pdf)

#### Diagrammes

[Diagramme état sortie](/assets/DiagEtatSortie.pdf)

[Diagramme de classe sortie](/assets/DiagClasse.pdf)

#### Itérations

##### Gestion des utilisateurs

■ En tant qu'utilisateur, je peux me connecter sur la plateforme sortir.com avec un login (adresse mail ou pseudo) et un mot de passe.<br>
■ En tant qu'utilisateur, je peux choisir d'enregistrer mon login sur mon ordinateur pour ne pas avoir à le resaisir.<br>
■ En tant qu’utilisateur, je peux gérer mes informations de profil, notamment mon nom, prénom, pseudo, email, mot de passe, et téléphone. Le pseudo doit être unique entre tous les participants.<br>
■ En tant que participant je peux afficher le profil des autres participants. Cette fonctionnalité est notamment disponible sur la page d’affichage des sorties et sur la page qui affiche les détails de la sortie.<br>
■ En tant que participant je peux uploader une photo pour être affichée dans ma page Profil.<br>
■ En qu'administrateur, je peux inscrire plusieurs utilisateurs via l'intégration d'un fichier .csv.<br> 
■ En tant qu'administrateur, je peux créer un nouvel utilisateur par un écran d'administration avec saisie manuelle des informations.<br>
■ En tant qu'utilisateur, je peux faire une demande de ré-initialisation de mot de passe. La plateforme créé un lien vers un écran de saisie du nouveau mot de passe. (Ce lien sera envoyé par mail à l'utilisateur. L'envoi par mail n'est pas demandé)<br>
■ En tant qu'administrateur, je peux rendre inactifs ou actifs des utilisateurs sélectionné dans une liste d'utilisateurs. Un utlisateur inactif ne peut pas se connecter à l'outil.<br>
■ En tant qu'administrateur, je peux supprimer des utilisateurs sélectionné dans une liste d'utilisateurs.<br>

##### Gestion des sorties

■ En tant que participant, je peux lister les sorties publiées sur chaque campus, celles auxquelles je suis inscrit et celles dont je suis l’organisateur. Je peux filtrer cette liste suivant différents critères (voir maquette écran).<br>
■ En tant que partipant je peux consulter les informations d'une sortie.<br>
■ En tant que participant je peux ajouter des lieux dans la plateforme.<br>
■ En tant qu'organisateur d'une sortie, je peux créer une nouvelle sortie ( définir un nom pour la sortie, une date et heure, une durée, un lieu (nom, adresse, gps), un nombre limite de participants, une note textuelle, et une date limite d'inscription ).<br>
■ En tant que participant, je peux m’inscrire à une sortie. Il faut que la sortie ai été publiée (ouverte),  que la date limite d’inscription ne soit pas dépassée et qu'il reste des places libres.<br>
■ En tant que participant inscrit à une sortie, je peux me désister tant que la sortie n'a pas débuté. En cas de désistement, la place devient libre pour un autre participant si la date limite d'inscription n'est pas dépassée.<br>
■ En tant qu'organisateur je peux modifier les informations d'une sortie.<br>
■ En tant qu'organisateur d'une sortie, je peux annuler une sortie si celle-ci n'est pas encore commencée. La sortie sera alors marquée comme annulée et sera accompagnée d'un motif d'annulation. Le motif d'annulation est rajouté dans la description de la sortie.<br>
■ Les sorties réalisées depuis plus d’un mois ne sont pas consultables. L'état des sorties devient "Historisée".<br>
■ En tant qu'administrateur, je peux annuler une sortie qui a été proposée par un autre participant.<br>
■ En tant qu'admin je peux ajouter des villes utilisables dans la plateforme (une ville est toujours associée à un code postal).<br>
■ En tant qu'admin je peux ajouter des campus utilisables dans la plateforme.<br>

##### Navigation

■ En tant que participant, je peux utiliser un petit écran de type smartphone pour afficher les sorties de mon campus de rattachement. Dans la version petit écran, la plateforme ne permet pas de créer des sorties.<br>
■ En tant que participant, je peux utiliser la plateforme avec un  écran de taille moyenne de type tablette. Les fonctionnalités sont les mêmes que l’utilisation sur grand écran de type ordinateur de bureau.<br>

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
<img src="/assets/BDENI-Accueil.jpg" alt="Page d'Accueil" class="hover-zoom">
<img src="/assets/BDENI-MonProfil.jpg" alt="Mon profil" class="hover-zoom">
<img src="/assets/BDENI-NewSortie.jpg" alt="Nouvelle sortie" class="hover-zoom">
<img src="/assets/BDENI-Campus.jpg" alt="Gerer les campus" class="hover-zoom">
</body>
</html>
 
