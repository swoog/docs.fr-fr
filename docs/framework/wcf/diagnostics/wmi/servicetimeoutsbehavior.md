---
title: ServiceTimeoutsBehavior
ms.date: 03/30/2017
ms.assetid: 4412525d-a3cc-4eae-b3e8-a50ce766d09d
ms.openlocfilehash: 1a5284915de739e95325234318842a4d1ab607be
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50196966"
---
# <a name="servicetimeoutsbehavior"></a><span data-ttu-id="b0d9e-102">ServiceTimeoutsBehavior</span><span class="sxs-lookup"><span data-stu-id="b0d9e-102">ServiceTimeoutsBehavior</span></span>
<span data-ttu-id="b0d9e-103">ServiceTimeoutsBehavior</span><span class="sxs-lookup"><span data-stu-id="b0d9e-103">ServiceTimeoutsBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b0d9e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0d9e-104">Syntax</span></span>  
  
```csharp
class ServiceTimeoutsBehavior : Behavior  
{  
  datetime TransactionTimeout;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="b0d9e-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b0d9e-105">Methods</span></span>  
 <span data-ttu-id="b0d9e-106">La classe ServiceTimeoutsBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="b0d9e-106">The ServiceTimeoutsBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="b0d9e-107">Properties</span><span class="sxs-lookup"><span data-stu-id="b0d9e-107">Properties</span></span>  
 <span data-ttu-id="b0d9e-108">La classe ServiceTimeoutsBehavior a la propriété suivante :</span><span class="sxs-lookup"><span data-stu-id="b0d9e-108">The ServiceTimeoutsBehavior class has the following property:</span></span>  
  
### <a name="transactiontimeout"></a><span data-ttu-id="b0d9e-109">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="b0d9e-109">TransactionTimeout</span></span>  
 <span data-ttu-id="b0d9e-110">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="b0d9e-110">Data type: datetime</span></span>  
  
 <span data-ttu-id="b0d9e-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="b0d9e-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b0d9e-112">Période pendant laquelle une transaction doit s'effectuer.</span><span class="sxs-lookup"><span data-stu-id="b0d9e-112">The period within which a transaction must complete.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b0d9e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0d9e-113">Requirements</span></span>  
  
|<span data-ttu-id="b0d9e-114">MOF</span><span class="sxs-lookup"><span data-stu-id="b0d9e-114">MOF</span></span>|<span data-ttu-id="b0d9e-115">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="b0d9e-115">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="b0d9e-116">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b0d9e-116">Namespace</span></span>|<span data-ttu-id="b0d9e-117">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="b0d9e-117">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b0d9e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0d9e-118">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceTimeoutsElement>
