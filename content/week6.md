---
title: week6
draft: 
tags:
---

La semaine dernière, lors de notre réunion hebdomadaire avec mon superviseur et le client, nous avons défini en détail les besoins des utilisateurs pour l'installeur de notre application. Il s'agissait de préciser toutes les options que l'utilisateur devrait pouvoir sélectionner lors de l'installation.

Suite à cela, j'ai commencé à approfondir mes connaissances sur Inno Setup, un outil permettant de créer des installeurs pour Windows, et j'ai implémenté une première version assez simplifiée de cet installeur.

C'était plus complexe que prévu. En général, pour des besoins basiques, la création d'un installeur peut se faire via une interface graphique. Cependant, dans notre cas, la procédure est plus spécifique et nécessite une implémentation sous forme de code, utilisant un langage basé sur le Pascal, que je ne maîtrisais pas auparavant. Ce langage présente de nombreuses particularités propres à Inno Setup, et j'ai trouvé que la documentation était peu clair, ce qui rend le développement assez fastidieux. De plus, cette tâche est, à mon sens, moins stimulante.

Par ailleurs, nous avons eu l'idée de rendre cet installeur adaptable, non seulement pour notre application, mais pour n'importe quelle application Python. Pour cela, j'ai introduit des paramètres lors de la création de l'installeur, et j'ai stocké le projet sur un dépôt GitLab.

Pour faciliter la création d'installeurs pour n'importe quel projet Python au sein d'IBA, nous voulons utiliser GitLab-CI (intégration continue). Cette fonctionnalité de GitLab permet de déclencher automatiquement une série d'opérations en réponse à certains événements, comme un commit. Cette fonctionnalité est souvent utilisée pour automatiser les tests et le déploiement de nouvelles versions.

GitLab-CI permet d'exécuter des scripts dans un environnement contrôlé (par exemple via des images Docker Windows ou Linux). L'idée est de connecter les autres projets GitLab à celui-ci afin qu'ils puissent utiliser un script pour générer leur propre installeur.

Cette partie du projet est, selon moi, plus intéressante, car elle est beaucoup plus générale. L'automatisation des tâches lors de la mise à jour du code n'est pas spécifique à mon projet ou à Python, et c'est une compétence cruciale en entreprise, que je n'avais pas encore abordée dans mes études.

Cette semaine, je vais m'efforcer de finaliser la partie déploiement de mon application afin que d'autres personnes puissent la tester. Si j'ai le temps, j'ajouterai également certaines fonctionnalités manquantes.