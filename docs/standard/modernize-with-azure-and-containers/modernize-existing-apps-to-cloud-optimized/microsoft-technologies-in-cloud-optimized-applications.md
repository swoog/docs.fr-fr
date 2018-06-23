---
title: Technologies Microsoft dans les applications d’optimisée pour le Cloud
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Technologies Microsoft dans les applications d’optimisée pour le Cloud
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/28/2018
ms.openlocfilehash: 3c5886dc3583a5d4a6cc9566556edbe1822ad6d1
ms.sourcegitcommit: c217b067985905cb21eafc5dd9a83568d7ff4e45
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2018
ms.locfileid: "36315178"
---
# <a name="microsoft-technologies-in-cloud-optimized-applications"></a>Technologies Microsoft dans les applications d’optimisée pour le cloud

La liste suivante décrit les outils, les technologies et les solutions qui sont reconnues comme des spécifications pour les applications d’optimisée pour le Cloud. Vous pouvez adopter optimisée pour le Cloud les éléments progressivement, ou de manière sélective en fonction de vos priorités.

-   **Infrastructure de nuage**: l’infrastructure qui fournit la plateforme de calcul, le système d’exploitation, le réseau et le stockage. Microsoft Azure est positionné à ce niveau.

-   **Runtime**: cette couche fournit l’environnement pour exécuter l’application. Si vous utilisez des conteneurs, cette couche est généralement basée sur [moteur Docker](https://docs.docker.com/engine/), en cours d’exécution sur les hôtes Linux ou sur les hôtes Windows. ([Les conteneurs Windows](https://docs.microsoft.com/virtualization/windowscontainers/about/) sont pris en charge à partir de Windows Server 2016. Les conteneurs Windows est le meilleur choix pour les applications .NET Framework existantes qui s’exécutent sur Windows.)

-   **Gérés cloud**: lorsque vous choisissez une option de cloud géré, vous pouvez éviter les coûts et la complexité de la gestion et les correctifs de système d’exploitation sous-jacent infrastructure, les machines virtuelles, de prise en charge et mise en réseau de configuration. Si vous choisissez de migrer à l’aide de IaaS, vous êtes responsable de toutes ces tâches, ainsi que pour les coûts associés. Une option cloud géré, vous permet de gérer uniquement les applications et les services que vous développez. Le fournisseur de services cloud gère habituellement tout le reste. Examples of managed cloud services in Azure include [Azure SQL Database](https://azure.microsoft.com/services/sql-database), [Azure Redis Cache](https://azure.microsoft.com/services/cache/), [Azure Cosmos DB](https://azure.microsoft.com/services/cosmos-db/), [Azure Storage](https://azure.microsoft.com/services/storage/), [Azure Database for MySQL](https://azure.microsoft.com/services/mysql/), [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/), [Azure Active Directory](https://azure.microsoft.com/services/active-directory/), and managed compute services like [VM scale sets](https://azure.microsoft.com/services/virtual-machine-scale-sets/), [Azure Service Fabric](https://azure.microsoft.com/services/service-fabric/), [Azure App Service](https://azure.microsoft.com/services/app-service/), and [Azure Kubernetes Service](https://azure.microsoft.com/services/container-service/).

-   **Développement d’applications**: vous pouvez choisir de nombreux langages lorsque vous générez des applications qui s’exécutent dans des conteneurs. Ce guide se concentre sur [.NET](https://www.microsoft.com/net), mais, vous pouvez développer des applications basées sur le conteneur à l’aide d’autres langages, comme Java/Node.js, Python, Spring, ou accédez.

-   **Télémétrie, journalisation et d’audit, d’analyse**: la possibilité pour les applications d’analyse et d’audit et les conteneurs qui sont en cours d’exécution dans le cloud est essentielle pour n’importe quelle application optimisée pour le Cloud. [Azure Application Insights](https://azure.microsoft.com/services/application-insights/) et [Microsoft Operations Management Suite](https://www.microsoft.com/cloud-platform/operations-management-suite) sont les principaux outils de Microsoft qui fournissent la surveillance et l’audit pour les applications d’optimisée pour le Cloud.

-   **Approvisionnement**: outils d’automatisation vous aider à configurer l’infrastructure et de déployer une application dans plusieurs environnements (production, test, intermédiaire). Vous pouvez utiliser des outils comme Chef et Puppet pour gérer la configuration d’une application et l’environnement. Cette couche permettre également être implémentée à l’aide des approches plus simples et plus directes. Par exemple, vous pouvez déployer directement à l’aide d’Azure interface de ligne de commande (CLI d’Azure) pour les outils et ensuite utiliser le déploiement continu et libérer des pipelines de gestion dans [Visual Studio Team Services](https://visualstudio.microsoft.com/team-services/).

-   **Cycle de vie application**: [Visual Studio Team Services](https://visualstudio.microsoft.com/team-services/) et d’autres outils, tels que de Jenkins, sont des serveurs automation intégrés qui vous aident à implémenter pipelines CI/CD, y compris la gestion de version.

Les sections suivantes de ce chapitre et les procédures associées, traitent spécifiquement de plus d’informations sur la couche d’exécution (les conteneurs Windows). Le guide décrit les méthodes que vous pouvez déployer des machines virtuelles de conteneurs Windows sur Windows Server 2016 (et versions ultérieures) et les Instances de conteneur Azure. Elle traite également plus avancées plateformes PaaS comme Azure App Service et orchestrator comme Azure Service Fabric et du Service de Kubernetes Azure.

## <a name="monolithic-applications-can-be-cloud-optimized"></a>Applications monolithiques *pouvez* être optimisée pour le Cloud

Il est important de souligner que les applications (applications qui ne sont pas basées sur microservices) monolithique *pouvez* être optimisée pour le Cloud des applications. Vous pouvez générer et monolithiques applications qui tirent parti du cloud computing de modèle à l’aide d’une combinaison des conteneurs, livraison continue et DevOps de fonctionner. Si une application monolithique existante ne répond à vos objectifs, vous pouvez il moderniser et rendre optimisée pour le Cloud.

De même, si des applications monolithiques peuvent être optimisée pour le Cloud des applications, les architectures autres et plus complexes telles que des applications multicouches peuvent également modernisés en tant qu’applications d’optimisée pour le Cloud.

>[!div class="step-by-step"]
[Précédent](reasons-to-modernize-existing-net-apps-to-cloud-optimized-applications.md)
[Suivant](what-about-cloud-native-applications.md)
