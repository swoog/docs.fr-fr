---
title: Workflow DevOps pour les applications Docker avec les outils Microsoft
description: En conteneur Docker Application Lifecycle with Microsoft Platform and Tools DevOps des flux de travail avec les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 80acd58d08900da8e79f6b7388da3b10f9e4e566
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59672301"
---
# <a name="docker-application-devops-workflow-with-microsoft-tools"></a>Workflow DevOps pour les applications Docker avec les outils Microsoft

*Microsoft Visual Studio, Azure DevOps Services, Team Foundation Server et Azure Monitor fournissent qu'un écosystème complet pour le développement et les opérations informatiques qui permettent à votre équipe les outils nécessaires pour gérer des projets et de rapidement générer, tester et déployer en conteneur applications.*

Avec Visual Studio et Azure DevOps Services dans le cloud, ainsi que de Team Foundation Server en local, les équipes de développement peuvent productive créer, tester et publier des applications en conteneur ciblant Windows ou Linux.

Outils Microsoft peuvent automatiser le pipeline pour les implémentations spécifiques d’applications en conteneur, Docker, .NET Core ou n’importe quelle combinaison avec d’autres plateformes, à partir de builds globales et intégration continue (CI) et les tests avec Azure DevOps Services ou de l’équipe Foundation Server, au déploiement continu (CD) aux environnements Docker (développement, intermédiaire, Production) et pour transmettre des informations d’analytique sur les services à l’équipe de développement via Azure Monitor. Chaque validation de code peut lancer une build (CI) et déployer automatiquement les services sur des environnements en conteneur spécifiques (CD).

Les développeurs et testeurs peuvent provisionner facilement et rapidement des environnements de développement et de test basés sur Docker similaires à des environnements de production au moyen de modèles dans Microsoft Azure.

La difficulté du développement d’applications en conteneur augmente de façon régulière en fonction de la complexité et des besoins en matière de scalabilité de l’entreprise. Un bon exemple de cette complexité sont des applications basées sur les architectures de microservices. Pour réussir dans un tel environnement, votre projet doit automatiser le cycle de vie — non seulement la génération et le déploiement, mais aussi la gestion des versions et la collecte de données de télémétrie. Azure DevOps Services et Azure offrent les fonctionnalités suivantes :

- Azure DevOps Services et Team Foundation Server source code gestion (basée sur Git ou Team Foundation Version Control), planification Agile (Agile, Scrum et CMMI sont pris en charge), élément de configuration, la gestion de version et d’autres outils pour les équipes Agile.

- Azure DevOps Services et Team Foundation Server incluent un écosystème puissant et croissant de premier - et des extensions tierces avec lequel vous facilement pourrez construire un élément de configuration, la création, test, remise et libérer le pipeline de gestion pour les microservices.

- Exécuter des tests automatisés dans le cadre de votre pipeline de build dans les Services Azure DevOps.

- Azure DevOps Services peut renforcer le cycle de vie DevOps avec les remises sur plusieurs environnements, pas seulement pour les environnements de production, mais également pour le test, y compris un / expérimentation B, [versions « Canary »](https://martinfowler.com/bliki/CanaryRelease.html), et ainsi de suite.

- Les organisations peuvent facilement provisionner des conteneurs Docker à partir d’images privées stockées dans Azure Container Registry, ainsi que toute dépendance sur les composants Azure (données, PaaS, etc.) à l’aide de modèles Azure Resource Manager avec les outils qu’ils sont déjà familiers.

>[!div class="step-by-step"]
>[Précédent](../design-develop-containerized-apps/build-aspnet-core-applications-linux-containers-aks-kubernetes.md)
>[Suivant](docker-application-outer-loop-devops-workflow.md)
