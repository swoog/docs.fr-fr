---
title: DeliveryRequirementsAttribute
ms.date: 03/30/2017
ms.assetid: 40c5435c-a325-4cf8-9dd0-d6e24b4a56a3
ms.openlocfilehash: d294ba4f14472012b9e311ee53742633b5173f54
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33485787"
---
# <a name="deliveryrequirementsattribute"></a><span data-ttu-id="834fd-102">DeliveryRequirementsAttribute</span><span class="sxs-lookup"><span data-stu-id="834fd-102">DeliveryRequirementsAttribute</span></span>
<span data-ttu-id="834fd-103">DeliveryRequirementsAttribute</span><span class="sxs-lookup"><span data-stu-id="834fd-103">DeliveryRequirementsAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="834fd-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="834fd-104">Syntax</span></span>  
  
```  
class DeliveryRequirementsAttribute : Behavior  
{  
  string QueuedDeliveryRequirements;  
  boolean RequireOrderedDelivery;  
  string TargetContract;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="834fd-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="834fd-105">Methods</span></span>  
 <span data-ttu-id="834fd-106">La classe DeliveryRequirementsAttribute ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="834fd-106">The DeliveryRequirementsAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="834fd-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="834fd-107">Properties</span></span>  
 <span data-ttu-id="834fd-108">La classe DeliveryRequirementsAttribute a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="834fd-108">The DeliveryRequirementsAttribute class has the following properties:</span></span>  
  
### <a name="queueddeliveryrequirements"></a><span data-ttu-id="834fd-109">QueuedDeliveryRequirements</span><span class="sxs-lookup"><span data-stu-id="834fd-109">QueuedDeliveryRequirements</span></span>  
 <span data-ttu-id="834fd-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="834fd-110">Data type: string</span></span>  
  
 <span data-ttu-id="834fd-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="834fd-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="834fd-112">Spécifie si la liaison pour un service prend en charge des contrats.</span><span class="sxs-lookup"><span data-stu-id="834fd-112">Specifies whether the binding for a service supports contracts.</span></span>  
  
### <a name="requireordereddelivery"></a><span data-ttu-id="834fd-113">RequireOrderedDelivery</span><span class="sxs-lookup"><span data-stu-id="834fd-113">RequireOrderedDelivery</span></span>  
 <span data-ttu-id="834fd-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="834fd-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="834fd-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="834fd-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="834fd-116">Spécifie si la liaison prend en charge les messages ordonnés.</span><span class="sxs-lookup"><span data-stu-id="834fd-116">Specifies whether the binding supports ordered messages.</span></span>  
  
### <a name="targetcontract"></a><span data-ttu-id="834fd-117">TargetContract</span><span class="sxs-lookup"><span data-stu-id="834fd-117">TargetContract</span></span>  
 <span data-ttu-id="834fd-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="834fd-118">Data type: string</span></span>  
  
 <span data-ttu-id="834fd-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="834fd-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="834fd-120">Contrat auquel il s'applique.</span><span class="sxs-lookup"><span data-stu-id="834fd-120">The contract to which it applies.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="834fd-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="834fd-121">Requirements</span></span>  
  
|<span data-ttu-id="834fd-122">MOF</span><span class="sxs-lookup"><span data-stu-id="834fd-122">MOF</span></span>|<span data-ttu-id="834fd-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="834fd-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="834fd-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="834fd-124">Namespace</span></span>|<span data-ttu-id="834fd-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="834fd-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="834fd-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="834fd-126">See Also</span></span>  
 <xref:System.ServiceModel.DeliveryRequirementsAttribute>
