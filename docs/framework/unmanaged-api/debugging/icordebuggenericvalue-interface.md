---
title: ICorDebugGenericValue, Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugGenericValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGenericValue
helpviewer_keywords:
- ICorDebugGenericValue interface [.NET Framework debugging]
ms.assetid: bc14f408-b359-4c8c-ade2-888ccdf7261b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ce4c1b73ab806958627bb68bfdcfcae890bc5e67
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54709830"
---
# <a name="icordebuggenericvalue-interface1"></a><span data-ttu-id="658e1-102">ICorDebugGenericValue, Interface1</span><span class="sxs-lookup"><span data-stu-id="658e1-102">ICorDebugGenericValue Interface1</span></span>
<span data-ttu-id="658e1-103">Une sous-classe de « ICorDebugValue » qui s’applique à toutes les valeurs.</span><span class="sxs-lookup"><span data-stu-id="658e1-103">A subclass of "ICorDebugValue" that applies to all values.</span></span> <span data-ttu-id="658e1-104">Cette interface fournit les méthodes Get et Set pour la valeur.</span><span class="sxs-lookup"><span data-stu-id="658e1-104">This interface provides Get and Set methods for the value.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="658e1-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="658e1-105">Methods</span></span>  
  
|<span data-ttu-id="658e1-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="658e1-106">Method</span></span>|<span data-ttu-id="658e1-107">Description</span><span class="sxs-lookup"><span data-stu-id="658e1-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="658e1-108">GetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="658e1-108">GetValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuggenericvalue-getvalue-method.md)|<span data-ttu-id="658e1-109">Copie la valeur dans la mémoire tampon spécifiée.</span><span class="sxs-lookup"><span data-stu-id="658e1-109">Copies the value into the specified buffer.</span></span>|  
|[<span data-ttu-id="658e1-110">SetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="658e1-110">SetValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuggenericvalue-setvalue-method.md)|<span data-ttu-id="658e1-111">Copie une nouvelle valeur à partir de la mémoire tampon spécifiée.</span><span class="sxs-lookup"><span data-stu-id="658e1-111">Copies a new value from the specified buffer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="658e1-112">Notes</span><span class="sxs-lookup"><span data-stu-id="658e1-112">Remarks</span></span>  
 <span data-ttu-id="658e1-113">`ICorDebugGenericValue` est une sous-interface, car il est non accessibles à distance.</span><span class="sxs-lookup"><span data-stu-id="658e1-113">`ICorDebugGenericValue` is a sub-interface because it is non-remotable.</span></span>  
  
 <span data-ttu-id="658e1-114">Pour les types référence, la valeur est la référence plutôt que le contenu de la référence.</span><span class="sxs-lookup"><span data-stu-id="658e1-114">For reference types, the value is the reference rather than the contents of the reference.</span></span>  
  
 <span data-ttu-id="658e1-115">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="658e1-115">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="658e1-116">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="658e1-116">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="658e1-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="658e1-117">Requirements</span></span>  
 <span data-ttu-id="658e1-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="658e1-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="658e1-119">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="658e1-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="658e1-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="658e1-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="658e1-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="658e1-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="658e1-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="658e1-122">See also</span></span>

- [<span data-ttu-id="658e1-123">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="658e1-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
