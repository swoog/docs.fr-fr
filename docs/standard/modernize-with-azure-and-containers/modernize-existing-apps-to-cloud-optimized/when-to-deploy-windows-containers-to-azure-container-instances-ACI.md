---
title: Moment de déployer des conteneurs Windows à Azure conteneur Instances (ACI)
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Moment de déployer des conteneurs Windows à Azure conteneur Instances (ACI)
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/29/2018
ms.openlocfilehash: 3dc23c96543d9611763b571105f52b150dfec06f
ms.sourcegitcommit: 88f251b08bf0718ce119f3d7302f514b74895038
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2018
---
# <a name="when-to-deploy-windows-containers-to-azure-container-instances-aci"></a>Moment de déployer des conteneurs Windows à Azure conteneur Instances (ACI)

Les Instances du conteneur Azure proposition de valeur principale est que vous pouvez immédiatement déployer des conteneurs à celui-ci et que vous n’avez pas besoin de mettre à jour cet environnement, vous n’avez pas besoin/mise à niveau de correctif du système d’exploitation sous-jacent ou les machines virtuelles, tout ce qui est transparente et que vous venez de déployer conteneurs dans un environnement de prêt à l’emploi.

Les raisons et les scénarios lorsque vous ne souhaitez pas utiliser ACI sont similaires pour les principaux scénarios lorsque vous utilisez les machines virtuelles Azure avec des conteneurs, donc en fait, les principaux scénarios pour l’utilisation d’Instances de conteneurs Azure sont :

-   **Scénarios de développement/Test**
-   **Automatisation des tâches**
-   **Agents de l’élément de configuration/CD**
-   **Traitement par lots de petite/mise à l’échelle**
-   **Applications web simples**

Le scénario d’applications web simple est un scénario juste ACI mais tiennent compte que depuis dans ACI vous ne pouvez avoir qu’une instance de conteneur unique par l’image de conteneur, vous n’avez pas une haute disponibilité et avez uniquement une évolutivité limitée.

Toutefois, même lorsque ACI est considérée comme l’infrastructure, car il fournit simplement des instances d’un conteneur unique, il est un énorme avantage par rapport à des machines virtuelles Azure régulières avec Windows Server. Avec ACI, vous déployez uniquement les conteneurs dans un environnement autonome, et vous payez uniquement pour ces conteneurs. Vous n’avez pas besoin de mettre à jour/mise à jour/patch machines virtuelles, afin qu’il soit une meilleure plateforme pour la plupart des scénarios où vous utilisez peut-être machines virtuelles avec des conteneurs. À l’aide de ACI est simple, vous déployez uniquement un conteneur, il est inutile de créer un environnement de machine virtuelle que vous déployez uniquement les conteneurs.

Les principaux avantages des Instances de conteneur Azure (ACI) sont :

-   Exécuter les conteneurs sans la gestion des serveurs
-   Augmenter la réactivité des conteneurs à la demande
-   Déployer des conteneurs dans le cloud de vitesse et de simplicité sans précédent, avec une seule commande. 
-   Applications sécurisées avec l’isolation de l’hyperviseur

En résumé, vous pouvez développer des applications avec ACI rapide sans gestion des ordinateurs virtuels ou de devoir apprendre de nouveaux outils. Il s’agit simplement votre application dans un conteneur, en cours d’exécution dans le cloud.

>[!div class="step-by-step"]
[Précédent](when-to-deploy-windows-containers-to-azure-vms-iaas-cloud.md)
[Suivant](when-to-deploy-windows-containers-to-service-fabric.md)
