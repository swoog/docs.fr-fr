---
title: Terminologie Docker
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/21/2017
ms.openlocfilehash: 1efb2fa567bd452f0a0a5ee5afb6f759511e4145
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53151306"
---
# <a name="docker-terminology"></a>Terminologie Docker

Cette section répertorie les termes et définitions avec lequel vous devez vous familiariser avec avant de plonger plus approfondie dans Docker (pour obtenir d’autres définitions, consultez la liste complète [glossaire](https://docs.docker.com/glossary/) fourni par Docker à <https://docs.docker.com/glossary/>:

-   **Image de conteneur** un package avec toutes les dépendances et les informations nécessaires pour créer un conteneur. Une image inclut toutes les dépendances (notamment les frameworks) ainsi que le déploiement et la configuration à utiliser par le runtime du conteneur. En règle générale, une image est dérivée à partir de plusieurs images de base que sont les calques empilées les unes au-dessus des autres pour former le système de fichiers du conteneur. Une image est immuable après que qu’il a été créé.

-   **Conteneur** une instance d’une image Docker. Un conteneur représente un runtime pour une application unique, un processus ou un service. Il se compose du contenu d’une image Docker, un environnement d’exécution et un ensemble standard d’instructions. Pour mettre un service à l’échelle, vous créez plusieurs instances d’un conteneur à partir de la même image. Ou bien, un traitement par lots peut créer plusieurs conteneurs à partir de la même image, en passant des paramètres différents pour chaque instance.

-   **Balise** marque ou étiquette que vous pouvez appliquer aux images, afin que les différentes images ou des versions de la même image (selon le numéro de version ou de l’environnement de destination) peuvent être identifiées.

-   **Fichier Dockerfile** un fichier texte qui contient des instructions pour la création d’une image Docker.

-   **Build** l’action de la création d’une image de conteneur basée sur les informations et le contexte fourni par son fichier Dockerfile, ainsi que des fichiers supplémentaires dans le dossier où l’image est créée. Vous pouvez créer des images à l’aide de la commande docker build.

-   **Référentiel (également appelé référentiel)** une collection d’images Docker associées, identifiées par une balise qui indique la version de l’image. Certains dépôts contiennent plusieurs variantes d’une image spécifique, tel qu’une image contenant des kits de développement logiciel (plus lourdes), une image contenant uniquement les runtimes (plus légère), et ainsi de suite. Ces variantes peuvent être identifiées par des balises. Un référentiel unique peut contenir des variantes de plateforme, par exemple une image Linux et une image de Windows.

-   **Registre** un service qui fournit l’accès à des référentiels. Le registre par défaut utilisé pour la plupart des images publiques est [Docker Hub](https://hub.docker.com/) (propriété de l’organisation Docker). Un registre contient généralement des dépôts de plusieurs équipes. Les entreprises possèdent souvent des registres privés pour stocker et gérer les images qu’ils ont créées. *Azure Container Registry* est un autre exemple.

-   **Docker Hub** un registre public pour charger des images et de les manipuler. Docker Hub fournit un hébergement d’images Docker, des registres publics ou privés, des déclencheurs de build et des webhooks, et l’intégration avec GitHub et Bitbucket.

-   **Azure Container Registry** une ressource publique pour l’utilisation des images Docker et de ses composants dans Azure. Vous disposez ainsi d’un registre au plus près de vos déploiements dans Azure, qui vous permet de contrôler l’accès avec vos groupes et autorisations Azure Active Directory existants.

-   **Docker Trusted Registry (DTR)** service de Registre Docker (à partir de Docker) que vous pouvez installer en local afin qu’il se trouve dans le centre de données et le réseau de l’organisation. Il est pratique pour les images privées devant être gérées en interne dans l’entreprise. Docker Trusted Registry est intégré au produit Docker Datacenter. Pour plus d’informations, accédez à [ https://docs.docker.com/docker-trusted-registry/overview/ ](https://docs.docker.com/docker-trusted-registry/overview/).

-   **Docker Community Edition (CE)** des outils de développement pour Windows et macOS pour générer, en cours d’exécution et tester des conteneurs localement. Docker CE pour Windows fournit des environnements de développement pour les conteneurs Linux et Windows. L’hôte Linux Docker sur Windows est basé sur un [Hyper-V](https://www.microsoft.com/en-us/server-cloud/solutions/virtualization.aspx) machine virtuelle. L’hôte pour les conteneurs Windows est directement basé sur Windows. Docker CE pour Mac est basé sur le framework Hypervisor d’Apple et le [l’hyperviseur xhyve](https://github.com/mist64/xhyve), qui fournit une machine virtuelle de l’hôte Linux Docker sur Mac OS X. Docker CE pour Windows et pour Mac remplace Docker Toolbox, qui était basé sur Oracle VirtualBox.

-   **Docker Enterprise Edition (EE)** une version de l’échelle de l’entreprise des outils Docker pour le développement Linux et Windows.

-   **Compose** un outil de ligne de commande et un YAML file format avec les métadonnées pour la définition et l’exécution des applications. Vous définissez une application basée sur plusieurs images avec un ou plusieurs fichiers .yml qui peuvent remplacer les valeurs en fonction de l’environnement. Une fois que vous avez créé les définitions, vous pouvez déployer l’ensemble de l’application multiconteneur à l’aide d’une seule commande (docker-compose haut) qui crée un conteneur par image sur l’hôte Docker.

-   **Cluster** une collection d’hôtes Docker exposés comme s’ils étaient un hôte Docker virtuel unique afin que l’application peut s’adapter à plusieurs instances des services répartis sur plusieurs hôtes au sein du cluster. Vous pouvez créer des clusters Docker à l’aide de Docker Swarm, Mesosphere DC/OS, Kubernetes et Azure Service Fabric. (Si vous utilisez Docker Swarm pour gérer un cluster, le cluster est généralement désigné sous le nom de *swarm*.)

-   **Orchestrator** un outil qui simplifie la gestion des clusters et des hôtes Docker. L’utilisation d’orchestrateurs, vous pouvez gérer leurs images, les conteneurs et les ordinateurs hôtes via une interface CLI ou d’une interface utilisateur graphique. Vous pouvez gérer la mise en réseau des conteneurs, les configurations, l’équilibrage de charge, la découverte des services, la haute disponibilité, la configuration des hôtes Docker, et bien plus encore. Un orchestrateur gère l’exécution, la distribution, la mise à l’échelle et la réparation des charges de travail dans une collection de nœuds. En règle générale, les produits Orchestrator sont les mêmes produits qui fournissent l’infrastructure de cluster, comme Mesosphere DC/OS, Kubernetes, Docker Swarm et Azure Service Fabric.

>[!div class="step-by-step"]
>[Précédent](what-is-docker.md)
>[Suivant](docker-containers-images-and-registries.md)