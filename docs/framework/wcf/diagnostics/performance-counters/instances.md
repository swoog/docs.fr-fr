---
title: Instances
ms.date: 03/30/2017
ms.assetid: c8cf3460-0ca1-4411-8262-e9ecaf7f0a31
ms.openlocfilehash: 668cfb3026b9ab7259665f5e53873a512b1e2238
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59118987"
---
# <a name="instances"></a><span data-ttu-id="1aab3-102">Instances</span><span class="sxs-lookup"><span data-stu-id="1aab3-102">Instances</span></span>
<span data-ttu-id="1aab3-103">Nom du compteur : instances.</span><span class="sxs-lookup"><span data-stu-id="1aab3-103">Counter Name: Instances.</span></span>  
  
## <a name="description"></a><span data-ttu-id="1aab3-104">Description</span><span class="sxs-lookup"><span data-stu-id="1aab3-104">Description</span></span>  
 <span data-ttu-id="1aab3-105">Nombre de contextes d'instance que le service contient actuellement.</span><span class="sxs-lookup"><span data-stu-id="1aab3-105">Number of instance contexts that the service currently contains.</span></span>  
  
 <span data-ttu-id="1aab3-106">La plupart du temps, le nombre de contextes d'instance est identique au nombre d'instances.</span><span class="sxs-lookup"><span data-stu-id="1aab3-106">Most of the time, the number of instance contexts is identical to the number of instances.</span></span> <span data-ttu-id="1aab3-107">Toutefois, les scénarios suivants constituent des exceptions à cette règle.</span><span class="sxs-lookup"><span data-stu-id="1aab3-107">However, the following scenarios are exception to this rule.</span></span>  
  
-   <span data-ttu-id="1aab3-108">Une méthode de service appelle la méthode <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="1aab3-108">A service method calls the <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> method explicitly.</span></span>  
  
-   <span data-ttu-id="1aab3-109">Un <xref:System.ServiceModel.ReleaseInstanceMode> est appliqué à une instance <xref:System.ServiceModel.OperationBehaviorAttribute>.</span><span class="sxs-lookup"><span data-stu-id="1aab3-109">A <xref:System.ServiceModel.ReleaseInstanceMode> is applied to an <xref:System.ServiceModel.OperationBehaviorAttribute> instance.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1aab3-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1aab3-110">See also</span></span>

- <xref:System.ServiceModel.OperationBehaviorAttribute>
