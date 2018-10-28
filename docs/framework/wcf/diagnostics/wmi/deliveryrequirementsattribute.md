---
title: DeliveryRequirementsAttribute
ms.date: 03/30/2017
ms.assetid: 40c5435c-a325-4cf8-9dd0-d6e24b4a56a3
ms.openlocfilehash: 7bfc03299fffc8070a7d8a4b3885706ea861bdf6
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/26/2018
ms.locfileid: "50042894"
---
# <a name="deliveryrequirementsattribute"></a><span data-ttu-id="013b2-102">DeliveryRequirementsAttribute</span><span class="sxs-lookup"><span data-stu-id="013b2-102">DeliveryRequirementsAttribute</span></span>
<span data-ttu-id="013b2-103">DeliveryRequirementsAttribute</span><span class="sxs-lookup"><span data-stu-id="013b2-103">DeliveryRequirementsAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="013b2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="013b2-104">Syntax</span></span>  
  
```csharp
class DeliveryRequirementsAttribute : Behavior  
{  
  string QueuedDeliveryRequirements;  
  boolean RequireOrderedDelivery;  
  string TargetContract;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="013b2-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="013b2-105">Methods</span></span>  
 <span data-ttu-id="013b2-106">La classe DeliveryRequirementsAttribute ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="013b2-106">The DeliveryRequirementsAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="013b2-107">Properties</span><span class="sxs-lookup"><span data-stu-id="013b2-107">Properties</span></span>  
 <span data-ttu-id="013b2-108">La classe DeliveryRequirementsAttribute a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="013b2-108">The DeliveryRequirementsAttribute class has the following properties:</span></span>  
  
### <a name="queueddeliveryrequirements"></a><span data-ttu-id="013b2-109">QueuedDeliveryRequirements</span><span class="sxs-lookup"><span data-stu-id="013b2-109">QueuedDeliveryRequirements</span></span>  
 <span data-ttu-id="013b2-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="013b2-110">Data type: string</span></span>  
  
 <span data-ttu-id="013b2-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="013b2-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="013b2-112">Spécifie si la liaison pour un service prend en charge des contrats.</span><span class="sxs-lookup"><span data-stu-id="013b2-112">Specifies whether the binding for a service supports contracts.</span></span>  
  
### <a name="requireordereddelivery"></a><span data-ttu-id="013b2-113">RequireOrderedDelivery</span><span class="sxs-lookup"><span data-stu-id="013b2-113">RequireOrderedDelivery</span></span>  
 <span data-ttu-id="013b2-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="013b2-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="013b2-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="013b2-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="013b2-116">Spécifie si la liaison prend en charge les messages ordonnés.</span><span class="sxs-lookup"><span data-stu-id="013b2-116">Specifies whether the binding supports ordered messages.</span></span>  
  
### <a name="targetcontract"></a><span data-ttu-id="013b2-117">TargetContract</span><span class="sxs-lookup"><span data-stu-id="013b2-117">TargetContract</span></span>  
 <span data-ttu-id="013b2-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="013b2-118">Data type: string</span></span>  
  
 <span data-ttu-id="013b2-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="013b2-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="013b2-120">Contrat auquel il s'applique.</span><span class="sxs-lookup"><span data-stu-id="013b2-120">The contract to which it applies.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="013b2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="013b2-121">Requirements</span></span>  
  
|<span data-ttu-id="013b2-122">MOF</span><span class="sxs-lookup"><span data-stu-id="013b2-122">MOF</span></span>|<span data-ttu-id="013b2-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="013b2-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="013b2-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="013b2-124">Namespace</span></span>|<span data-ttu-id="013b2-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="013b2-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="013b2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="013b2-126">See Also</span></span>  
 <xref:System.ServiceModel.DeliveryRequirementsAttribute>
