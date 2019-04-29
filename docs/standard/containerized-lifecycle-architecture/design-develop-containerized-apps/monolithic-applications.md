---
title: Applications monolithiques
description: Comprendre les concepts fondamentaux pour conteneuriser des applications monolithiques.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: e7454100b09f602e1e103c38685609e1dab62fe9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61644962"
---
# <a name="monolithic-applications"></a>Applications monolithiques

Dans ce scénario, vous créez une application web unique et monolithique ou le service et déployez-le en tant que conteneur. Au sein de l’application, la structure ne peut pas être monolithique ; Il peut comprendre plusieurs bibliothèques, composants ou mêmes couches (couche application, couche de domaine, couche d’accès aux données, etc.). En externe, il est un conteneur unique, comme un processus unique, application web unique ou service unique.

Pour gérer ce modèle, vous déployez un seul conteneur pour représenter l’application. Mettre à l’échelle, ajoutez simplement quelques autres copies avec un équilibreur de charge à l’avant. Cette simplicité provient de la gestion d’un déploiement unique dans un conteneur unique ou de la machine virtuelle (VM).

Le principal qu’un conteneur fait une chose uniquement et le fait dans un processus, ce modèle monolithique est en conflit. Vous pouvez inclure plusieurs composants ou bibliothèques ou couches internes dans chaque conteneur, comme illustré dans la Figure 4-1.

![Une application monolithique a toutes ou la plupart de ses fonctionnalités dans un processus unique ou un conteneur, et elle est organisée en composants dans les couches internes ou des bibliothèques.](./media/image1.png)

**Figure 4-1.** Un exemple d’architecture d’application monolithique

L’inconvénient de cette approche est fourni si ou quand l’application grandit, nécessitant sa mise à l’échelle. Si l’application entière est mise à l’échelle, ce n’est pas vraiment un problème. Toutefois, dans la plupart des cas, quelques parties de l’application sont des goulots nécessitant une mise à l’échelle, tandis que les autres composants sont moins utilisés.

À l’aide de l’exemple de commerce électronique ordinaire, ce que vous avez probablement besoin consiste à mettre à l’échelle le composant d’informations de produit. Les clients qui recherchent des produits sont beaucoup plus nombreux que ceux qui en achètent. Plus de clients utilisent leur panier d’achat que ceux qui utilisent le pipeline de paiement. Moins de clients ajoutent des commentaires ou consultent leur historique d’achat. Et vous avez probablement uniquement un certain nombre d’employés, d’une seule région, qui doivent gérer le contenu et les campagnes marketing. Par la mise à l’échelle de la conception monolithique, tout le code est déployé plusieurs fois.

En plus de la « mise à l’échelle-tous les éléments « problème, les modifications apportées à un seul composant nécessitent un nouveau test complet de l’application entière, mais aussi un redéploiement complet de toutes les instances.

L’approche monolithique est commun, et de nombreuses organisations développez avec cette méthode architecturale. Nombreux Profitez bien suffisamment de résultats, tandis que d’autres limites de rencontrer. Souvent conçu leurs applications dans ce modèle, car les outils et l’infrastructure étaient trop complexes pour concevoir des SOA, et elles ne voyaient la nécessité, jusqu'à ce que l’application a augmenté.

Du point de vue de l’infrastructure, chaque serveur peut exécuter de nombreuses applications au sein du même hôte et avoir un ratio acceptable d’efficacité dans votre utilisation des ressources, comme indiqué dans la Figure 4-2.

![Un seul hôte peut exécuter plusieurs applications dans des conteneurs distincts.](./media/image2.png)

**Figure 4-2.** Un ordinateur hôte exécutant plusieurs applications/conteneurs

Enfin, du point de vue de la disponibilité, les applications monolithiques doivent être déployées ensemble ; Cela signifie que, au cas où vous devez *arrêter et démarrer*, toutes les fonctionnalités et tous les utilisateurs seront affectés au cours de la fenêtre de déploiement. Dans certaines situations, l’utilisation d’Azure et les conteneurs permettre réduire ces situations et réduisent la probabilité de temps d’arrêt de votre application, comme vous pouvez le voir dans la Figure 4-3.

Vous pouvez déployer des applications monolithiques dans Azure à l’aide de machines virtuelles dédiées pour chaque instance. À l’aide de [Azure VM Scale Sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/), vous pouvez évoluer facilement les machines virtuelles.

