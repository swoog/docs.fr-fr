---
title: Applications monolithiques
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: a2fe2c325377ec49f89199ad2e36c950ebab6a24
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49374701"
---
# <a name="monolithic-applications"></a>Applications monolithiques

Dans ce scénario, vous générez une application web unique et monolithique ou le service et déployez-le en tant que conteneur. Au sein de l’application, la structure ne peut pas être monolithique ; Il peut comprendre plusieurs bibliothèques, composants ou mêmes couches (couche application, couche de domaine, couche d’accès aux données, etc.). En externe, il est un conteneur unique, comme un processus unique, application web unique ou service unique.

Pour gérer ce modèle, vous déployez un seul conteneur pour représenter l’application. Mettre à l’échelle, ajoutez simplement quelques autres copies avec un équilibreur de charge à l’avant. Cette simplicité provient de la gestion d’un déploiement unique dans un conteneur unique ou de la machine virtuelle (VM).

Le principal qu’un conteneur fait une chose uniquement et le fait dans un processus, ce modèle monolithique est en conflit. Vous pouvez inclure plusieurs composants ou bibliothèques ou couches internes dans chaque conteneur, comme illustré dans la Figure 4-1.

![](./media/image1.png)

Figure 4-1 : un exemple d’architecture de l’application monolithique

L’inconvénient de cette approche est fourni si ou quand l’application grandit, nécessitant sa mise à l’échelle. Si l’application entière est mise à l’échelle, ce n’est pas vraiment un problème. Toutefois, dans la plupart des cas, quelques parties de l’application sont des goulots nécessitant une mise à l’échelle, tandis que les autres composants sont moins utilisés.

À l’aide de l’exemple de commerce électronique ordinaire, ce que vous avez probablement besoin consiste à mettre à l’échelle le composant d’informations de produit. Les clients qui recherchent des produits sont beaucoup plus nombreux que ceux qui en achètent. Plus de clients utilisent leur panier d’achat que ceux qui utilisent le pipeline de paiement. Moins de clients ajoutent des commentaires ou consultent leur historique d’achat. Et vous avez probablement uniquement un certain nombre d’employés, d’une seule région, qui doivent gérer le contenu et les campagnes marketing. Par la mise à l’échelle de la conception monolithique, tout le code est déployé plusieurs fois.

En plus de la « mise à l’échelle-tous les éléments « problème, les modifications apportées à un seul composant nécessitent un nouveau test complet de l’application entière, mais aussi un redéploiement complet de toutes les instances.

L’approche monolithique est commun, et de nombreuses organisations développez avec cette méthode architecturale. Nombreux Profitez bien suffisamment de résultats, tandis que d’autres limites de rencontrer. Souvent conçu leurs applications dans ce modèle, car les outils et l’infrastructure étaient trop complexes pour concevoir des SOA, et elles ne voyaient la nécessité, jusqu'à ce que l’application a augmenté.

Du point de vue de l’infrastructure, chaque serveur peut exécuter de nombreuses applications au sein du même hôte et avoir un ratio acceptable d’efficacité dans votre utilisation des ressources, comme indiqué dans la Figure 4-2.

![](./media/image2.png)

Figure 4-2 : un ordinateur hôte exécutant plusieurs applications/conteneurs

