---
title: Instances
ms.date: 03/30/2017
ms.assetid: c8cf3460-0ca1-4411-8262-e9ecaf7f0a31
ms.openlocfilehash: 1b2801b5df3a5d2ca6d7fd03299ecdf4b7df426a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54520263"
---
# <a name="instances"></a><span data-ttu-id="227ef-102">Instances</span><span class="sxs-lookup"><span data-stu-id="227ef-102">Instances</span></span>
<span data-ttu-id="227ef-103">Nom du compteur : instances.</span><span class="sxs-lookup"><span data-stu-id="227ef-103">Counter Name: Instances.</span></span>  
  
## <a name="description"></a><span data-ttu-id="227ef-104">Description</span><span class="sxs-lookup"><span data-stu-id="227ef-104">Description</span></span>  
 <span data-ttu-id="227ef-105">Nombre de contextes d'instance que le service contient actuellement.</span><span class="sxs-lookup"><span data-stu-id="227ef-105">Number of instance contexts that the service currently contains.</span></span>  
  
 <span data-ttu-id="227ef-106">La plupart du temps, le nombre de contextes d'instance est identique au nombre d'instances.</span><span class="sxs-lookup"><span data-stu-id="227ef-106">Most of the time, the number of instance contexts is identical to the number of instances.</span></span> <span data-ttu-id="227ef-107">Toutefois, les scénarios suivants constituent des exceptions à cette règle.</span><span class="sxs-lookup"><span data-stu-id="227ef-107">However, the following scenarios are exception to this rule.</span></span>  
  
-   <span data-ttu-id="227ef-108">Une méthode de service appelle la méthode <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="227ef-108">A service method calls the <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> method explicitly.</span></span>  
  
-   <span data-ttu-id="227ef-109">Un <xref:System.ServiceModel.ReleaseInstanceMode> est appliqué à une instance <xref:System.ServiceModel.OperationBehaviorAttribute>.</span><span class="sxs-lookup"><span data-stu-id="227ef-109">A <xref:System.ServiceModel.ReleaseInstanceMode> is applied to an <xref:System.ServiceModel.OperationBehaviorAttribute> instance.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="227ef-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="227ef-110">See also</span></span>
- <xref:System.ServiceModel.OperationBehaviorAttribute>
