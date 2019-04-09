---
title: DeliveryRequirementsAttribute
ms.date: 03/30/2017
ms.assetid: 40c5435c-a325-4cf8-9dd0-d6e24b4a56a3
ms.openlocfilehash: c81e4b27969d879a70806082f48879cbf1b32ccc
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59101775"
---
# <a name="deliveryrequirementsattribute"></a><span data-ttu-id="fcb5d-102">DeliveryRequirementsAttribute</span><span class="sxs-lookup"><span data-stu-id="fcb5d-102">DeliveryRequirementsAttribute</span></span>
<span data-ttu-id="fcb5d-103">DeliveryRequirementsAttribute</span><span class="sxs-lookup"><span data-stu-id="fcb5d-103">DeliveryRequirementsAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fcb5d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fcb5d-104">Syntax</span></span>  
  
```csharp
class DeliveryRequirementsAttribute : Behavior  
{  
  string QueuedDeliveryRequirements;  
  boolean RequireOrderedDelivery;  
  string TargetContract;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="fcb5d-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fcb5d-105">Methods</span></span>  
 <span data-ttu-id="fcb5d-106">La classe DeliveryRequirementsAttribute ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-106">The DeliveryRequirementsAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="fcb5d-107">Properties</span><span class="sxs-lookup"><span data-stu-id="fcb5d-107">Properties</span></span>  
 <span data-ttu-id="fcb5d-108">La classe DeliveryRequirementsAttribute a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="fcb5d-108">The DeliveryRequirementsAttribute class has the following properties:</span></span>  
  
### <a name="queueddeliveryrequirements"></a><span data-ttu-id="fcb5d-109">QueuedDeliveryRequirements</span><span class="sxs-lookup"><span data-stu-id="fcb5d-109">QueuedDeliveryRequirements</span></span>  
 <span data-ttu-id="fcb5d-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="fcb5d-110">Data type: string</span></span>  
  
 <span data-ttu-id="fcb5d-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="fcb5d-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="fcb5d-112">Spécifie si la liaison pour un service prend en charge des contrats.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-112">Specifies whether the binding for a service supports contracts.</span></span>  
  
### <a name="requireordereddelivery"></a><span data-ttu-id="fcb5d-113">RequireOrderedDelivery</span><span class="sxs-lookup"><span data-stu-id="fcb5d-113">RequireOrderedDelivery</span></span>  
 <span data-ttu-id="fcb5d-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="fcb5d-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="fcb5d-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="fcb5d-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="fcb5d-116">Spécifie si la liaison prend en charge les messages ordonnés.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-116">Specifies whether the binding supports ordered messages.</span></span>  
  
### <a name="targetcontract"></a><span data-ttu-id="fcb5d-117">TargetContract</span><span class="sxs-lookup"><span data-stu-id="fcb5d-117">TargetContract</span></span>  
 <span data-ttu-id="fcb5d-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="fcb5d-118">Data type: string</span></span>  
  
 <span data-ttu-id="fcb5d-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="fcb5d-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="fcb5d-120">Contrat auquel il s'applique.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-120">The contract to which it applies.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fcb5d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fcb5d-121">Requirements</span></span>  
  
|<span data-ttu-id="fcb5d-122">MOF</span><span class="sxs-lookup"><span data-stu-id="fcb5d-122">MOF</span></span>|<span data-ttu-id="fcb5d-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="fcb5d-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fcb5d-124">Namespace</span></span>|<span data-ttu-id="fcb5d-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="fcb5d-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="fcb5d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcb5d-126">See also</span></span>

- <xref:System.ServiceModel.DeliveryRequirementsAttribute>
