---
title: Instances
ms.date: 03/30/2017
ms.assetid: c8cf3460-0ca1-4411-8262-e9ecaf7f0a31
ms.openlocfilehash: a95acf8e775e0802dc0ed781c562fa6373995a70
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33473040"
---
# <a name="instances"></a><span data-ttu-id="fe2d9-102">Instances</span><span class="sxs-lookup"><span data-stu-id="fe2d9-102">Instances</span></span>
<span data-ttu-id="fe2d9-103">Nom du compteur : Instances.</span><span class="sxs-lookup"><span data-stu-id="fe2d9-103">Counter Name: Instances.</span></span>  
  
## <a name="description"></a><span data-ttu-id="fe2d9-104">Description</span><span class="sxs-lookup"><span data-stu-id="fe2d9-104">Description</span></span>  
 <span data-ttu-id="fe2d9-105">Nombre de contextes d'instance que le service contient actuellement.</span><span class="sxs-lookup"><span data-stu-id="fe2d9-105">Number of instance contexts that the service currently contains.</span></span>  
  
 <span data-ttu-id="fe2d9-106">La plupart du temps, le nombre de contextes d'instance est identique au nombre d'instances.</span><span class="sxs-lookup"><span data-stu-id="fe2d9-106">Most of the time, the number of instance contexts is identical to the number of instances.</span></span> <span data-ttu-id="fe2d9-107">Toutefois, les scénarios suivants constituent des exceptions à cette règle.</span><span class="sxs-lookup"><span data-stu-id="fe2d9-107">However, the following scenarios are exception to this rule.</span></span>  
  
-   <span data-ttu-id="fe2d9-108">Une méthode de service appelle la méthode <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="fe2d9-108">A service method calls the <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> method explicitly.</span></span>  
  
-   <span data-ttu-id="fe2d9-109">Un <xref:System.ServiceModel.ReleaseInstanceMode> est appliqué à une instance <xref:System.ServiceModel.OperationBehaviorAttribute>.</span><span class="sxs-lookup"><span data-stu-id="fe2d9-109">A <xref:System.ServiceModel.ReleaseInstanceMode> is applied to an <xref:System.ServiceModel.OperationBehaviorAttribute> instance.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe2d9-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe2d9-110">See Also</span></span>  
 <xref:System.ServiceModel.OperationBehaviorAttribute>
