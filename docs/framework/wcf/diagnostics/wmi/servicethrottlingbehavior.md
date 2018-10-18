---
title: ServiceThrottlingBehavior
ms.date: 03/30/2017
ms.assetid: 37b9e517-1f1f-4ec4-9fcb-2b8016794f5b
ms.openlocfilehash: edc154fcce0058455f1376a2a45807c92f7f2457
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49373693"
---
# <a name="servicethrottlingbehavior"></a><span data-ttu-id="da141-102">ServiceThrottlingBehavior</span><span class="sxs-lookup"><span data-stu-id="da141-102">ServiceThrottlingBehavior</span></span>
<span data-ttu-id="da141-103">ServiceThrottlingBehavior</span><span class="sxs-lookup"><span data-stu-id="da141-103">ServiceThrottlingBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="da141-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da141-104">Syntax</span></span>  
  
```csharp  
class ServiceThrottlingBehavior : Behavior  
{  
  sint32 MaxConcurrentCalls;  
  sint32 MaxConcurrentInstances;  
  sint32 MaxConcurrentSessions;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="da141-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="da141-105">Methods</span></span>  
 <span data-ttu-id="da141-106">La classe ServiceThrottlingBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="da141-106">The ServiceThrottlingBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="da141-107">Properties</span><span class="sxs-lookup"><span data-stu-id="da141-107">Properties</span></span>  
 <span data-ttu-id="da141-108">La classe ServiceThrottlingBehavior a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="da141-108">The ServiceThrottlingBehavior class has the following properties:</span></span>  
  
### <a name="maxconcurrentcalls"></a><span data-ttu-id="da141-109">MaxConcurrentCalls</span><span class="sxs-lookup"><span data-stu-id="da141-109">MaxConcurrentCalls</span></span>  
 <span data-ttu-id="da141-110">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="da141-110">Data type: sint32</span></span>  
  
 <span data-ttu-id="da141-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="da141-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="da141-112">Nombre maximal de messages en cours de traitement actif sur tous les objets de répartiteur dans un ServiceHost.</span><span class="sxs-lookup"><span data-stu-id="da141-112">The maximum number of messages actively processing across all dispatcher objects in a ServiceHost.</span></span>  
  
### <a name="maxconcurrentinstances"></a><span data-ttu-id="da141-113">MaxConcurrentInstances</span><span class="sxs-lookup"><span data-stu-id="da141-113">MaxConcurrentInstances</span></span>  
 <span data-ttu-id="da141-114">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="da141-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="da141-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="da141-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="da141-116">Nombre maximal d'objets de service simultanément exécutables.</span><span class="sxs-lookup"><span data-stu-id="da141-116">The maximum number of service objects that can execute at one time.</span></span>  
  
### <a name="maxconcurrentsessions"></a><span data-ttu-id="da141-117">MaxConcurrentSessions</span><span class="sxs-lookup"><span data-stu-id="da141-117">MaxConcurrentSessions</span></span>  
 <span data-ttu-id="da141-118">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="da141-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="da141-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="da141-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="da141-120">Nombre maximal de sessions qu'un hôte peut accepter à la fois.</span><span class="sxs-lookup"><span data-stu-id="da141-120">The maximum number of sessions a host can accept at one time.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="da141-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da141-121">Requirements</span></span>  
  
|<span data-ttu-id="da141-122">MOF</span><span class="sxs-lookup"><span data-stu-id="da141-122">MOF</span></span>|<span data-ttu-id="da141-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="da141-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="da141-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="da141-124">Namespace</span></span>|<span data-ttu-id="da141-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="da141-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="da141-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da141-126">See Also</span></span>  
 <xref:System.ServiceModel.Description.ServiceThrottlingBehavior>
