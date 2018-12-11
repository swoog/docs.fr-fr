---
title: Conteneurs comme fondement de la collaboration DevOps
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: ccc8ef765cadfec31a2f714767d8e6eb76508093
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53126625"
---
# <a name="containers-as-the-foundation-for-devops-collaboration"></a>Conteneurs comme fondement de la collaboration DevOps

La nature des conteneurs et de la technologie Docker, les développeurs peuvent partager leurs logiciels et dépendances facilement avec les environnements de production et les opérations informatiques tout en éliminant l’excuse classique « ça marche sur ma machine ». Conteneurs de résolvent les conflits d’application entre les différents environnements. Indirectement, conteneurs et Docker rassemblent les développeurs et plus proche des opérations informatiques, facilitant ainsi pour qu’ils puissent collaborer efficacement. Adopter le flux de travail de conteneur fournit de nombreux clients avec la continuité des activités de DevOps ils ont recherché mais précédemment devaient implémenter via une configuration plus complexe pour la mise en production et de générer des pipelines. Conteneurs simplifient les pipelines de build/test/déploiement dans DevOps.

![](./media/image1.png)

Figure 2-1 : Charges de travail principales par « personnes » dans le cycle de vie des applications Docker en conteneur

Avec les conteneurs Docker, les développeurs propres Nouveautés dans le conteneur (application et service et les dépendances envers les infrastructures et de composants) et comment les conteneurs et les services se comportent comme une application composée par une collection de services. Les interdépendances des conteneurs plusieurs sont définies dans un fichier docker-compose.yml, ou ce qui peut être appelé une *manifeste de déploiement*. Pendant ce temps, les équipes informatiques (professionnels de l’informatique et administration) peuvent vous concentrer sur la gestion des environnements de production ; infrastructure ; évolutivité ; surveillance ; et, finalement, en garantissant que les applications offrent correctement pour les utilisateurs finaux, sans avoir à connaître le contenu des conteneurs différents. Par conséquent, le nom « conteneur, « rappelant l’analogie avec les conteneurs de transport du monde réel. Par conséquent, les propriétaires de contenu d’un conteneur ne pas concerner eux-mêmes avec la façon dont le conteneur feront et les transports de société expédition un conteneur à partir de son point d’origine vers sa destination sans connaître en rende compte ou sur le contenu. Dans la même façon, les développeurs peuvent créer et possédez le contenu d’un conteneur Docker sans devoir se préoccuper des mécanismes de « transport ».

Dans le pilier sur le côté gauche de la Figure 2-1, les développeurs écrivant et exécuter localement le code dans des conteneurs Docker à l’aide de Docker pour Windows ou Mac. Elles définissent l’environnement d’exploitation pour le code à l’aide d’un fichier Dockerfile qui spécifie le système d’exploitation de base pour exécuter, ainsi que les étapes de génération pour la création de leur code dans une image Docker. Les développeurs définissent la façon dont l’une ou plusieurs images peut interagir à l’aide de la *docker-compose.yml* manifeste de déploiement de fichier. Comme elles terminent leur développement local, push leur code d’application ainsi que les fichiers de configuration de Docker dans le référentiel de code de leur choix (autrement dit, le référentiel Git).

Le pilier DevOps définit les pipelines d’intégration (CI) de build – continu à l’aide du fichier Dockerfile fourni dans le référentiel de code. Le système CI extrait les images de conteneur de base à partir du Registre Docker sélectionné et génère les images Docker personnalisées pour l’application. Les images sont ensuite validées et transmises au Registre Docker utilisé pour les déploiements sur plusieurs environnements.

Dans le pilier sur la droite, gérer les équipes des opérations déploiement des applications et l’infrastructure en production pendant la surveillance de l’environnement et les applications afin qu’ils peuvent fournir des commentaires et informations pour l’équipe de développement sur la façon dont l’application peut être amélioré. Applications de conteneur sont généralement exécutées en production à l’aide d’orchestrateurs de conteneurs.

Les deux équipes collaborent via une plate-forme fondamentale (conteneurs Docker) qui fournit une séparation des préoccupations en tant que contrat, tout en améliorant considérablement la collaboration si les deux équipes dans le cycle de vie d’application. Les développeurs détiennent le contenu du conteneur, son environnement d’exploitation et les interdépendances de conteneur, tandis que les équipes d’exploitation prennent les images intégrées, ainsi que le manifeste et les exécute dans leur système d’orchestration.

