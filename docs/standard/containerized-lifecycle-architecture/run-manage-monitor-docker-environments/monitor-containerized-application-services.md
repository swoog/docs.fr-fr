---
title: Surveiller les services d’application en conteneur
description: Découvrez certains aspects essentiels de la surveillance des architectures de conteneur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 925db543617deb28590cf6631ebbda3ee96836c4
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56975743"
---
# <a name="monitor-containerized-application-services"></a>Surveiller les services d’application en conteneur

Il est essentiel pour les applications de fractionner en plusieurs conteneurs et microservices de disposer d’un moyen pour surveiller et analyser le comportement de l’application entière.

## <a name="microsoft-application-insights"></a>Microsoft Application Insights

[Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-overview) est un service analytique extensible qui surveille votre application en direct. Il vous aide à détecter et diagnostiquer les problèmes de performances et de comprendre ce que les utilisateurs font avec votre application. Il est conçu pour les développeurs, avec l’intention de vous aider à améliorer continuellement les performances et facilité d’utilisation de vos applications ou services. Application Insights fonctionne avec/services web et autonome des applications sur un large éventail de plateformes telles que .NET, Java, Node.js et nombreuses autres plateformes, hébergées en local ou dans le cloud.

### <a name="analyzing-docker-apps-in-qa-environments-using-application-insights"></a>Analyse des applications Docker dans les environnements d’assurance qualité à l’aide d’Application Insights

En ce qui concerne à Docker, vous pouvez représenter des événements de cycle de vie et des compteurs de performances à partir de conteneurs Docker sur Application Insights. Vous devez simplement exécuter la [image Application Insights Docker](https://hub.docker.com/r/microsoft/applicationinsights/) comme un conteneur dans votre hôte et il affiche les compteurs de performance pour l’hôte ainsi que pour les autres images de Docker. Cette image Application Insights Docker (Figure 6 - 1) vous aide à surveiller vos applications en conteneur en collectant les données de télémétrie concernant les performances et l’activité de votre hôte Docker (autrement dit, vos machines virtuelles Linux), des conteneurs Docker et des applications en cours d’exécution au sein de celles-ci.

![exemple](./media/image1.png)

**Figure 6-1** : Application Insights, surveillance des conteneurs et des hôtes Docker

Lorsque vous exécutez le [image Application Insights Docker](https://hub.docker.com/r/microsoft/applicationinsights/) sur votre hôte Docker, vous pouvez :

- Données de télémétrie concernant tous les conteneurs en cours d’exécution sur l’ordinateur hôte de cycle de vie, Démarrer, arrêter et ainsi de suite.

- Compteurs de performances pour tous les conteneurs : Processeur, mémoire, l’utilisation du réseau et bien plus encore.

- Si vous avez également installé [SDK Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net) dans les applications en cours d’exécution dans les conteneurs, toutes les données de télémétrie de ces applications auront des propriétés supplémentaires identifiant l’ordinateur et le conteneur hôte. Par conséquent, par exemple, si vous avez des instances d’une application en cours d’exécution dans plusieurs hôtes, vous facilement serez en mesure de filtrer la télémétrie d’application par hôte.

### <a name="setting-up-application-insights-to-monitor-docker-applications-and-docker-hosts"></a>Configuration d’Application Insights pour surveiller les applications Docker et des hôtes Docker

Pour créer une ressource Application Insights, suivez les instructions fournies dans les articles présentés dans la liste qui suit. Portail Azure crée le script nécessaire pour vous.

- **Surveiller des applications Docker dans Application Insights :** \
  <https://docs.microsoft.com/azure/application-insights/app-insights-docker>

- **Image d’application Insights Docker à Docker Hub et GitHub :** \
  <https://hub.docker.com/r/microsoft/applicationinsights/> et \
  <https://github.com/Microsoft/ApplicationInsights-Docker>

- **Configurer Application Insights pour les applications web ASP.NET et ASP.NET Core :** \
  <https://docs.microsoft.com/azure/application-insights/app-insights-asp-net>

- **Application Insights pour les pages web :**  
  <https://docs.microsoft.com/azure/application-insights/app-insights-javascript>

## <a name="security-backup-and-monitoring-services"></a>Sécurité, de sauvegarde et de surveillance des services

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

- **Surveillance**. Avec [surveillance Azure](https://azure.microsoft.com/solutions/monitoring/), [Analytique de journal](https://azure.microsoft.com/services/log-analytics/), et [Application Insights](https://azure.microsoft.com/services/application-insights/).
  - Bénéficiez d’une visibilité complète sur l’intégrité et les performances de vos charges de travail Azure, les applications et infrastructure.
  - Collecter des données à partir de n’importe quelle source et obtenez des insights enrichis dans vos machines virtuelles, les conteneurs et les applications.
  - Trouvez les informations que vous avez besoin à l’aide des requêtes interactives et recherche en texte intégral. 
  - Effectuer une analyse de cause racine avec analytique avancée, y compris les algorithmes d’apprentissage automatique.

- **Ressources locales**. Avec [un cloud hybride réellement cohérent](https://azure.microsoft.com/resources/truly-consistent-hybrid-cloud-with-microsoft-azure/).

>[!div class="step-by-step"]
>[Précédent](manage-production-docker-environments.md)
>[Suivant](../key-takeaways/index.md)
