---
title: Présentation de Docker
description: Architecture des microservices .NET pour les applications .NET en conteneur | Présentation de Docker
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: 06dd5199b8dbc42ce3e9ae35bc5c3673d01cb4de
ms.sourcegitcommit: 979597cd8055534b63d2c6ee8322938a27d0c87b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37106799"
---
# <a name="what-is-docker"></a>Présentation de Docker

[Docker](https://www.docker.com/) est un [projet open source](https://github.com/docker/docker) permettant d’automatiser le déploiement d’applications en tant que conteneurs portables et autonomes exécutables sur le cloud ou localement. Docker est également le nom de la [société](https://www.docker.com/) qui développe et diffuse cette technologie. Docker travaille en collaboration avec certains fournisseurs de cloud, Linux et Windows, parmi lesquels Microsoft.

![](./media/image2.png)

**Figure 2-2**. Docker déploie des conteneurs dans toutes les couches du cloud hybride

Les conteneurs d’images Docker s’exécutent en mode natif sur Linux et Windows. Les images Windows et les images Linux s’exécutent uniquement sur des hôtes Windows et des hôtes Linux, respectivement. L’hôte est un serveur ou une machine virtuelle.

Le développement peut s’effectuer sur Windows, Linux ou macOS. L’ordinateur de développement exécute un hôte Docker sur lequel sont déployées les images Docker, y compris l’application et ses dépendances. Sur Linux ou macOS, vous utilisez un hôte Docker basé sur Linux qui vous permet de créer des images uniquement pour des conteneurs Linux. (Sur macOS, vous pouvez modifier le code ou exécuter l’interface CLI de Docker, mais à ce jour, les conteneurs ne s’exécutent pas directement sur macOS.) Sur Windows, vous pouvez créer des images pour des conteneurs Windows ou Linux.

Sur Windows ou macOS, [Docker Community Edition (CE)](https://www.docker.com/community-edition) héberge les conteneurs dans un environnement de développement et fournit des outils de développement supplémentaires. [Docker Enterprise Edition (EE)](https://www.docker.com/enterprise-edition) est utilisé par les équipes informatiques pour créer, livrer et exécuter des applications stratégiques volumineuses. ~Les deux produits installent la machine virtuelle nécessaire (l’hôte Docker) pour héberger les conteneurs.~ 

Les [conteneurs Windows](https://msdn.microsoft.com/en-us/virtualization/windowscontainers/about/about_overview) fonctionnent avec deux types de runtime :

-   Les conteneurs Windows Server assurent l’isolation des applications par le biais d’une technologie d’isolation des processus et des espaces de noms. Un conteneur Windows Server partage un noyau avec l’hôte conteneur et avec tous les conteneurs exécutés sur l’hôte.

-   Les conteneurs Hyper-V étendent l’isolation fournie par les conteneurs Windows Server en exécutant chaque conteneur sur une machine virtuelle hautement optimisée. Dans cette configuration, le noyau de l’hôte conteneur n’est pas partagé avec les conteneurs Hyper-V, ce qui garantit une meilleure isolation. Les conteneurs Hyper-V autorisent l’exécution d’applications non approuvées et *multilocataires hostiles* sur le même hôte. Par rapport aux conteneurs Windows Server, les conteneurs Hyper-V sont un peu moins performants du point de vue de la densité et du temps de démarrage.

Les images de ces deux types de conteneurs sont créées et fonctionnent de la même façon. Elles diffèrent dans la manière dont le conteneur est créé. Pour plus d’informations, consultez [Conteneurs Hyper-V](https://msdn.microsoft.com/en-us/virtualization/windowscontainers/about/about_overview).

## <a name="comparing-docker-containers-with-virtual-machines"></a>Comparaison entre les conteneurs Docker et les machines virtuelles

La figure 2-3 compare les machines virtuelles et les conteneurs Docker.

  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Machines virtuelles**                                                                                                                                                                  **Conteneurs Docker**
                                                                                                                                                                                        
  ![](./media/image3.png)                                                                                                                                ![](./media/image4.png)
                                                                                                                                                                                        
  Les machines virtuelles incluent l’application, les bibliothèques ou binaires requis, et un système d’exploitation invité complet. La virtualisation complète nécessite plus de ressources que la mise en conteneur. Les conteneurs incluent l’application et toutes ses dépendances. Toutefois, les conteneurs partagent le noyau du système d’exploitation avec d’autres conteneurs. Les conteneurs sont exécutés en tant que processus isolés dans l’espace utilisateur sur le système d’exploitation hôte. Ce n’est pas le cas des conteneurs Hyper-V, où chaque conteneur s’exécute sur une machine virtuelle spécifique.
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Figure 2-3**. Comparaison entre les machines virtuelles traditionnelles et les conteneurs Docker

Du fait que les conteneurs nécessitent beaucoup moins de ressources (par exemple, ils n’ont pas besoin d’un système d’exploitation complet), leur démarrage est rapide et leur déploiement est simple. La faible utilisation de ressources permet une densité plus élevée. Vous pouvez exécuter davantage de services sur la même unité matérielle et ainsi réduire vos coûts.

L’exécution sur le même noyau entraîne une moins bonne isolation comparativement aux machines virtuelles.

L’objectif principal d’une image est de garantir un environnement (dépendances) identique entre les différents déploiements. Vous pouvez ainsi la déboguer sur votre machine et la déployer sur une autre machine en étant sûr de garder le même environnement.

Une image conteneur est un moyen d’empaqueter une application ou un service et de les déployer ensuite d’une façon fiable et reproductible. Plus qu’une simple technologie, Docker peut également être vu comme une philosophie et un processus.

Les développeurs Docker ne disent pas : « Cela fonctionne sur ma machine, alors pourquoi pas en production ? » Ils disent : « Cela s’exécute sur Docker ». Les applications empaquetées dans Docker s’exécutent dans tous les environnements Docker pris en charge. Elles s’exécutent de façon cohérente sur toutes les cibles de déploiement (développement, test, préproduction, production).

>[!div class="step-by-step"]
[Précédent](index.md)
[Suivant](docker-terminology.md)
