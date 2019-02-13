---
title: Qu’est-ce que Docker ?
description: Obtenir un peu plus loin dans votre présentation de Docker, une analogie simple ici peut-être vous aider.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: c8300c964dfce0cc8e39478cc10ed7589dbca2c9
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56218552"
---
# <a name="what-is-docker"></a>Qu’est-ce que Docker ?

[Docker](https://www.docker.com/) est un [projet open source](https://github.com/docker/docker) pour automatiser le déploiement d’applications en tant que conteneurs portables et autonomes pouvant s’exécuter dans le nuage ou sur site (voir Figure 1 - 2). Docker est également un [entreprise](https://www.docker.com/) qui promeut et développe cette technologie, travailler en collaboration avec le cloud, Linux et les fournisseurs de Windows, y compris Microsoft.

![](./media/image2.png)

Figure 1-2 : Docker déploie des conteneurs à toutes les couches du cloud hybride

Les conteneurs d’images Docker peuvent s’exécuter en mode natif sur Linux et Windows. Toutefois, les images Windows peuvent s’exécuter uniquement sur les ordinateurs hôtes Windows et Linux images peuvent s’exécuter uniquement sur les hôtes Linux, ce qui signifie qu’un serveur hôte ou une machine virtuelle.

Les développeurs peuvent utiliser des environnements de développement sur Windows, Linux ou macOS. Sur l’ordinateur de développement, le développeur exécute un hôte Docker à quels Docker images sont déployées, y compris l’application et ses dépendances. Les développeurs qui travaillent sur Linux ou sur Mac utilisent un hôte Docker qui est basé sur Linux, et ils peuvent créer des images uniquement pour les conteneurs Linux. (Les développeurs qui travaillent sur le Mac peuvent modifier le code ou exécuter l’interface de ligne de commande de Docker \[CLI\] à partir de Mac OS, mais à ce jour, les conteneurs n’exécutent pas directement sur macOS.) Les développeurs qui travaillent sur Windows peuvent créer des images pour des conteneurs Windows ou Linux.

Pour héberger des conteneurs dans un environnement de développement et fournir des outils de développement supplémentaires, Docker fournit [Docker Community Edition (CE)](https://www.docker.com/community-edition) pour Windows ou macOS. Ces produits installent la machine virtuelle nécessaire (l’hôte Docker) pour héberger les conteneurs. Docker fournit aussi [Docker Enterprise Edition (EE)](https://www.docker.com/enterprise-edition), conçu pour le développement en entreprise et utilisé par les équipes informatiques qui génèrent, livrent et exécutent des applications métier stratégiques volumineuses en production.

Les [conteneurs Windows](/virtualization/windowscontainers/about/) fonctionnent avec deux types de runtime :

-   **Conteneur Windows Server** ce runtime fournit l’isolation des applications via une technologie d’isolation des processus et l’espace de noms. Un conteneur Windows Server partage un noyau avec l’hôte de conteneur et tous les conteneurs en cours d’exécution sur l’ordinateur hôte.

-   **Conteneur Hyper-V** cela développe l’isolation fournie par les conteneurs Windows Server en exécutant chaque conteneur dans une machine virtuelle hautement optimisée. Dans cette configuration, le noyau de l’hôte de conteneur n’est pas partagé avec les conteneurs Hyper-V, qui fournit une meilleure isolation.

Les images de ces conteneurs sont créés dans la même façon et la même fonctionnent. La différence réside dans la façon dont le conteneur est créé à partir de l’image : exécution d’un conteneur Hyper-V nécessite un paramètre supplémentaire. Pour plus d’informations, consultez [conteneurs Hyper-V](/virtualization/windowscontainers/about/).

## <a name="comparing-docker-containers-with-vms"></a>Comparaison de conteneurs Docker avec des machines virtuelles

Figure 1-3 présente une comparaison entre les machines virtuelles et Docker conteneurs.

Étant donné que les conteneurs nécessitent beaucoup moins de ressources (par exemple, il est inutile un système d’exploitation complet), ils sont faciles à déployer et de leur démarrage rapide. Cela rend possible pour que vous disposiez d’une densité plus élevée, ce qui signifie que vous pouvez exécuter plus de services sur la même unité de matériel, ce qui réduit les coûts.

Comme effet secondaire de l’exécution sur le même noyau, vous obtenir moins bonne isolation que les machines virtuelles.

L’objectif principal d’une image est qu’elle rend l’environnement (dépendances) identique entre les différents déploiements. Cela signifie que vous pouvez le déboguer sur votre ordinateur et puis le déployer sur un autre ordinateur avec le même environnement garanti.

Une image de conteneur consiste à empaqueter une application ou le service et le déployer de manière fiable et reproductible. À cet égard, Docker n’est pas uniquement une technologie, il est également une philosophie et un processus.

Lorsque vous utilisez Docker, vous n’entendrez pas les développeurs dire, « Ça marche sur ma machine, pourquoi ne pas en production ? » Ils peuvent dire simplement, « Il s’exécute sur Docker, », car l’application Docker empaquetée peut être exécutée sur n’importe quel environnement Docker pris en charge, et il s’exécutera la façon qu'il devait sur toutes les destinations de déploiement (développement, test, intermédiaire, production, etc..).

![](./media/image3.png)

Figure 1-3 : Comparaison des machines virtuelles traditionnelles sur des conteneurs Docker

>[!div class="step-by-step"]
>[Précédent](index.md)
>[Suivant](docker-terminology.md)
