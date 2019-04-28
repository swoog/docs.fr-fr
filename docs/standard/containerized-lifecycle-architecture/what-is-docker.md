---
title: Qu’est-ce que Docker ?
description: Obtenir un peu plus loin dans votre présentation de Docker, une analogie simple ici peut-être vous aider.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: fbb91466a86c7082e89d0ac4a3673ad83ab39b88
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61921467"
---
# <a name="what-is-docker"></a>Qu’est-ce que Docker ?

[Docker](https://www.docker.com/) est un [projet open source](https://github.com/docker/docker) permettant d’automatiser le déploiement d’applications en tant que conteneurs portables et autonomes exécutables sur le cloud ou localement. Docker est également une [entreprise](https://www.docker.com/) qui développe et diffuse cette technologie, en collaboration avec des fournisseurs de services cloud, Linux et Windows, notamment Microsoft.

![Les conteneurs Docker peuvent s’exécuter n’importe où, en local dans le centre de données client, dans un fournisseur de services externe ou dans le cloud, sur Azure.](./media/image2.png)

**Figure 1-2**. Docker déploie des conteneurs à toutes les couches du cloud hybride

Les conteneurs d’images Docker peuvent s’exécuter en mode natif sur Linux et Windows. Toutefois, les images Windows peuvent s’exécuter uniquement sur des hôtes Windows et les images Linux peuvent s’exécuter sur des hôtes Linux et des hôtes Windows (à l’aide d’une machine virtuelle Linux Hyper-V, jusqu’à présent), où le terme « hôte » désigne un serveur ou une machine virtuelle.

Les développeurs peuvent utiliser des environnements de développement sur Windows, Linux ou macOS. Sur l’ordinateur de développement, le développeur exécute un hôte Docker sur lequel sont déployées les images Docker, y compris l’application et ses dépendances. Les développeurs qui travaillent sur Linux ou sur le Mac, utilisez un hôte Docker qui est basé sur Linux, et ils peuvent uniquement créer des images pour les conteneurs Linux. (Les développeurs qui travaillent sur le Mac peuvent modifier le code ou exécuter l’interface de ligne de commande (CLI) Docker à partir de Mac OS, mais à ce jour, les conteneurs ne s’exécutent directement sur macOS.) Les développeurs qui travaillent sur Windows peuvent créer des images pour des conteneurs Windows ou Linux.

Pour héberger des conteneurs dans un environnement de développement et fournir des outils de développement supplémentaires, Docker fournit [Docker Community Edition (CE)](https://www.docker.com/community-edition) pour Windows ou macOS. Ces produits installent la machine virtuelle nécessaire (l’hôte Docker) pour héberger les conteneurs. Docker fournit aussi [Docker Enterprise Edition (EE)](https://www.docker.com/enterprise-edition), conçu pour le développement en entreprise et utilisé par les équipes informatiques qui génèrent, livrent et exécutent des applications métier stratégiques volumineuses en production.

Les [conteneurs Windows](/virtualization/windowscontainers/about/) fonctionnent avec deux types de runtime :

- **Conteneurs Windows Server** isolement des applications via une technologie d’isolation des processus et l’espace de noms. Un conteneur Windows Server partage un noyau avec l’hôte de conteneur et tous les conteneurs en cours d’exécution sur l’ordinateur hôte.

- **Conteneurs Hyper-V** développent l’isolation fournie par les conteneurs Windows Server en exécutant chaque conteneur dans une machine virtuelle hautement optimisée. Dans cette configuration, le noyau de l’hôte conteneur n’est pas partagé avec les conteneurs Hyper-V, ce qui garantit une meilleure isolation.

Les images de ces conteneurs sont créées et fonctionnent de la même façon. La différence réside dans la façon dont le conteneur est créé à partir de l’image : exécution d’un conteneur Hyper-V nécessite un paramètre supplémentaire. Pour plus d’informations, consultez [conteneurs Hyper-V](https://docs.microsoft.com/virtualization/windowscontainers/manage-containers/hyperv-container).

## <a name="comparing-docker-containers-with-virtual-machines"></a>Comparaison des conteneurs Docker avec des machines virtuelles

Figure 1-3 présente une comparaison entre les machines virtuelles et Docker conteneurs.

![Pour les machines virtuelles, il existe trois couches de base dans le serveur hôte, de bas en haut : infrastructure, système d’exploitation hôte et un hyperviseur, et par-dessus chaque machine virtuelle a son propre système d’exploitation et toutes les bibliothèques nécessaires. En revanche, pour Docker, le serveur hôte ne comprend l’infrastructure et le système d’exploitation et en plus de cela, le moteur de conteneur, qui conserve conteneur isolé, mais les services de système d’exploitation de base de partage.](./media/image3.png)

**Figure 1-3**. Comparaison des machines virtuelles traditionnelles dans des conteneurs Docker

Du fait que les conteneurs nécessitent beaucoup moins de ressources (par exemple, ils n’ont pas besoin d’un système d’exploitation complet), leur démarrage est rapide et leur déploiement est simple. Cela vous permet d’avoir une densité plus élevée, ce qui vous permet d’exécuter plus de services sur la même unité matérielle, limitant les coûts.

Comme effet secondaire de l’exécution sur le même noyau, vous obtenez une moins bonne isolation que sur les machines virtuelles.

L’objectif principal d’une image consiste à garantir le même environnement (dépendances) entre les différents déploiements. Cela signifie que vous pouvez déboguer sur votre ordinateur et puis le déployer sur un autre ordinateur, le même environnement garanti.

Une image de conteneur est un moyen pour empaqueter une application ou un service et le déployer de manière fiable et reproductible. Plus qu’une simple technologie, Docker peut également être vu comme une philosophie et un processus.

Les développeurs qui utilisent Docker ne disent pas : « Cela fonctionne sur ma machine, alors pourquoi pas en production ? » Il suffit de dire, « Il s’exécute sur Docker », car l’application Docker empaquetée peut être exécutée sur un environnement Docker, et il s’exécute comme il était censé sur toutes les cibles de déploiement (par exemple développement, test, intermédiaire et production).

## <a name="a-simple-analogy"></a>Une simple analogie

Peut-être qu’une analogie simple peut aider à bien comprendre le concept de base de Docker.

Retournons dans les années 1950 un instant. Ne portaient sur aucun processeur de word, et les photocopieurs ont été utilisés partout (Eh bien, type de).

Imaginez que vous devez émettre rapidement des lots de lettres à envoyer aux clients, avec du papier et des enveloppes, et les livrer physiquement à l’adresse de chaque client (l’e-mail n’existait pas à l’époque).

À un moment donné, vous réalisez que les lettres sont simplement une composition d’un grand ensemble de paragraphes, qui sont organisés en fonction des besoins, selon l’objectif de la lettre, donc vous concevez un système permettant d’émettre des lettres rapidement, afin d’obtenir une augmentation importante.

Le système est simple :

1. Vous commencez avec un jeu de feuilles transparentes contenant chacune un paragraphe.

2. Pour émettre un ensemble de lettres, vous choisissez les feuilles avec les paragraphes dont vous avez besoin, vous les empilez et les alignez afin de pouvoir les lire correctement.

3. Enfin, vous placez l’ensemble dans la photocopieuse, puis appuyez sur démarrer pour produire autant de lettres que nécessaire.

C’est cela l’idée fondamentale de Docker (en version simplifiée).

Dans Docker, chaque couche est un jeu de résultats des modifications qui se produisent dans le système de fichiers après l’exécution d’une commande, par exemple, l’installation d’un programme.

Par conséquent, lorsque vous « regardez » le système de fichiers une fois que la couche a été copiée, vous voyez tous les fichiers, y compris la couche lorsque le programme a été installé.

Vous pouvez considérer une image en tant que disque dur en lecture seule auxiliaire prêt à être installé dans un « ordinateur » où le système d’exploitation est déjà installé.

De même, vous pouvez considérer un conteneur comme « l’ordinateur » avec le disque dur de l’image installé. Le conteneur, tout comme un ordinateur, peut être activé ou désactivé.

>[!div class="step-by-step"]
>[Précédent](index.md)
>[Suivant](docker-terminology.md)
