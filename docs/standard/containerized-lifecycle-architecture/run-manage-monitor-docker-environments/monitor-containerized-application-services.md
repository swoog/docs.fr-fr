---
title: Superviser des services d’application conteneurisée
description: Découvrez certains aspects essentiels de la surveillance des architectures de conteneur
ms.date: 02/15/2019
ms.openlocfilehash: e14553d510751d8a75020a1b6beb9fd7bc29596e
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65641219"
---
# <a name="monitor-containerized-application-services"></a>Superviser des services d’application conteneurisée

Il est essentiel pour les applications de fractionner en plusieurs conteneurs et microservices de disposer d’un moyen pour surveiller et analyser le comportement de l’application entière.

## <a name="azure-monitor"></a>Azure Monitor

[Azure Monitor](https://azure.microsoft.com/services/monitor/) est un service analytique extensible qui surveille votre application en direct. Il vous aide à détecter et diagnostiquer les problèmes de performances et de comprendre ce que les utilisateurs font avec votre application. Il est conçu pour les développeurs, avec l’intention de vous aider à améliorer continuellement les performances et facilité d’utilisation de vos applications ou services. Azure Monitor fonctionne avec les services/web et autonome des applications sur un large éventail de plateformes telles que .NET, Java, Node.js et nombreuses autres plateformes, hébergées en local ou dans le cloud.

### <a name="additional-resources"></a>Ressources supplémentaires

- **Vue d’ensemble d’Azure Monitor** \
  <https://docs.microsoft.com/azure/azure-monitor/overview>

- **Présentation d’Application Insights** \
  <https://docs.microsoft.com/azure/azure-monitor/app/app-insights-overview>

- **Nouveautés des métriques Azure Monitor ?** \
  <https://docs.microsoft.com/azure/azure-monitor/platform/data-platform-metrics>

- **Solution Container Monitoring dans Azure Monitor** \
  <https://docs.microsoft.com/azure/azure-monitor/insights/containers>

## <a name="security-and-backup-services"></a>Services de sécurité et de sauvegarde

Il existe de nombreuses tâches de prise en charge avec un grand nombre de détails que vous devez gérer pour garantir à que vos applications et votre infrastructure sont en état de haut de gamme pour prendre en charge les besoins de l’entreprise, et la situation devient plus complexe dans le domaine des microservices, donc un moyen ont des vues générales et détaillées lorsque vous avez besoin prendre des mesures.

Azure propose les outils nécessaires pour gérer et fournir une vue unifiée des quatre aspects critiques des ressources de votre cloud et en local :

- **Sécurité**. Avec [Azure Security Center](https://azure.microsoft.com/services/security-center/).
  - Obtenir une visibilité complète et un contrôle accrus de la sécurité de vos machines virtuelles, les applications et les charges de travail.
  - Centraliser la gestion de vos stratégies de sécurité et d’intégrer des outils et processus existants.
  - Détecter les menaces réelles avec analytique avancée.

- **Sauvegarde**. Avec [sauvegarde Azure](https://azure.microsoft.com/services/backup/).
  - Éviter les interruptions de l’entreprise, répondre aux objectifs de conformité et protégez vos données contre les ransomware et les erreurs humaines.
  - Gardez vos données de sauvegarde chiffrées en transit et au repos.
  - Garantir l’accès en fonction de l’authentification multifacteur pour empêcher toute utilisation non autorisée.

- **Ressources locales**. Avec [un cloud hybride réellement cohérent](https://azure.microsoft.com/resources/truly-consistent-hybrid-cloud-with-microsoft-azure/).

>[!div class="step-by-step"]
>[Précédent](manage-production-docker-environments.md)
>[Suivant](../key-takeaways/index.md)