Vous pouvez déployer des applications monolithiques dans Azure à l’aide de machines virtuelles dédiées pour chaque instance. À l’aide de [Azure VM Scale Sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/), vous pouvez évoluer facilement les machines virtuelles. [Azure App Service](https://azure.microsoft.com/services/app-service/) peut également exécuter des applications monolithiques et facilement mettre à l’échelle des instances sans nécessiter une gestion des machines virtuelles. Depuis 2016, Azure App Services peut exécuter des instances uniques de conteneurs Docker, ainsi, ce qui simplifie le déploiement. Et, à l’aide de Docker, vous pouvez déployer une seule machine virtuelle comme hôte Docker et exécuter plusieurs instances. À l’aide de l’équilibrage de Azure, comme illustré dans la Figure 4-3, vous pouvez gérer la mise à l’échelle.

![](./media/image3.png)

Figure 4-3 : plusieurs hôtes montée une seule application applications/conteneurs Docker

Vous pouvez gérer le déploiement sur les différents hôtes par le biais de techniques de déploiement traditionnelles. Vous pouvez gérer des hôtes Docker à l’aide des commandes telles que `docker run` manuellement, à l’aide d’automation, telles que les pipelines de livraison continue (CD), ce qui nous expliquer plus loin dans ce livre électronique.

## <a name="monolithic-application-deployed-as-a-container"></a>Application monolithique déployée comme conteneur

Il existe des avantages à l’utilisation de conteneurs pour gérer les déploiements monolithiques. La mise à l’échelle des instances des conteneurs est beaucoup plus rapide et facile que le déploiement de machines virtuelles supplémentaires. Bien que les machines virtuelles identiques sont une fonctionnalité intéressante à l’échelle de machines virtuelles, qui sont requis pour héberger vos conteneurs Docker, ils tarder à configurer. Quand une machine virtuelle est déployée en tant qu’instance de l’application, la configuration de l’application est gérée en interne par la machine virtuelle.

Le déploiement de mises à jour comme images Docker est beaucoup plus rapide et efficace du point de vue du réseau. Les instances Vn peuvent être configurés sur les mêmes hôtes que vos instances Vn-1, en éliminant les coûts supplémentaires résultant des machines virtuelles supplémentaires. Les images docker démarrent généralement en quelques secondes, ce qui accélère les déploiements. Destruction d’une instance Docker est aussi simple que l’appel de la `docker stop` commande, normalement moins d’une seconde.

Étant donné que les conteneurs sont immuables, par conception, vous devez jamais à vous soucier d’endommagement des machines virtuelles, car vous avez oublié par un script de mise à jour pour prendre en compte une configuration spécifique ou d’un fichier restant sur le disque.

Bien que les applications monolithiques peuvent tirer parti de Docker, nous touchons sur uniquement les conseils des avantages. Les avantages de plus grande de la gestion des conteneurs provient de déploiement avec des orchestrateurs de conteneur qui gèrent les différentes instances et le même cycle de vie de chaque instance de conteneur. La décomposition de l’application monolithique en sous-systèmes qui peuvent être mis à l’échelle, développés et déployés individuellement est votre point d’entrée dans le domaine des microservices.

## <a name="publishing-a-single-docker-container-app-to-azure-app-service"></a>Publication d’une seule application de conteneur Docker sur Azure App Service

Soit parce que vous souhaitez obtenir une validation rapide d’un conteneur déployé sur Azure, soit parce que l’application est simplement une application de conteneur unique, Azure App Services fournit un excellent moyen de fournir des services évolutifs de conteneur unique.

À l’aide d’Azure App Service est intuitif et vous pouvez être opérationnel et en cours d’exécution rapidement, car elle fournit Git excellente intégration à votre code, générez-le dans Microsoft Visual Studio et déployer directement dans Azure. Mais, traditionnellement (avec aucune Docker), si vous avez besoin d’autres fonctionnalités, les frameworks ou dépendances qui ne sont pas pris en charge dans les Services d’application, vous nécessaire d’attendre jusqu'à ce que l’équipe Azure met à jour ces dépendances dans App Service ou basculé vers d’autres services tels que Service Fabric, Services Cloud ou même simple des machines virtuelles, pour lequel vous avez davantage de contrôle et pourrez installer un framework ou un composant requis pour votre application.

Maintenant, toutefois, (annoncée à Microsoft Connect 2016 en novembre 2016) et comme indiqué dans la Figure 4‑4, lorsque vous utilisez Visual Studio 2017, prise en charge des conteneurs dans Azure App Service vous donne la possibilité d’inclure tout ce que vous voulez dans votre environnement d’application. Si vous avez ajouté une dépendance à votre application, car vous l’exécutez dans un conteneur, vous obtenez la fonctionnalité d’inclusion de ces dépendances dans votre image de fichier Dockerfile ou Docker.

![](./media/image4.png)

Figure 4-4 : publication d’un conteneur sur Azure App Service à partir de Visual Studio applications/conteneurs

Figure 4-4 montre également que le flux de publication envoie une image via un Registre de conteneurs, qui peut être Azure Container Registry (un Registre de près à vos déploiements dans Azure et sécurisés par les comptes et groupes Azure Active Directory) ou tout autre registre Docker comme les registres Docker Hub ou en local.


>[!div class="step-by-step"]
[Précédent](common-container-design-principles.md)
[Suivant](state-and-data-in-docker-applications.md)
