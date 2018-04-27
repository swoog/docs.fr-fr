---
title: Contrôle de l'auto-lancement de l'hôte de service WCF
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- WcfOptions
ms.assetid: 6abe5d34-519b-4cef-8f02-3c0a7f125585
caps.latest.revision: 8
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 5bb6356ba4698cad00d443fdb80b1a45d35e2175
ms.sourcegitcommit: 2042de78fcdceebb6b8ac4b7a292b93e8782cbf5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2018
---
# <a name="controlling-auto-launching-of-wcf-service-host"></a><span data-ttu-id="302fa-102">Contrôle de l'auto-lancement de l'hôte de service WCF</span><span class="sxs-lookup"><span data-stu-id="302fa-102">Controlling Auto-launching of WCF Service Host</span></span>
<span data-ttu-id="302fa-103">Vous pouvez contrôler la fonction d’auto-lancement de [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] hôte de Service (WcfSvcHost.exe) pour un [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] projet bibliothèque du Service, lorsque vous déboguez un autre projet dans la même solution Visual Studio contenant plusieurs projets.</span><span class="sxs-lookup"><span data-stu-id="302fa-103">You can control the auto-launching capability of [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] Service Host (WcfSvcHost.exe) for a [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] Service Library project, when you debug another project in the same Visual Studio solution containing multiple projects.</span></span>  
  
 <span data-ttu-id="302fa-104">Pour ce faire, cliquez sur le [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] projet de Service dans **l’Explorateur de solutions**, choisissez **propriétés**, puis cliquez sur **Options WCF** onglet. Le **démarrer WCF Service hôte lors du débogage d’un autre projet dans la même solution** case à cocher est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="302fa-104">To do so, right-click the [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] Service Project in **Solution Explorer**, choose **Properties**, and click **WCF Options** tab. The **Start WCF Service Host when debugging another project in the same solution** check box is enabled by default.</span></span> <span data-ttu-id="302fa-105">Vous pouvez la désactiver afin que l'hôte du service [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] de ce projet spécifique ne démarre pas lorsqu'un autre projet est débogué dans la même solution.</span><span class="sxs-lookup"><span data-stu-id="302fa-105">You can clear the box so that [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] Service Host for this specific project is not launched when another project is debugged in the same solution.</span></span>  
  
 <span data-ttu-id="302fa-106">Ce comportement n'affecte pas le débogage F5 ni les fonctionnalités d'ajout d'une référence de service pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="302fa-106">This behavior does not affect the F5 debugging, or Add Service Reference functionalities for this project.</span></span>  
  
 <span data-ttu-id="302fa-107">Cette option est disponible dans le cadre des projets suivants :</span><span class="sxs-lookup"><span data-stu-id="302fa-107">This option is available to the following projects:</span></span>  
  
-   [!INCLUDE[indigo2](../../../includes/indigo2-md.md)]<span data-ttu-id="302fa-108"> Projet de la bibliothèque du service</span><span class="sxs-lookup"><span data-stu-id="302fa-108"> Service Library Project.</span></span>  
  
-   <span data-ttu-id="302fa-109">Projet de la bibliothèque du service du workflow séquentiel</span><span class="sxs-lookup"><span data-stu-id="302fa-109">Sequential Workflow Service Library Project.</span></span>  
  
-   <span data-ttu-id="302fa-110">Projet de la bibliothèque du service de workflow d'ordinateur d'état</span><span class="sxs-lookup"><span data-stu-id="302fa-110">State Machine Workflow Service Library Project.</span></span>  
  
-   <span data-ttu-id="302fa-111">Projet de la bibliothèque du service de syndication</span><span class="sxs-lookup"><span data-stu-id="302fa-111">Syndication Service Library Project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="302fa-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="302fa-112">See Also</span></span>  
 [<span data-ttu-id="302fa-113">WCF Service Host (WcfSvcHost.exe)</span><span class="sxs-lookup"><span data-stu-id="302fa-113">WCF Service Host (WcfSvcHost.exe)</span></span>](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)
