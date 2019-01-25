---
title: Méthode ICorDebugVariableSymbol::GetSlotIndex
ms.date: 03/30/2017
ms.assetid: 09c19f5f-afc4-4e0c-bffe-cd7147bc7a43
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 09b50af49f8379539773d2000a6c1f8222fee875
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54563832"
---
# <a name="icordebugvariablesymbolgetslotindex-method"></a><span data-ttu-id="29cac-102">Méthode ICorDebugVariableSymbol::GetSlotIndex</span><span class="sxs-lookup"><span data-stu-id="29cac-102">ICorDebugVariableSymbol::GetSlotIndex Method</span></span>
<span data-ttu-id="29cac-103">Obtient l'index d'emplacement géré d'une variable locale.</span><span class="sxs-lookup"><span data-stu-id="29cac-103">Gets the managed slot index of a local variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="29cac-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29cac-104">Syntax</span></span>  
  
```  
HRESULT GetSlotIndex(  
   [out] ULONG32 *pSlotIndex  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="29cac-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29cac-105">Parameters</span></span>  
 `pSlotIndex`  
 <span data-ttu-id="29cac-106">[out] Pointeur vers l'index d'emplacement de la variable locale.</span><span class="sxs-lookup"><span data-stu-id="29cac-106">[out] A pointer to the local variable's slot index.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="29cac-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="29cac-107">Return Value</span></span>  
 <span data-ttu-id="29cac-108">`S_OK` si l'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="29cac-108">`S_OK` if successful.</span></span> <span data-ttu-id="29cac-109">`E_FAIL` si la variable est un argument de fonction.</span><span class="sxs-lookup"><span data-stu-id="29cac-109">`E_FAIL` if the variable is a function argument.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="29cac-110">Notes</span><span class="sxs-lookup"><span data-stu-id="29cac-110">Remarks</span></span>  
 <span data-ttu-id="29cac-111">L'index emplacement managé d'une variable locale peut être utilisé pour récupérer des informations de métadonnées de la variable.</span><span class="sxs-lookup"><span data-stu-id="29cac-111">The managed slot index of a local variable can be used to retrieve the variable's metadata information</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="29cac-112">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="29cac-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="29cac-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="29cac-113">Requirements</span></span>  
 <span data-ttu-id="29cac-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="29cac-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="29cac-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="29cac-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="29cac-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="29cac-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="29cac-117">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="29cac-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="29cac-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29cac-118">See also</span></span>
- [<span data-ttu-id="29cac-119">ICorDebugVariableSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="29cac-119">ICorDebugVariableSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="29cac-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="29cac-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
