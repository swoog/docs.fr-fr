---
title: IReferenceAppId, interface
ms.date: 03/30/2017
api_name:
- IReferenceAppId
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IReferenceAppId
helpviewer_keywords:
- IReferenceAppId interface [.NET Framework fusion]
ms.assetid: 8eb9e565-f358-43ce-900e-a8f8a5aa6cfb
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2289a9a75311c9642a764844ee466adcc5838655
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54744347"
---
# <a name="ireferenceappid-interface"></a><span data-ttu-id="e58e0-102">IReferenceAppId, interface</span><span class="sxs-lookup"><span data-stu-id="e58e0-102">IReferenceAppId Interface</span></span>
<span data-ttu-id="e58e0-103">Représente une référence à l’identificateur unique pour l’application dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="e58e0-103">Represents a reference to the unique identifier for the application in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e58e0-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e58e0-104">Methods</span></span>  
  
|<span data-ttu-id="e58e0-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="e58e0-105">Method</span></span>|<span data-ttu-id="e58e0-106">Description</span><span class="sxs-lookup"><span data-stu-id="e58e0-106">Description</span></span>|  
|------------|-----------------|  
|`IReferenceAppId::get_CodeBase`|<span data-ttu-id="e58e0-107">Obtient un pointeur vers une représentation sous forme de chaîne de l’identificateur de code de l’application référencée par ce `IReferenceAppId`.</span><span class="sxs-lookup"><span data-stu-id="e58e0-107">Gets a pointer to a string representation of the code identifier for the application referenced by this `IReferenceAppId`.</span></span>|  
|`IReferenceAppId::put_CodeBase`|<span data-ttu-id="e58e0-108">Définit l’identificateur de code de l’application référencée par ce `IReferenceAppId`.</span><span class="sxs-lookup"><span data-stu-id="e58e0-108">Sets the code identifier for the application referenced by this `IReferenceAppId`.</span></span>|  
|`IReferenceAppId::EnumAppPath`|<span data-ttu-id="e58e0-109">Obtient un pointeur d’interface vers un `IEnumReferenceIdentity` instance contenant le `IReferenceIdentity` instances qui représentent les membres de ce `IReferenceAppId`.</span><span class="sxs-lookup"><span data-stu-id="e58e0-109">Gets an interface pointer to an `IEnumReferenceIdentity` instance containing the `IReferenceIdentity` instances that represent members of this `IReferenceAppId`.</span></span>|  
|`IReferenceAppId::get_SubscriptionId`|<span data-ttu-id="e58e0-110">Obtient un pointeur vers une représentation sous forme de chaîne de l’identificateur de jeton pour un abonnement à ce `IReferenceAppId`.</span><span class="sxs-lookup"><span data-stu-id="e58e0-110">Gets a pointer to a string representation of the token identifier for a subscription to this `IReferenceAppId`.</span></span>|  
|`IReferenceAppId::put_SubscriptionId`|<span data-ttu-id="e58e0-111">Définit l’identificateur de jeton pour un abonnement à ce `IReferenceAppId` à la valeur de chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e58e0-111">Sets the token identifier for a subscription to this `IReferenceAppId` to the specified string value.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e58e0-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e58e0-112">Requirements</span></span>  
 <span data-ttu-id="e58e0-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e58e0-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e58e0-114">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="e58e0-114">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="e58e0-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e58e0-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e58e0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e58e0-116">See also</span></span>
- [<span data-ttu-id="e58e0-117">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="e58e0-117">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [<span data-ttu-id="e58e0-118">IEnumReferenceIdentity, interface</span><span class="sxs-lookup"><span data-stu-id="e58e0-118">IEnumReferenceIdentity Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/ienumreferenceidentity-interface.md)
- [<span data-ttu-id="e58e0-119">IReferenceIdentity, interface</span><span class="sxs-lookup"><span data-stu-id="e58e0-119">IReferenceIdentity Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/ireferenceidentity-interface.md)
