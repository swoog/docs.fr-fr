---
title: Conteneurs comme fondement de la collaboration DevOps
description: Comprendre le rôle de clé de conteneurs pour simplifier les opérations de développement.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 4b40837bf2b74d801b9794c88e79eb03bcd72e95
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57679097"
---
# <a name="containers-as-the-foundation-for-devops-collaboration"></a>Conteneurs comme fondement de la collaboration DevOps

La nature des conteneurs et de la technologie Docker, les développeurs peuvent partager leurs logiciels et dépendances facilement avec les environnements de production et les opérations informatiques tout en éliminant l’excuse classique « ça marche sur ma machine ». Conteneurs de résolvent les conflits d’application entre les différents environnements. Indirectement, conteneurs et Docker rassemblent les développeurs et plus proche des opérations informatiques, facilitant ainsi pour qu’ils puissent collaborer efficacement. Adopter le flux de travail de conteneur fournit de nombreux clients avec la continuité des activités de DevOps ils ont recherché mais précédemment devaient implémenter via une configuration plus complexe pour la mise en production et de générer des pipelines. Conteneurs simplifient les pipelines de build/test/déploiement dans DevOps.

![Docker vous aide à la création de ponts entre les architectes et développeurs sur la charge de travail de développement/de conception et les opérations informatiques dans la charge de travail d’exécution/analyse/gérer](./media/image1.png)

**Figure 2-1.** Charges de travail principales par « personnes » dans le cycle de vie des applications Docker en conteneur

Avec les conteneurs Docker, les développeurs propres Nouveautés dans le conteneur (application et service et les dépendances envers les infrastructures et de composants) et comment les conteneurs et les services se comportent comme une application composée par une collection de services. Les interdépendances des plusieurs conteneurs sont définis dans un `docker-compose.yml` fichier ou ce qui peut être appelé une *manifeste de déploiement*. Pendant ce temps, les équipes informatiques (professionnels de l’informatique et administration) peuvent vous concentrer sur la gestion des environnements de production ; infrastructure ; évolutivité ; surveillance ; et, finalement, en garantissant que les applications offrent correctement pour les utilisateurs finaux, sans avoir à connaître le contenu des conteneurs différents. Par conséquent, le nom « conteneur, « rappelant l’analogie avec les conteneurs de transport du monde réel. Par conséquent, les propriétaires de contenu d’un conteneur ne pas concerner eux-mêmes avec la façon dont le conteneur feront et les transports de société expédition un conteneur à partir de son point d’origine vers sa destination sans connaître en rende compte ou sur le contenu. Dans la même façon, les développeurs peuvent créer et possédez le contenu d’un conteneur Docker sans devoir se préoccuper des mécanismes de « transport ».

Dans le pilier sur le côté gauche de la Figure 2-1, les développeurs écrivant et exécuter localement le code dans des conteneurs Docker à l’aide de Docker pour Windows ou Mac. Elles définissent l’environnement d’exploitation pour le code à l’aide d’un fichier Dockerfile qui spécifie le système d’exploitation de base pour exécuter, ainsi que les étapes de génération pour la création de leur code dans une image Docker. Les développeurs définissent la façon dont une ou plusieurs images peut interagir à l’aide de la `docker-compose.yml` manifeste de déploiement de fichier. Comme elles terminent leur développement local, push leur code d’application ainsi que les fichiers de configuration de Docker dans le référentiel de code de leur choix (autrement dit, le référentiel Git).

Le pilier DevOps définit les pipelines d’intégration (CI) de build – continu à l’aide du fichier Dockerfile fourni dans le référentiel de code. Le système CI extrait les images de conteneur de base à partir du Registre Docker sélectionné et génère les images Docker personnalisées pour l’application. Les images sont ensuite validées et transmises au Registre Docker utilisé pour les déploiements sur plusieurs environnements.

Dans le pilier sur la droite, gérer les équipes des opérations déploiement des applications et l’infrastructure en production pendant la surveillance de l’environnement et les applications afin qu’ils peuvent fournir des commentaires et informations pour l’équipe de développement sur la façon dont l’application peut être amélioré. Applications de conteneur sont généralement exécutées en production à l’aide d’orchestrateurs de conteneurs.

Les deux équipes collaborent via une plate-forme fondamentale (conteneurs Docker) qui fournit une séparation des préoccupations en tant que contrat, tout en améliorant considérablement la collaboration si les deux équipes dans le cycle de vie d’application. Les développeurs détiennent le contenu du conteneur, son environnement d’exploitation et les interdépendances de conteneur, tandis que les équipes d’exploitation prennent les images intégrées, ainsi que le manifeste et les exécute dans leur système d’orchestration.

## <a name="challenges-in-application-life-cycle-when-using-docker"></a>Cycle de défis dans la vie de l’application lors de l’utilisation de Docker.

Il existe plusieurs raisons qui vise à augmenter le nombre d’applications en conteneur dans les années à venir, et une des raisons suivantes est la création d’applications basées sur des microservices.

Au cours des 15 dernières années, l’utilisation des services web a été la base des milliers d’applications, et probablement, après quelques années, vous trouverez la même situation avec les applications basées sur des microservices en cours d’exécution sur des conteneurs Docker.

Il est également important de mentionner que vous pouvez également utiliser des conteneurs Docker pour les applications monolithiques et vous obtenez encore la plupart des avantages de Docker. Conteneurs ne ciblez pas uniquement des microservices.

L’utilisation de Docker microservices et conteneurs sont les causes de nouveaux défis dans le processus de développement de votre organisation et par conséquent, vous avez besoin d’une stratégie solide pour gérer de nombreux conteneurs et microservices en cours d’exécution sur les systèmes de production. Finalement, applications d’entreprise aura des centaines voire des milliers de conteneurs/instances en cours d’exécution en production.

