---
title: Terminologie Docker
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
keywords: Docker, microservices, ASP.NET, conteneur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/21/2017
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: a622b2949c1d2277bb3e82617a5bc2d8cb432263
ms.sourcegitcommit: 15316053918995cc1380163a7d7e7edd5c44e6d7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2018
---
# <a name="docker-terminology"></a>Terminologie Docker

Cette section répertorie les termes et définitions avec lequel vous devez vous familiariser avec avant d’aborder plus approfondie pour Docker (pour les autres définitions, consultez l’étendue [glossaire](https://docs.docker.com/glossary/) fournie par Docker à <https://docs.docker.com/glossary/>:

-   **Image de conteneur** un package avec toutes les dépendances et les informations nécessaires pour créer un conteneur. Une image inclut toutes les dépendances (par exemple, des infrastructures) ainsi que le déploiement et la configuration à utiliser par un conteneur d’exécution. En règle générale, une image déduit à partir de plusieurs images de base que sont couches empilés un au-dessus de l’autre pour former le système de fichiers du conteneur. Une image est immuable après que qu’elle a été créée.

-   **Conteneur** une instance d’une image Docker. Un conteneur représente un runtime pour une application unique, un processus ou un service. Il se compose du contenu d’une image Docker, un environnement d’exécution et un ensemble standard d’instructions. Pour mettre un service à l’échelle, vous créez plusieurs instances d’un conteneur à partir de la même image. Ou bien, un traitement par lots peut créer plusieurs conteneurs à partir de la même image, en passant des paramètres différents pour chaque instance.

-   **Balise** une marque ou l’étiquette que vous pouvez appliquer aux images afin que des images ou des versions de la même image (selon le numéro de version ou de l’environnement de destination) peuvent être identifiées.

-   **Fichier Dockerfile** un fichier texte qui contient des instructions pour la création d’une image Docker.

-   **Build** l’action de création d’une image de conteneur en fonction des informations et du contexte fourni par son fichier Dockerfile, ainsi que les autres fichiers dans le dossier où l’image est créée. Vous pouvez créer des images à l’aide de la commande de génération docker Docker.

-   **Référentiel (également appelée référentiel)** une collection d’images Docker connexes identifié par une balise qui indique la version de l’image. Certains référentiels contiennent plusieurs variantes d’une image spécifique, tel qu’une image contenant des kits de développement logiciel (plus), une image contenant uniquement les runtimes (plus claires), et ainsi de suite. Ces variantes peuvent être identifiées par des balises. Un référentiel unique peut contenir des variantes de plateforme, par exemple une image Linux et une image système Windows.

-   **Registre** un service qui fournit l’accès à des référentiels. Le registre par défaut utilisé pour la plupart des images publiques est [Docker Hub](https://hub.docker.com/) (propriété de l’organisation Docker). Un registre contient généralement des dépôts de plusieurs équipes. Les entreprises ont souvent des registres privés pour stocker et gérer les images qu’ils ont créées. *Registre de conteneur Azure* est un autre exemple.

-   **Hub docker** un registre public pour le téléchargement d’images et de les manipuler. Docker Hub fournit un hébergement d’images Docker, des registres publics ou privés, des déclencheurs de build et des webhooks, et l’intégration avec GitHub et Bitbucket.

-   **Registre de conteneur Azure** une ressource publique pour travailler avec les images Docker et ses composants dans Azure. Vous disposez ainsi d’un registre au plus près de vos déploiements dans Azure, qui vous permet de contrôler l’accès avec vos groupes et autorisations Azure Active Directory existants.

-   **Docker Trusted Registre DTR ()** service de Registre A Docker (à partir de Docker) que vous pouvez installer localement afin qu’il se trouve dans le centre de données et le réseau de l’organisation. Il est pratique pour les images privées devant être gérées en interne dans l’entreprise. Docker Trusted Registry est intégré au produit Docker Datacenter. Pour plus d’informations, accédez à [ https://docs.docker.com/docker-trusted-registry/overview/ ](https://docs.docker.com/docker-trusted-registry/overview/).

-   **Docker Community Edition (CE)** les outils de développement pour Windows et macOS pour générer, en cours d’exécution et tester localement des conteneurs. Docker CE pour Windows fournit des environnements de développement pour les conteneurs Linux et Windows. L’hôte Linux Docker sur Windows est basée sur un [Hyper-V](https://www.microsoft.com/en-us/server-cloud/solutions/virtualization.aspx) machine virtuelle. L’hôte pour les conteneurs Windows est directement basé sur Windows. Docker CE pour Mac est basée sur l’infrastructure de l’hyperviseur d’Apple et le [xhyve hyperviseur](https://github.com/mist64/xhyve), qui fournit une machine virtuelle de l’hôte Linux Docker sur Mac OS X. Docker CE pour Windows et Mac remplace boîte à outils Docker, qui était basé sur Oracle VirtualBox.

-   **Docker Enterprise Edition (EE)** une version de l’entreprise à l’échelle des outils de Docker pour le développement Linux et Windows.

-   **Composer** un outil de ligne de commande et les YAML file format avec les métadonnées pour la définition et l’exécution d’applications multicontainer. Vous définissez une application basée sur plusieurs images avec un ou plusieurs fichiers .yml qui peuvent remplacer les valeurs en fonction de l’environnement. Après avoir créé les définitions, vous pouvez déployer l’application multicontainer entière à l’aide d’une commande unique (docker-composer des) qui crée un conteneur par image sur l’hôte Docker.

-   **Cluster** une collection d’hôtes Docker exposé comme s’il s’agissait d’un seul hôte Docker virtuel afin que l’application peut s’adapter à plusieurs instances des services répartis sur plusieurs hôtes au sein du cluster. Vous pouvez créer des clusters de Docker à l’aide de Docker Swarm mésosphère DC/OS, Kubernetes et Azure Service Fabric. (Si vous utilisez Docker Swarm pour gérer un cluster, le cluster est généralement désigné sous le nom de *swarm*.)

-   **Orchestrator** un outil qui simplifie la gestion de clusters et hôtes de Docker. À l’aide d’orchestrators, vous pouvez gérer leurs images, les conteneurs et les ordinateurs hôtes via une interface CLI ou une interface utilisateur graphique. Vous pouvez gérer la mise en réseau des conteneurs, les configurations, l’équilibrage de charge, la découverte des services, la haute disponibilité, la configuration des hôtes Docker, et bien plus encore. Un orchestrateur gère l’exécution, la distribution, la mise à l’échelle et la réparation des charges de travail dans une collection de nœuds. En règle générale, les produits Orchestrator sont les mêmes produits qui fournissent l’infrastructure de cluster, comme Mesosphere DC/OS, Kubernetes, Docker Swarm et Azure Service Fabric.


>[!div class="step-by-step"]
[Précédente] (scénario-est-docker.md) [suivant] (docker-conteneurs-images-et-registries.md)
