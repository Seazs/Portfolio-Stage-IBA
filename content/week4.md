---
title: week4
draft: 
tags:
---

En début de semaine dernière, j'avais évoqué avec mon superviseur une nouvelle architecture que nous avions imaginée. Cette architecture devait permettre d'optimiser l'espace de stockage de notre application en utilisant un cache central, évitant ainsi la duplication de nombreux fichiers. Cependant, après une première tentative d'implémentation, nous avons constaté la difficulté d'implémenter cette architecture manuellement.

Indépendamment de cela, une réunion de synchronisation pour tous les membres du département est normalement prévue chaque mardi. Toutefois, durant les vacances, les projets avançant moins vite, cette réunion est souvent annulée. La semaine dernière, le directeur des ressources humaines du département a maintenu la réunion afin que je présente mon projet et son avancement. En effet, bien que je travaille aux côtés de mes collègues, ils ne sont pas toujours au courant de ce que je fais.

J'ai donc profité de cette réunion pour demander des conseils sur le problème d'optimisation auquel je faisais face.

Une petite dizaine de personnes étaient présentes lors de la réunion, et j'ai été étonné de constater qu'elles se sont toutes réellement intéressées au problème, en proposant des solutions potentielles.

Pendant la réunion, personne n'a proposé d'idée à laquelle mon superviseur et moi n'avions pas déjà pensé. Cependant, deux jours plus tard, un collègue est venu me parler d'un nouvel outil de gestion d'environnement Python : `uv`. Bien qu'il n'existe que depuis février, l'outil est déjà très complet et répond exactement à nos besoins. Notamment, il permet une optimisation de l'espace de stockage grâce à un cache central pour toutes les bibliothèques externes installées. Ensuite, pour chaque environnement nécessitant une bibliothèque, l'outil utilise des hard links afin d'éviter de simplement copier les fichiers.

Jeudi et vendredi derniers, j'ai donc approfondi les possibilités offertes par cet outil et j'ai implémenté une architecture l'utilisant.

Cette semaine sera courte car, à partir de mercredi, je vais prendre un congé pour préparer mon examen de lundi prochain. Je me suis arrangé avec le responsable des ressources humaines pour rattraper ces jours à la fin de mon stage.