## <a name="introduction-to-a-generic-end-to-end-docker-application-life-cycle-workflow"></a>Introduction à un workflow de cycle de vie d’application de Docker end-to-end générique

Figure 2-2 présente un flux de travail plus détaillée pour un cycle de vie application Docker, se concentrant dans cette instance sur les ressources et des activités spécifiques DevOps.

![](./media/image2.png)

Figure 2-2 : Flux de travail général pour le cycle de vie d’application en conteneur Docker

Tout commence par le développeur, qui démarre l’écriture de code dans le workflow de la boucle interne. L’étape de la boucle interne est où les développeurs définissent tout ce qui se produit avant l’envoi de code dans le référentiel de code (par exemple, un système de contrôle source tels que Git). Une fois validée, le référentiel déclenche une intégration continue (CI) et le reste du flux de travail.

La boucle interne se compose essentiellement de la procédure standard comme « code », « run », « test » et « debug », ainsi que des étapes supplémentaires directement avant d’exécuter l’application localement. Il s’agit quand le développeur s’exécute et teste l’application comme un conteneur Docker. Le workflow de la boucle interne est expliqué dans les sections qui suivent.

Reprise en une étape d’examiner le flux de travail à fin fin, le flux de travail DevOps est plus d’une technologie ou d’un jeu d’outils : il s’agit d’un état d’esprit qui nécessite une évolution culturelle. Il est de personnes, processus et les outils appropriés pour rendre votre cycle de vie d’application plus rapide et plus prévisible. Les entreprises qui adoptent un flux de travail en conteneur généralement restructurer leurs organisations pour représenter les personnes et les processus qui correspondent à des flux de travail en conteneur.

Pratiquant DevOps peut aider les équipes à répondre plus rapidement conjointement aux pressions concurrentielles en remplaçant les processus manuels susceptibles d’engendrer des erreurs avec automation, ce qui entraîne une traçabilité améliorée et des flux de travail reproductible. Les organisations peuvent également gérer plus efficacement les environnements et réaliser des économies de coût avec une combinaison de locaux et des ressources de cloud, ainsi que des outils étroitement intégrés.

Lorsque vous implémentez votre flux de travail DevOps pour les applications Docker, vous verrez que les technologies de Docker sont présents dans presque toutes les étapes du flux de travail, à partir de votre boîte de développement tout en travaillant dans la boucle interne (code, exécuter, déboguer), à la phase de génération-test-CI et, Bien sûr, à la production et des environnements intermédiaires et lors du déploiement de vos conteneurs à ces environnements.

Amélioration des pratiques de qualité permettant d’identifier des défauts au début du cycle de développement, ce qui réduit le coût de leur résolution. En incluant l’environnement et les dépendances dans l’image et en adoptant une philosophie du déploiement de la même image sur plusieurs environnements, vous promouvoir une discipline d’extraire les configurations spécifiques à l’environnement effectue des déploiements plus fiable.

Données enrichies obtenues via l’instrumentation efficace (surveillance et diagnostics) permet de connaître les problèmes de performances et le comportement de l’utilisateur pour guider les investissements et les priorités futures.

DevOps doit être considéré un parcours, pas une destination. Il doit être implémentée de façon incrémentielle par le biais des projets correctement délimitées à partir de laquelle vous pouvez démontrer la réussite, en savoir plus et évoluer.

## <a name="benefits-of-devops-for-containerized-applications"></a>Avantages de DevOps pour les applications en conteneur

Voici quelques-uns des principaux avantages fournis par un flux de travail DevOps solid :

-   Fournir des logiciels de meilleure qualité, plus rapidement et avec une meilleure conformité

-   Lecteur des réglages et l’amélioration continue plus tôt et plus économique

-   Augmenter la transparence et la collaboration entre les parties prenantes impliquées dans la fourniture et l’exploitation des logiciels

-   Contrôler les coûts et d’utiliser plus efficacement les ressources configurées tout en réduisant les risques de sécurité

-   Plug-and-play bien avec la plupart de vos investissements DevOps existants, y compris les investissements en l’open source

>[!div class="step-by-step"]
>[Précédent](index.md)
>[Suivant](../Microsoft-platform-tools-containerized-apps/index.md)