---
title: ICorDebugFunction2, Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugFunction2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction2
helpviewer_keywords:
- ICorDebugFunction2 interface [.NET Framework debugging]
ms.assetid: 2b936bef-9b75-48bf-859f-42e419c65f1c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 190e2323fb07dbca6e156d7a24397997e54b6da9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54540791"
---
# <a name="icordebugfunction2-interface1"></a><span data-ttu-id="f26db-102">ICorDebugFunction2, Interface1</span><span class="sxs-lookup"><span data-stu-id="f26db-102">ICorDebugFunction2 Interface1</span></span>
<span data-ttu-id="f26db-103">Étend logiquement l’interface ICorDebugFunction pour prendre en charge pour le débogage uniquement mon Code pas à pas, qui ignore le code non-utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f26db-103">Logically extends the ICorDebugFunction interface to provide support for Just My Code step-through debugging, which skips non-user code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f26db-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f26db-104">Methods</span></span>  
  
|<span data-ttu-id="f26db-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="f26db-105">Method</span></span>|<span data-ttu-id="f26db-106">Description</span><span class="sxs-lookup"><span data-stu-id="f26db-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f26db-107">EnumerateNativeCode, méthode</span><span class="sxs-lookup"><span data-stu-id="f26db-107">EnumerateNativeCode Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction2-enumeratenativecode-method.md)|<span data-ttu-id="f26db-108">(Pas encore implémenté.) Obtient un pointeur d’interface vers un ICorDebugCodeEnum qui contient les instructions de code natif dans la fonction référencée par cet objet ICorDebugFunction2.</span><span class="sxs-lookup"><span data-stu-id="f26db-108">(Not yet implemented.) Gets an interface pointer to an ICorDebugCodeEnum that contains the native code statements in the function referenced by this ICorDebugFunction2 object.</span></span>|  
|[<span data-ttu-id="f26db-109">GetJMCStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="f26db-109">GetJMCStatus Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction2-getjmcstatus-method.md)|<span data-ttu-id="f26db-110">Obtient une valeur qui indique si cette fonction est marquée comme code utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f26db-110">Gets a value that indicates whether this function is marked as user code.</span></span>|  
|[<span data-ttu-id="f26db-111">GetVersionNumber, méthode</span><span class="sxs-lookup"><span data-stu-id="f26db-111">GetVersionNumber Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction2-getversionnumber-method.md)|<span data-ttu-id="f26db-112">Obtient la version Modifier & Continuer de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f26db-112">Gets the Edit and Continue version of this function.</span></span>|  
|[<span data-ttu-id="f26db-113">SetJMCStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="f26db-113">SetJMCStatus Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction2-setjmcstatus-method.md)|<span data-ttu-id="f26db-114">Marque cette fonction pour uniquement mon Code pas à pas détaillé.</span><span class="sxs-lookup"><span data-stu-id="f26db-114">Marks this function for Just My Code stepping.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f26db-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f26db-115">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f26db-116">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="f26db-116">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f26db-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f26db-117">Requirements</span></span>  
 <span data-ttu-id="f26db-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f26db-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f26db-119">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f26db-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f26db-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f26db-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f26db-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f26db-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f26db-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f26db-122">See also</span></span>
- [<span data-ttu-id="f26db-123">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="f26db-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