Vous pouvez également utiliser [Azure App Services](https://azure.microsoft.com/services/app-service/) pour exécuter des applications monolithiques et facilement mettre à l’échelle d’instances sans avoir à gérer les machines virtuelles. Azure App Services peut exécuter des instances uniques de conteneurs Docker, également, ce qui simplifie le déploiement.

Vous pouvez déployer plusieurs machines virtuelles en tant qu’hôtes Docker et exécuter n’importe quel nombre de conteneurs par machine virtuelle. Ensuite, en utilisant un équilibreur de charge Azure, comme illustré dans la Figure 4-3, vous pouvez gérer mise à l’échelle.

![Une application monolithique peut être montée à des hôtes différents où chacun d’eux s’exécute l’application dans des conteneurs.](./media/image3.png)

**Figure 4-3**. Plusieurs hôtes de l’évolution horizontale une seule application applications/conteneurs Docker

Vous pouvez gérer le déploiement des hôtes eux-mêmes par le biais de techniques de déploiement traditionnelles.

Vous pouvez gérer des conteneurs Docker à partir de la ligne de commande à l’aide des commandes telles que `docker run` et `docker-compose up`, et vous pouvez également automatiser dans les pipelines de livraison continue (CD) et le déployer sur des hôtes Docker à partir d’Azure DevOps Services, par exemple.

## <a name="monolithic-application-deployed-as-a-container"></a>Application monolithique déployée comme conteneur

Il existe des avantages à l’utilisation de conteneurs pour gérer les déploiements monolithiques. La mise à l’échelle des instances des conteneurs est beaucoup plus rapide et facile que le déploiement de machines virtuelles supplémentaires.

Le déploiement de mises à jour comme images Docker est beaucoup plus rapide et efficace du point de vue du réseau. Conteneurs docker démarrent généralement en secondes, ce qui accélère les déploiements. Destruction d’un conteneur Docker est aussi simple que l’appel de la `docker stop` commande, normalement moins d’une seconde.

Étant donné que les conteneurs sont immuables, par conception, vous devez jamais à vous soucier d’endommagement des machines virtuelles, car vous avez oublié par un script de mise à jour pour prendre en compte une configuration spécifique ou d’un fichier restant sur le disque.

Bien que les applications monolithiques peuvent tirer parti de Docker, nous touchons sur uniquement les conseils des avantages. Les avantages de plus grande de la gestion des conteneurs proviennent du déploiement avec des orchestrateurs de conteneurs qui gèrent les différentes instances et le même cycle de vie de chaque instance de conteneur. La décomposition de l’application monolithique en sous-systèmes qui peuvent être mis à l’échelle, développés et déployés individuellement est votre point d’entrée dans le domaine des microservices.

Pour en savoir plus sur la « lift- and -shift » des applications monolithiques avec des conteneurs et comment vous pouvez moderniser vos applications, vous pouvez lire ce guide Microsoft supplémentaire, [moderniser des applications .NET existantes avec le cloud Azure et les conteneurs Windows ](../../modernize-with-azure-and-containers/index.md), que vous pouvez également télécharger au format PDF à partir de <https://aka.ms/LiftAndShiftWithContainersEbook>.

## <a name="publish-a-single-docker-container-app-to-azure-app-service"></a>Publier une application de conteneur unique sur Azure App Service

Soit parce que vous souhaitez obtenir une validation rapide d’un conteneur déployé sur Azure, soit parce que l’application est simplement une application de conteneur unique, Azure App Services fournit un excellent moyen de fournir des services évolutifs de conteneur unique.

À l’aide d’Azure App Service est intuitif et vous pouvez être opérationnel et en cours d’exécution rapidement, car elle fournit Git excellente intégration à votre code, générez-le dans Microsoft Visual Studio et déployer directement dans Azure. Mais, traditionnellement (avec aucune Docker), si vous avez besoin d’autres fonctionnalités, les frameworks ou dépendances qui ne sont pas pris en charge dans les Services d’application, vous nécessaire d’attendre jusqu'à ce que l’équipe Azure met à jour ces dépendances dans App Service ou basculé vers d’autres services tels que Service Fabric, Services Cloud ou même simple des machines virtuelles, pour lequel vous avez davantage de contrôle et pourrez installer un framework ou un composant requis pour votre application.

À présent, comme illustré dans la Figure 4-4, lorsque vous utilisez Visual Studio 2017, prise en charge des conteneurs dans Azure App Service vous donne la possibilité d’inclure tout ce que vous voulez dans votre environnement d’application. Si vous avez ajouté une dépendance à votre application, car vous l’exécutez dans un conteneur, vous obtenez la fonctionnalité d’inclusion de ces dépendances dans votre image de fichier Dockerfile ou Docker.

![Affichage de l’Assistant de Visual Studio pour publier sur un service d’application Azure, la mise en surbrillance le sélecteur pour le Registre de conteneurs.](./media/image4.png)

**Figure 4-4**. Publication d’un conteneur sur Azure App Service à partir de Visual Studio/conteneurs d’applications

Figure 4-4 montre également que le flux de publication envoie une image via un Registre de conteneurs, qui peut être Azure Container Registry (un Registre de près à vos déploiements dans Azure et sécurisés par les comptes et groupes Azure Active Directory) ou tout autre registre Docker comme les registres Docker Hub ou en local.

>[!div class="step-by-step"]
>[Précédent](common-container-design-principles.md)
>[Suivant](state-and-data-in-docker-applications.md)