Ces défis créer de nouvelles demandes lors de l’utilisation des outils de développement, vous devez donc définir de nouveaux processus dans vos activités de DevOps et trouver les réponses pour ce type de questions :

- Quels outils puis-je utiliser pour le développement, pour les opérations, gestion et CI/CD ?

- Comment mon entreprise peut gérer les erreurs dans des conteneurs lors de l’exécution en production ?

- Comment pouvons-nous changer de nos logiciels en production avec des temps d’arrêt minimum ?

- Comment pouvons-nous nous mettre à l’échelle et comment nous pouvons la surveiller notre système de production ?

- Comment pouvons-nous nous incluent le test et déploiement de conteneurs dans notre pipeline de mise en production ?

- Comment pouvons-nous utiliser outils/plateformes Open Source pour les conteneurs dans Microsoft Azure ?

Si vous pouvez répondre à toutes ces questions, vous serez mieux préparé à migrer vos applications (applications existantes ou nouvelle) dans des conteneurs Docker. 

## <a name="introduction-to-a-generic-end-to-end-docker-application-life-cycle-workflow"></a>Introduction à un workflow de cycle de vie d’application de Docker end-to-end générique

Figure 2-2 présente un flux de travail plus détaillée pour un cycle de vie application Docker, se concentrant dans cette instance sur les ressources et des activités spécifiques DevOps.

![Ce diagramme illustre la boucle « externe » de DevOps. Lorsque le code est envoyé dans le référentiel, un pipeline CI est démarré, puis commence le pipeline de livraison, où l’application est déployée. Les métriques collectées à partir des applications déployées sont renvoyées dans la charge de travail de développement, où la « boucle intérieure » se produit, afin d’équipes de développement ont des données réelles pour répondre aux besoins des utilisateurs et des entreprises.](./media/image2.png)

**Figure 2-2.** Flux de travail général pour le cycle de vie d’application en conteneur Docker

Tout commence par le développeur, qui démarre l’écriture de code dans le workflow de la boucle interne. L’étape de la boucle interne est où les développeurs définissent tout ce qui se produit avant l’envoi de code dans le référentiel de code (par exemple, un système de contrôle source tels que Git). Après qu’il a validé, les déclencheurs de référentiel intégration continue (CI) et le reste du flux de travail.

La boucle interne se compose essentiellement de la procédure standard comme « code », « exécuter », « test » et « debug », ainsi que les étapes supplémentaires nécessaires juste avant l’exécution de l’application localement. Il s’agit de processus du développeur pour exécuter et tester l’application comme un conteneur Docker. Le workflow de la boucle interne est expliqué dans les sections qui suivent.

Reprise en une étape d’examiner le flux de travail à fin fin, le flux de travail DevOps est plus d’une technologie ou d’un jeu d’outils : il s’agit d’un état d’esprit qui nécessite une évolution culturelle. Il s’agit de personnes, processus et les outils appropriés pour rendre votre cycle de vie d’application plus rapide et plus prévisible. Les entreprises qui adoptent un flux de travail en conteneur généralement restructurer leurs organisations pour représenter les personnes et les processus qui correspondent à des flux de travail en conteneur.

Pratiquant DevOps peut aider les équipes à répondre plus rapidement conjointement aux pressions concurrentielles en remplaçant les processus manuels susceptibles d’engendrer des erreurs avec automation, ce qui entraîne une traçabilité améliorée et des flux de travail reproductible. Les organisations peuvent également gérer plus efficacement les environnements et réaliser des économies de coût avec une combinaison de locaux et des ressources de cloud, ainsi que des outils étroitement intégrés.

Lorsque vous implémentez votre flux de travail DevOps pour les applications Docker, vous verrez que les technologies de Docker sont présents dans presque toutes les étapes du flux de travail, à partir de votre boîte de développement tout en travaillant dans la boucle interne (code, exécuter, déboguer), la phase de génération-test-CI et, Enfin, le déploiement de ces conteneurs pour les environnements intermédiaire et de production.

Amélioration des pratiques de qualité permettant d’identifier des défauts au début du cycle de développement, ce qui réduit le coût de leur résolution. En incluant l’environnement et les dépendances dans l’image et en adoptant une philosophie du déploiement de la même image sur plusieurs environnements, vous promouvoir une discipline d’extraire les configurations spécifiques à l’environnement effectue des déploiements plus fiable.

Données enrichies obtenues via l’instrumentation efficace (surveillance et diagnostics) permet de connaître les problèmes de performances et le comportement de l’utilisateur pour guider les investissements et les priorités futures.

DevOps doit être considéré un parcours, pas une destination. Il doit être implémentée de façon incrémentielle par le biais des projets correctement délimitées à partir de laquelle vous pouvez démontrer la réussite, en savoir plus et évoluer.

## <a name="benefits-of-devops-for-containerized-applications"></a>Avantages de DevOps pour les applications en conteneur

Voici quelques-uns des principaux avantages fournis par un flux de travail DevOps solid :

- Fournir des logiciels de meilleure qualité, plus rapidement et avec une meilleure conformité.

- Lecteur des réglages et l’amélioration continue plus tôt et plus économique.

- Augmenter la transparence et la collaboration entre les parties prenantes impliquées dans la fourniture et l’exploitation des logiciels.

- Contrôler les coûts et utiliser plus efficacement les ressources configurées tout en réduisant les risques de sécurité.

- Plug and play bien avec la plupart de vos investissements DevOps existants, y compris les investissements dans open source.

>[!div class="step-by-step"]
>[Précédent](index.md)
>[Suivant](../Microsoft-platform-tools-containerized-apps/index.md)
