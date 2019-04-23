---
title: ServiceThrottlingBehavior
ms.date: 03/30/2017
ms.assetid: 37b9e517-1f1f-4ec4-9fcb-2b8016794f5b
ms.openlocfilehash: 572e458f08c4717207667db9940296c4a957199a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59771768"
---
# <a name="servicethrottlingbehavior"></a><span data-ttu-id="c8f52-102">ServiceThrottlingBehavior</span><span class="sxs-lookup"><span data-stu-id="c8f52-102">ServiceThrottlingBehavior</span></span>
<span data-ttu-id="c8f52-103">ServiceThrottlingBehavior</span><span class="sxs-lookup"><span data-stu-id="c8f52-103">ServiceThrottlingBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c8f52-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8f52-104">Syntax</span></span>  
  
```csharp  
class ServiceThrottlingBehavior : Behavior  
{  
  sint32 MaxConcurrentCalls;  
  sint32 MaxConcurrentInstances;  
  sint32 MaxConcurrentSessions;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="c8f52-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c8f52-105">Methods</span></span>  
 <span data-ttu-id="c8f52-106">La classe ServiceThrottlingBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="c8f52-106">The ServiceThrottlingBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="c8f52-107">Properties</span><span class="sxs-lookup"><span data-stu-id="c8f52-107">Properties</span></span>  
 <span data-ttu-id="c8f52-108">La classe ServiceThrottlingBehavior a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8f52-108">The ServiceThrottlingBehavior class has the following properties:</span></span>  
  
### <a name="maxconcurrentcalls"></a><span data-ttu-id="c8f52-109">MaxConcurrentCalls</span><span class="sxs-lookup"><span data-stu-id="c8f52-109">MaxConcurrentCalls</span></span>  
 <span data-ttu-id="c8f52-110">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="c8f52-110">Data type: sint32</span></span>  
  
 <span data-ttu-id="c8f52-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8f52-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c8f52-112">Nombre maximal de messages en cours de traitement actif sur tous les objets de répartiteur dans un ServiceHost.</span><span class="sxs-lookup"><span data-stu-id="c8f52-112">The maximum number of messages actively processing across all dispatcher objects in a ServiceHost.</span></span>  
  
### <a name="maxconcurrentinstances"></a><span data-ttu-id="c8f52-113">MaxConcurrentInstances</span><span class="sxs-lookup"><span data-stu-id="c8f52-113">MaxConcurrentInstances</span></span>  
 <span data-ttu-id="c8f52-114">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="c8f52-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="c8f52-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8f52-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c8f52-116">Nombre maximal d'objets de service simultanément exécutables.</span><span class="sxs-lookup"><span data-stu-id="c8f52-116">The maximum number of service objects that can execute at one time.</span></span>  
  
### <a name="maxconcurrentsessions"></a><span data-ttu-id="c8f52-117">MaxConcurrentSessions</span><span class="sxs-lookup"><span data-stu-id="c8f52-117">MaxConcurrentSessions</span></span>  
 <span data-ttu-id="c8f52-118">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="c8f52-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="c8f52-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8f52-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c8f52-120">Nombre maximal de sessions qu'un hôte peut accepter à la fois.</span><span class="sxs-lookup"><span data-stu-id="c8f52-120">The maximum number of sessions a host can accept at one time.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c8f52-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8f52-121">Requirements</span></span>  
  
|<span data-ttu-id="c8f52-122">MOF</span><span class="sxs-lookup"><span data-stu-id="c8f52-122">MOF</span></span>|<span data-ttu-id="c8f52-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="c8f52-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="c8f52-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c8f52-124">Namespace</span></span>|<span data-ttu-id="c8f52-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="c8f52-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c8f52-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8f52-126">See also</span></span>

- <xref:System.ServiceModel.Description.ServiceThrottlingBehavior>
