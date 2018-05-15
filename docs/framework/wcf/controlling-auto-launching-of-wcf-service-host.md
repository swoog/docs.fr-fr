---
title: Contrôle de l'auto-lancement de l'hôte de service WCF
ms.date: 03/30/2017
f1_keywords:
- WcfOptions
ms.assetid: 6abe5d34-519b-4cef-8f02-3c0a7f125585
ms.openlocfilehash: 63c3ca00c0cdc0b28de0fe245b616acd04ca50fe
ms.sourcegitcommit: 15109844229ade1c6449f48f3834db1b26907824
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2018
---
# <a name="controlling-auto-launching-of-wcf-service-host"></a><span data-ttu-id="ff670-102">Contrôle de l'auto-lancement de l'hôte de service WCF</span><span class="sxs-lookup"><span data-stu-id="ff670-102">Controlling Auto-launching of WCF Service Host</span></span>
<span data-ttu-id="ff670-103">Vous pouvez contrôler la fonction d’auto-lancement de l’hôte de Service Windows Communication Foundation (WCF) (WcfSvcHost.exe) pour un projet de bibliothèque de Service WCF lors du débogage d’un autre projet dans la même solution Visual Studio contenant plusieurs projets.</span><span class="sxs-lookup"><span data-stu-id="ff670-103">You can control the auto-launching capability of Windows Communication Foundation (WCF) Service Host (WcfSvcHost.exe) for a WCF Service Library project, when you debug another project in the same Visual Studio solution containing multiple projects.</span></span>  
  
 <span data-ttu-id="ff670-104">Pour ce faire, cliquez sur le projet de Service WCF dans **l’Explorateur de solutions**, choisissez **propriétés**, puis cliquez sur **Options WCF** onglet. Le **démarrer WCF Service hôte lors du débogage d’un autre projet dans la même solution** case à cocher est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="ff670-104">To do so, right-click the WCF Service Project in **Solution Explorer**, choose **Properties**, and click **WCF Options** tab. The **Start WCF Service Host when debugging another project in the same solution** check box is enabled by default.</span></span> <span data-ttu-id="ff670-105">Vous pouvez désactiver la case pour que l’hôte de Service WCF pour ce projet spécifique n’est pas lancé lorsqu’un autre projet est débogué dans la même solution.</span><span class="sxs-lookup"><span data-stu-id="ff670-105">You can clear the box so that WCF Service Host for this specific project is not launched when another project is debugged in the same solution.</span></span>  
  
 <span data-ttu-id="ff670-106">Ce comportement n'affecte pas le débogage F5 ni les fonctionnalités d'ajout d'une référence de service pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="ff670-106">This behavior does not affect the F5 debugging, or Add Service Reference functionalities for this project.</span></span>  
  
 <span data-ttu-id="ff670-107">Cette option est disponible dans le cadre des projets suivants :</span><span class="sxs-lookup"><span data-stu-id="ff670-107">This option is available to the following projects:</span></span>  
  
-   <span data-ttu-id="ff670-108">Projet de bibliothèque de Service WCF.</span><span class="sxs-lookup"><span data-stu-id="ff670-108">WCF Service Library Project.</span></span>  
  
-   <span data-ttu-id="ff670-109">Projet de la bibliothèque du service du workflow séquentiel</span><span class="sxs-lookup"><span data-stu-id="ff670-109">Sequential Workflow Service Library Project.</span></span>  
  
-   <span data-ttu-id="ff670-110">Projet de la bibliothèque du service de workflow d'ordinateur d'état</span><span class="sxs-lookup"><span data-stu-id="ff670-110">State Machine Workflow Service Library Project.</span></span>  
  
-   <span data-ttu-id="ff670-111">Projet de la bibliothèque du service de syndication</span><span class="sxs-lookup"><span data-stu-id="ff670-111">Syndication Service Library Project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff670-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff670-112">See Also</span></span>  
 [<span data-ttu-id="ff670-113">WCF Service Host (WcfSvcHost.exe)</span><span class="sxs-lookup"><span data-stu-id="ff670-113">WCF Service Host (WcfSvcHost.exe)</span></span>](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)
