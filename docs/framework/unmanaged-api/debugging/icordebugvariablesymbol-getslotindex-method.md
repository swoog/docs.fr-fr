---
title: Méthode ICorDebugVariableSymbol::GetSlotIndex
ms.date: 03/30/2017
ms.assetid: 09c19f5f-afc4-4e0c-bffe-cd7147bc7a43
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: affe67006c9e37d55b0f9d107c92441da44c9ab8
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59138786"
---
# <a name="icordebugvariablesymbolgetslotindex-method"></a><span data-ttu-id="ec1c4-102">Méthode ICorDebugVariableSymbol::GetSlotIndex</span><span class="sxs-lookup"><span data-stu-id="ec1c4-102">ICorDebugVariableSymbol::GetSlotIndex Method</span></span>
<span data-ttu-id="ec1c4-103">Obtient l'index d'emplacement géré d'une variable locale.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-103">Gets the managed slot index of a local variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ec1c4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec1c4-104">Syntax</span></span>  
  
```  
HRESULT GetSlotIndex(  
   [out] ULONG32 *pSlotIndex  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ec1c4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec1c4-105">Parameters</span></span>  
 `pSlotIndex`  
 <span data-ttu-id="ec1c4-106">[out] Pointeur vers l'index d'emplacement de la variable locale.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-106">[out] A pointer to the local variable's slot index.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ec1c4-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ec1c4-107">Return Value</span></span>  
 `S_OK` <span data-ttu-id="ec1c4-108">en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-108">if successful.</span></span> `E_FAIL` <span data-ttu-id="ec1c4-109">Si la variable est un argument de fonction.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-109">if the variable is a function argument.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ec1c4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ec1c4-110">Remarks</span></span>  
 <span data-ttu-id="ec1c4-111">L'index emplacement managé d'une variable locale peut être utilisé pour récupérer des informations de métadonnées de la variable.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-111">The managed slot index of a local variable can be used to retrieve the variable's metadata information</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ec1c4-112">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ec1c4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec1c4-113">Requirements</span></span>  
 <span data-ttu-id="ec1c4-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ec1c4-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ec1c4-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ec1c4-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ec1c4-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ec1c4-116">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="ec1c4-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="ec1c4-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="ec1c4-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec1c4-118">See also</span></span>

- [<span data-ttu-id="ec1c4-119">ICorDebugVariableSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="ec1c4-119">ICorDebugVariableSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="ec1c4-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="ec1c4-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
