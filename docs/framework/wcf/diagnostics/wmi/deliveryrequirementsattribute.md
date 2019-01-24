---
title: DeliveryRequirementsAttribute
ms.date: 03/30/2017
ms.assetid: 40c5435c-a325-4cf8-9dd0-d6e24b4a56a3
ms.openlocfilehash: 809e9d809bce456c831aab83c7ac19a882b2959b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54571322"
---
# <a name="deliveryrequirementsattribute"></a><span data-ttu-id="32497-102">DeliveryRequirementsAttribute</span><span class="sxs-lookup"><span data-stu-id="32497-102">DeliveryRequirementsAttribute</span></span>
<span data-ttu-id="32497-103">DeliveryRequirementsAttribute</span><span class="sxs-lookup"><span data-stu-id="32497-103">DeliveryRequirementsAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="32497-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32497-104">Syntax</span></span>  
  
```csharp
class DeliveryRequirementsAttribute : Behavior  
{  
  string QueuedDeliveryRequirements;  
  boolean RequireOrderedDelivery;  
  string TargetContract;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="32497-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="32497-105">Methods</span></span>  
 <span data-ttu-id="32497-106">La classe DeliveryRequirementsAttribute ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="32497-106">The DeliveryRequirementsAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="32497-107">Properties</span><span class="sxs-lookup"><span data-stu-id="32497-107">Properties</span></span>  
 <span data-ttu-id="32497-108">La classe DeliveryRequirementsAttribute a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="32497-108">The DeliveryRequirementsAttribute class has the following properties:</span></span>  
  
### <a name="queueddeliveryrequirements"></a><span data-ttu-id="32497-109">QueuedDeliveryRequirements</span><span class="sxs-lookup"><span data-stu-id="32497-109">QueuedDeliveryRequirements</span></span>  
 <span data-ttu-id="32497-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="32497-110">Data type: string</span></span>  
  
 <span data-ttu-id="32497-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="32497-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="32497-112">Spécifie si la liaison pour un service prend en charge des contrats.</span><span class="sxs-lookup"><span data-stu-id="32497-112">Specifies whether the binding for a service supports contracts.</span></span>  
  
### <a name="requireordereddelivery"></a><span data-ttu-id="32497-113">RequireOrderedDelivery</span><span class="sxs-lookup"><span data-stu-id="32497-113">RequireOrderedDelivery</span></span>  
 <span data-ttu-id="32497-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="32497-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="32497-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="32497-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="32497-116">Spécifie si la liaison prend en charge les messages ordonnés.</span><span class="sxs-lookup"><span data-stu-id="32497-116">Specifies whether the binding supports ordered messages.</span></span>  
  
### <a name="targetcontract"></a><span data-ttu-id="32497-117">TargetContract</span><span class="sxs-lookup"><span data-stu-id="32497-117">TargetContract</span></span>  
 <span data-ttu-id="32497-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="32497-118">Data type: string</span></span>  
  
 <span data-ttu-id="32497-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="32497-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="32497-120">Contrat auquel il s'applique.</span><span class="sxs-lookup"><span data-stu-id="32497-120">The contract to which it applies.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="32497-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="32497-121">Requirements</span></span>  
  
|<span data-ttu-id="32497-122">MOF</span><span class="sxs-lookup"><span data-stu-id="32497-122">MOF</span></span>|<span data-ttu-id="32497-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="32497-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="32497-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="32497-124">Namespace</span></span>|<span data-ttu-id="32497-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="32497-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="32497-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32497-126">See also</span></span>
- <xref:System.ServiceModel.DeliveryRequirementsAttribute>
