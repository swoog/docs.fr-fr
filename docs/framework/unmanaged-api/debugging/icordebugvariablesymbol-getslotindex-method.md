---
title: Méthode ICorDebugVariableSymbol::GetSlotIndex
ms.date: 03/30/2017
ms.assetid: 09c19f5f-afc4-4e0c-bffe-cd7147bc7a43
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: affe67006c9e37d55b0f9d107c92441da44c9ab8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59138786"
---
# <a name="icordebugvariablesymbolgetslotindex-method"></a><span data-ttu-id="90d76-102">Méthode ICorDebugVariableSymbol::GetSlotIndex</span><span class="sxs-lookup"><span data-stu-id="90d76-102">ICorDebugVariableSymbol::GetSlotIndex Method</span></span>
<span data-ttu-id="90d76-103">Obtient l'index d'emplacement géré d'une variable locale.</span><span class="sxs-lookup"><span data-stu-id="90d76-103">Gets the managed slot index of a local variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="90d76-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90d76-104">Syntax</span></span>  
  
```  
HRESULT GetSlotIndex(  
   [out] ULONG32 *pSlotIndex  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="90d76-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90d76-105">Parameters</span></span>  
 `pSlotIndex`  
 <span data-ttu-id="90d76-106">[out] Pointeur vers l'index d'emplacement de la variable locale.</span><span class="sxs-lookup"><span data-stu-id="90d76-106">[out] A pointer to the local variable's slot index.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="90d76-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="90d76-107">Return Value</span></span>  
 <span data-ttu-id="90d76-108">`S_OK` si l'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="90d76-108">`S_OK` if successful.</span></span> <span data-ttu-id="90d76-109">`E_FAIL` si la variable est un argument de fonction.</span><span class="sxs-lookup"><span data-stu-id="90d76-109">`E_FAIL` if the variable is a function argument.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="90d76-110">Notes</span><span class="sxs-lookup"><span data-stu-id="90d76-110">Remarks</span></span>  
 <span data-ttu-id="90d76-111">L'index emplacement managé d'une variable locale peut être utilisé pour récupérer des informations de métadonnées de la variable.</span><span class="sxs-lookup"><span data-stu-id="90d76-111">The managed slot index of a local variable can be used to retrieve the variable's metadata information</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="90d76-112">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="90d76-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="90d76-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90d76-113">Requirements</span></span>  
 <span data-ttu-id="90d76-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="90d76-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="90d76-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="90d76-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="90d76-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="90d76-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="90d76-117">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="90d76-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="90d76-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90d76-118">See also</span></span>

- [<span data-ttu-id="90d76-119">ICorDebugVariableSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="90d76-119">ICorDebugVariableSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="90d76-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="90d76-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
