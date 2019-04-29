---
title: Contrôle de l'auto-lancement de l'hôte de service WCF
ms.date: 03/30/2017
f1_keywords:
- WcfOptions
ms.assetid: 6abe5d34-519b-4cef-8f02-3c0a7f125585
ms.openlocfilehash: 2fa060e567fba9bb5e6344b2c8fc67fb639ad0f7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61608448"
---
# <a name="controlling-auto-launching-of-wcf-service-host"></a><span data-ttu-id="61fe3-102">Contrôle de l'auto-lancement de l'hôte de service WCF</span><span class="sxs-lookup"><span data-stu-id="61fe3-102">Controlling Auto-launching of WCF Service Host</span></span>
<span data-ttu-id="61fe3-103">Lorsque vous déboguez un autre projet dans la même solution Visual Studio contenant plusieurs projets, vous pouvez contrôler la fonction d’auto-lancement de l’hôte de Service Windows Communication Foundation (WCF) (WcfSvcHost.exe) pour un projet de bibliothèque de Service WCF.</span><span class="sxs-lookup"><span data-stu-id="61fe3-103">You can control the auto-launching capability of Windows Communication Foundation (WCF) Service Host (WcfSvcHost.exe) for a WCF Service Library project, when you debug another project in the same Visual Studio solution containing multiple projects.</span></span>  
  
 <span data-ttu-id="61fe3-104">Pour ce faire, cliquez sur le projet de Service WCF dans **l’Explorateur de solutions**, choisissez **propriétés**, puis cliquez sur **Options WCF** onglet. Le **démarrer WCF Service hôte lors du débogage d’un autre projet dans la même solution** case à cocher est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="61fe3-104">To do so, right-click the WCF Service Project in **Solution Explorer**, choose **Properties**, and click **WCF Options** tab. The **Start WCF Service Host when debugging another project in the same solution** check box is enabled by default.</span></span> <span data-ttu-id="61fe3-105">Vous pouvez désactiver la case pour que l’hôte de Service WCF pour ce projet spécifique n’est pas lancée lorsqu’un autre projet est débogué dans la même solution.</span><span class="sxs-lookup"><span data-stu-id="61fe3-105">You can clear the box so that WCF Service Host for this specific project is not launched when another project is debugged in the same solution.</span></span>  
  
 <span data-ttu-id="61fe3-106">Ce comportement n'affecte pas le débogage F5 ni les fonctionnalités d'ajout d'une référence de service pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="61fe3-106">This behavior does not affect the F5 debugging, or Add Service Reference functionalities for this project.</span></span>  
  
 <span data-ttu-id="61fe3-107">Cette option est disponible dans le cadre des projets suivants :</span><span class="sxs-lookup"><span data-stu-id="61fe3-107">This option is available to the following projects:</span></span>  
  
- <span data-ttu-id="61fe3-108">Projet de bibliothèque de Service WCF.</span><span class="sxs-lookup"><span data-stu-id="61fe3-108">WCF Service Library Project.</span></span>  
  
- <span data-ttu-id="61fe3-109">Projet de la bibliothèque du service du workflow séquentiel</span><span class="sxs-lookup"><span data-stu-id="61fe3-109">Sequential Workflow Service Library Project.</span></span>  
  
- <span data-ttu-id="61fe3-110">Projet de la bibliothèque du service de workflow d'ordinateur d'état</span><span class="sxs-lookup"><span data-stu-id="61fe3-110">State Machine Workflow Service Library Project.</span></span>  
  
- <span data-ttu-id="61fe3-111">Projet de la bibliothèque du service de syndication</span><span class="sxs-lookup"><span data-stu-id="61fe3-111">Syndication Service Library Project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61fe3-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61fe3-112">See also</span></span>

- [<span data-ttu-id="61fe3-113">WCF Service Host (WcfSvcHost.exe)</span><span class="sxs-lookup"><span data-stu-id="61fe3-113">WCF Service Host (WcfSvcHost.exe)</span></span>](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)
