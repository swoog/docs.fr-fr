---
title: Surveiller les services d’application en conteneur
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 4bdc4470624ce6e905ab858a2bd8b607c8d3d646
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44275858"
---
# <a name="monitor-containerized-application-services"></a>Surveiller les services d’application en conteneur

Il est essentiel pour les applications de fractionner en plusieurs conteneurs et microservices de disposer d’un moyen pour surveiller et analyser le comportement de l’application.

## <a name="microsoft-application-insights"></a>Microsoft Application Insights

[Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-overview) est un service analytique extensible qui surveille votre application en direct. Il vous aide à détecter et diagnostiquer les problèmes de performances et de comprendre ce que les utilisateurs font avec votre application. Il est conçu pour les développeurs, avec l’intention de vous aider à améliorer continuellement les performances et facilité d’utilisation de vos applications ou services. Application Insights fonctionne avec/services web et autonome des applications sur un large éventail de plateformes telles que .NET, Java, Node.js et nombreuses autres plateformes, hébergées en local ou dans le cloud.

### <a name="analyzing-docker-apps-in-qa-environments-using-application-insights"></a>Analyse des applications Docker dans les environnements d’assurance qualité à l’aide d’Application Insights

En ce qui concerne à Docker, vous pouvez représenter des événements de cycle de vie et des compteurs de performances à partir de conteneurs Docker sur Application Insights. Vous devez simplement exécuter la [image Application Insights Docker](https://hub.docker.com/r/microsoft/applicationinsights/) comme un conteneur dans votre hôte et il affiche les compteurs de performance pour l’hôte ainsi que pour les autres images de Docker. Cette image Application Insights Docker (Figure 6 - 1) vous aide à surveiller vos applications en conteneur en collectant les données de télémétrie concernant les performances et l’activité de votre hôte Docker (autrement dit, vos machines virtuelles Linux), des conteneurs Docker et des applications en cours d’exécution au sein de celles-ci.

![exemple](./media/image1.png)

Figure 6-1 : Application Insights, surveillance des conteneurs et des hôtes Docker

Lorsque vous exécutez le [image Application Insights Docker](https://hub.docker.com/r/microsoft/applicationinsights/) sur votre hôte Docker, vous pouvez :

-   Données de télémétrie concernant tous les conteneurs en cours d’exécution sur l’ordinateur hôte de cycle de vie, Démarrer, arrêter et ainsi de suite.

-   Compteurs de performances pour tous les conteneurs : processeur, mémoire, l’utilisation du réseau et bien plus encore.

-   Si vous avez également installé [SDK Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net) dans les applications en cours d’exécution dans les conteneurs, toutes les données de télémétrie de ces applications auront des propriétés supplémentaires identifiant l’ordinateur et le conteneur hôte. Par conséquent, par exemple, si vous avez des instances d’une application en cours d’exécution dans plusieurs hôtes, vous facilement serez en mesure de filtrer la télémétrie d’application par hôte.

### <a name="setting-up-application-insights-to-monitor-docker-applications-and-docker-hosts"></a>Configuration d’Application Insights pour surveiller les applications Docker et des hôtes Docker

Pour créer une ressource Application Insights, suivez les instructions fournies dans les articles présentés dans la liste qui suit. Portail Azure crée le script nécessaire pour vous.

-   **Surveiller des applications Docker dans Application Insights :**  [https://docs.microsoft.com/azure/application-insights/app-insights-docker](https://docs.microsoft.com/azure/application-insights/app-insights-docker)

-   **Image d’application Insights Docker à Docker Hub et Github :**  
[https://hub.docker.com/r/microsoft/applicationinsights/](https://hub.docker.com/r/microsoft/applicationinsights/) Et <https://github.com/Microsoft/ApplicationInsights-Docker>

-   **Configurer Application Insights pour ASP.NET :**  
[https://docs.microsoft.com/azure/application-insights/app-insights-asp-net](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net)

-   **Application Insights pour les pages web :**  
<https://docs.microsoft.com/azure/application-insights/app-insights-javascript>

## <a name="microsoft-operations-management-suite"></a>Microsoft Operations Management Suite

[Operations Management Suite](https://microsoft.com/oms) est une solution de gestion informatique simplifiée qui fournit l’analytique de journal, automation, sauvegarde et la récupération de site. Selon [requêtes](https://blogs.technet.microsoft.com/msoms/2016/01/21/easy-microsoft-operations-management-suite-search-queries/) dans Operations Management Suite, vous pouvez augmenter [alertes](https://docs.microsoft.com/azure/operations-management-suite/operations-management-suite-monitoring-alerts) et mise à jour par le biais de la valeur [Azure Automation](https://docs.microsoft.com/azure/automation/). Il s’intègre également de façon transparente avec vos solutions existantes de gestion pour fournir une vue de volet de verre unique. Operations Management Suite vous aide à gérer et protéger votre réseau local et infrastructure cloud.

### <a name="operations-management-suitehttpsmicrosoftcomoms-container-solution-for-docker"></a>[Operations Management Suite](https://microsoft.com/oms) Solution de conteneur pour Docker

En plus de fournir des services précieux sur son propre, la Solution de conteneur Operations Management Suite pouvez gérer et surveiller des hôtes et conteneurs Docker en affichant les informations sur l’emplacement vos conteneurs et les hôtes de conteneur, qui exécutent des conteneurs ou ayant échoué et les journaux des démons et conteneurs Docker envoyés à *stdout* et *stderr*. Elle montre également les métriques de performances, notamment celles liées au processeur, à la mémoire, au réseau et au stockage pour le conteneur et les hôtes pour vous aider à résoudre et à trouver les conteneurs voisins bruyants.

![](./media/image2.png)

Figure 6-2 : les informations sur les conteneurs Docker indiqué par Operations Management Suite

Application Insights et Operations Management Suite se concentrent sur la surveillance des activités ; Toutefois, Application Insights se concentre plus précisément sur les applications elles-mêmes grâce à son kit de développement logiciel en cours d’exécution au sein de l’application de surveillance. Toutefois, Operations Management Suite se concentre beaucoup plus sur l’infrastructure sur les ordinateurs hôtes, il offre en outre une analyse approfondie sur les journaux à l’échelle tout en fournissant un système très flexible orientés données/requête de recherche.

Operations Management Suite étant implémenté en tant que cloud-service, il peut être opérationnel rapidement avec un investissement minimal en services d’infrastructure. Nouvelles fonctionnalités sont fournies automatiquement, qui vous évite de maintenance continue et les coûts de mise à niveau.

À l’aide de la Solution de conteneur Operations Management Suite, vous pouvez procédez comme suit :

-   Centraliser et de mettre en corrélation des millions de journaux des conteneurs Docker à l’échelle

-   Afficher des informations sur tous les hôtes de conteneur dans un emplacement unique

-   Savoir quels conteneurs sont en cours d’exécution, image qu’ils s’exécutent et où ils s’exécutent

-   Diagnostiquer rapidement les conteneurs de « voisin bruyant » qui peuvent entraîner des problèmes sur les hôtes de conteneur

-   Consultez une piste d’audit pour les actions sur les conteneurs

-   Résoudre les problèmes à afficher et rechercher des journaux centralisés sans communication à distance pour les hôtes Docker

-   Rechercher des conteneurs qui peuvent être « voisins bruyants » et consomme des ressources excessives sur un ordinateur hôte

-   Afficher centralisées sur le processeur, mémoire, stockage et informations de performances et l’utilisation du réseau de conteneurs

-   Générer des conteneurs Docker avec Azure Automation de test

Vous pouvez voir des informations sur les performances en exécutant des requêtes comme Type = Perf, comme illustré dans la Figure 6-3.

![DockerPerfMetricsView](./media/image3.png){width="5.78625in" height="3.25in"}

Figure 6-3 : les mesures de performances des hôtes Docker indiqués par Operations Management Suite

L’enregistrement des requêtes est également une fonctionnalité standard dans Operations Management Suite et peut vous aider à conserver les requêtes que vous avez trouvées utiles et découvrez des tendances dans votre système.

**Plus d’informations** pour rechercher des informations sur l’installation et configuration de la Docker solution conteneur dans [Operations Management Suite](https://microsoft.com/oms), accédez à <https://docs.microsoft.com/azure/log-analytics/log-analytics-containers>.

>[!div class="step-by-step"]
[Précédent](manage-production-docker-environments.md)
[Suivant](../key-takeaways/index.md)
