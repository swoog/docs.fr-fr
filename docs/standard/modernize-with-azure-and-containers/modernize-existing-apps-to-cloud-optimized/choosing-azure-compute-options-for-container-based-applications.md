---
title: Choisir des plates-formes de calcul Azure pour les applications conteneur
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Choisir des plates-formes de calcul Azure pour les applications conteneur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/04/2018
ms.openlocfilehash: ebf022a52aaaf95ae335976f5e097921b0ac8006
ms.sourcegitcommit: 88f251b08bf0718ce119f3d7302f514b74895038
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2018
ms.locfileid: "33958009"
---
# <a name="choosing-azure-compute-platforms-for-container-based-applications"></a>Choisir des plates-formes de calcul Azure pour les applications conteneur

Comme vous l’avez remarqué après avoir lu les sections précédentes, Azure est un cloud ouvert qui offre plusieurs choix. Vous pouvez utiliser le mieux à vos besoins, toutefois, il met également en évidence les questions sur les produits et technologies que vous devez utiliser pour vos applications en conteneur.

Comme un *par défaut* recommandation, ce qui suit est le principal critère recommandé dans ce guide :

  - **Application monolithique unique :** choisissez Azure App Service
  - **Les applications multicouches :** choisissez orchestrators comme Azure Kubernetes Service (AKS), l’infrastructure de Service (DF) ou du Service d’applications si vous avez un seul ou plusieurs services principaux
  - **Linux microservices :** AKS/Kubernetes choisissez
  - **Windows microservices :** choisissez Service Fabric
  - **Les fonctions sans serveur et les gestionnaires d’événements :** choisir les fonctions de Azure
  - **Les lots à grande échelle :** choisissez Azure par lot

Toutefois, cette recommandation convient avec un pincement de salt, comme la sélection du produit varient selon les caractéristiques et les besoins spécifiques de votre application. Toutes les applications ne sont identiques, même lorsque initialement, il peut présenter des types semblables.

Après une analyse plus approfondie des besoins de l’application, le produit sélectionné peut être différent. Mais, comme point de départ, il est recommandé d’avoir des recommandations initiales d’où vous pouvez commencer à évaluer et de test en fonction de certaine priorité.

Dans la figure suivante, vous pouvez analyser plus global lors de la table de décision détaillé.

![](./media/image8.5.png)

Notez comment le sous-jacente du système d’exploitation (Windows Visual Studio. Linux) peut également être un facteur de décision que certains orchestrators sont plus matures sur les conteneurs Linux et d’autres sur les conteneurs Windows. Par exemple, les conteneurs Linux sont très matures dans Kubernetes (AKS dans Azure), mais moins abouti sur le Service Fabric. En revanche, les conteneurs Windows sont plus matures dans Service Fabric (publiée en mai 2017) et moins mature dans AKS.

Cependant, ces différences de maturité de système d’exploitation seront fondu à l’avenir, plusieurs plateformes aura comparable au niveau de maturité de système d’exploitation et la décision dispose de plus d’informations sur les préférences en fonction des fonctionnalités spécifiques, votre application peut avoir besoin, ou en fonction de l’écosystème de chaque plate-forme raisons.


>[!div class="step-by-step"]
[Précédent](when-to-deploy-windows-containers-to-azure-container-service-kubernetes.md)
[Suivant](build-resilient-services-ready-for-the-cloud-embrace-transient-failures-in-the-cloud.md)
