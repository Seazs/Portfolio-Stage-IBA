---
title: week3
draft: 
tags:
---

Comme expliqué dans les précédents rapports, j'ai commencé la semaine passée par une réunion avec le client pour voir mon avancée dans le projet, les points bloquants et ce sur quoi je devrais me pencher durant la semaine.

  

Ça peut être dur d'avoir une réunion le lundi a 9h mais je trouve que c'est une bonne manière de commencer la semaine. Ça permet de se rappeler où l'on s'était arrêté et de lancer la semaine avec des objectifs claires. 

  

La semaine passée, je voulais trouver une manière d'optimiser l'espace de stockage de mon application. Pour être plus précis, le launcher d'applications pythons que je développe, télécharge et installe ces applications. Lorsque les dépendances (librairies externes) de ces applications ne sont pas compatibles, il faut créer deux environnement pythons séparés afin d'y installer les 2 versions de la librairie problématique.

  

Créer un environnement différent par applications est la solution la plus basique. Mais on se retrouve avec un système où chaque applications peut prendre jusque 700MB, et ceci pour de simples scripts python qui affichent des graphiques.

Tout le but est donc d'arriver à minimiser le nombre d'environnement crée.

  

Je n'ai pas réussi à trouver de solutions d'optimisations la semaine passée. Mais j'ai néanmoins pu évaluer les avantages et inconvénients de l'utilisations d'outils comme _pyenv_ et _pipx_ dans le cadre de ce projet.

  

La réunion de ce matin avec mon superviseur, de retour de vacances, et Valentin, notre "Client" interne, a permis de concevoir une nouvelle architecture. Celle-ci s'inspirerait du fonctionnement de Maven pour la gestion des dépendances en Java. Nous envisagerions de créer un répertoire où chaque version des dépendances nécessaires serait installée. Chaque application pourrait ensuite créer son environnement personnalisé en sélectionnant les dépendances appropriées dans ce répertoire.

  

Étant donné que la majorité de l'espace occupé par un environnement provient des dépendances, cette approche permettrait d'éviter les doublons, en empêchant d'avoir plusieurs fois la même version d'une dépendance.

C'est donc sur cela que je vais travailler cette semaine.