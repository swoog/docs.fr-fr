---
title: Choix des plateformes de calcul Azure pour les applications basées sur des conteneurs
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Choisir des plates-formes de calcul Azure pour les applications en conteneur
ms.date: 05/04/2018
ms.openlocfilehash: 28e103c67f47d63582384c9ab468a5f631b5ce9e
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65638977"
---
# <a name="choosing-azure-compute-platforms-for-container-based-applications"></a>Choix des plateformes de calcul Azure pour les applications basées sur des conteneurs

Comme vous l’avez remarqué après avoir lu les sections précédentes, Azure est un cloud ouverte qui offre plusieurs choix. Vous pouvez utiliser la mieux adaptée à vos besoins, toutefois, il met également en évidence questions sur les produits et technologies que vous devez utiliser pour vos applications en conteneur.

Comme un *par défaut* recommandation, ce qui suit est le principal critère recommandé dans ce guide :

- **Application monolithique unique :** Choisissez Azure App Service
- **Application multiniveau :** Choisissez des orchestrateurs tels que App Service, Service Fabric (SF) ou Azure Kubernetes Service (AKS) si vous avez un seul ou plusieurs services back-end
- **Microservices de Linux :** Choisissez AKS/Kubernetes
- **Microservices de Windows :** Choisissez Service Fabric
- **& Gestionnaires d’événements de fonctions sans serveur :** Choisissez Azure Functions
- **Lots à grande échelle :** Choisissez Azure Batch

Toutefois, cette recommandation à entreprendre avec une pincée de salt, comme la sélection du produit varie selon les besoins spécifiques de votre application et de caractéristiques. Pas toutes les applications sont les mêmes, même lorsque initialement, il peut présenter des types similaires.

Après une analyse plus approfondie des besoins de l’application, le produit sélectionné peut être différent. Mais, en tant que point de départ, il est judicieux d’avoir des recommandations initiales relatives à partir d’où vous pouvez commencer à évaluer et de test en fonction de certaine priorité.

Dans la figure suivante, vous pouvez analyser plus global lors de la table de prise de décision détaillé.

![](./media/image8.5.png)

Notez comment la sous-jacente du système d’exploitation (Windows Visual Studio. Linux) peut également être un facteur de décision que certains orchestrateurs sont plus mature sur des conteneurs Linux et d’autres sur les conteneurs Windows. Par exemple, les conteneurs Linux sont parvenues à maturité dans Kubernetes (AKS dans Azure), mais moins reconnue sur Service Fabric. En revanche, les conteneurs Windows sont plus mature dans Service Fabric (publiée en mai 2017) et moins reconnue dans ACS.

Cependant, ces différences de maturité de système d’exploitation seront estompe à l’avenir, plusieurs plateformes auront comparable maturité du système d’exploitation et la décision sera mise en page plus sur les préférences en fonction des fonctionnalités spécifiques, votre application peut avoir besoin, ou en fonction de l’écosystème de chaque plateforme raisons.

> [!div class="step-by-step"]
> [Précédent](when-to-deploy-windows-containers-to-azure-container-service-kubernetes.md)
> [Suivant](build-resilient-services-ready-for-the-cloud-embrace-transient-failures-in-the-cloud.md)
