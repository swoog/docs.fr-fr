---
title: ICorDebugCode::GetILToNativeMapping, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetILToNativeMapping
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetILToNativeMapping
helpviewer_keywords:
- GetILToNativeMapping method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetILToNativeMapping method [.NET Framework debugging]
ms.assetid: a8ecd8c8-9627-4356-9c6f-bd05e24637c0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c30623e53b57a78287b26d4a362793cfb32baede
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59131057"
---
# <a name="icordebugcodegetiltonativemapping-method"></a><span data-ttu-id="787b3-102">ICorDebugCode::GetILToNativeMapping, méthode</span><span class="sxs-lookup"><span data-stu-id="787b3-102">ICorDebugCode::GetILToNativeMapping Method</span></span>
<span data-ttu-id="787b3-103">Obtient un tableau d’instances de « COR_DEBUG_IL_TO_NATIVE_MAP » qui représentent les mappages à partir de Microsoft intermediate language (MSIL) aux offsets natifs.</span><span class="sxs-lookup"><span data-stu-id="787b3-103">Gets an array of "COR_DEBUG_IL_TO_NATIVE_MAP" instances that represent mappings from Microsoft intermediate language (MSIL) offsets to native offsets.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="787b3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="787b3-104">Syntax</span></span>  
  
```  
HRESULT GetILToNativeMapping (  
    [in]  ULONG32    cMap,  
    [out] ULONG32    *pcMap,  
    [out, size_is(cMap), length_is(*pcMap)]  
        COR_DEBUG_IL_TO_NATIVE_MAP map[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="787b3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="787b3-105">Parameters</span></span>  
 `cMap`  
 <span data-ttu-id="787b3-106">[in] Taille du tableau `map`.</span><span class="sxs-lookup"><span data-stu-id="787b3-106">[in] The size of the `map` array.</span></span>  
  
 `pcMap`  
 <span data-ttu-id="787b3-107">[out] Un pointeur vers le nombre réel d’éléments retournés dans le `map` tableau.</span><span class="sxs-lookup"><span data-stu-id="787b3-107">[out] A pointer to the actual number of elements returned in the `map` array.</span></span>  
  
 `map`  
 <span data-ttu-id="787b3-108">[out] Un tableau de `COR_DEBUG_IL_TO_NATIVE_MAP` structures, chacun d’eux représente un mappage d’un offset MSIL à un offset natif.</span><span class="sxs-lookup"><span data-stu-id="787b3-108">[out] An array of `COR_DEBUG_IL_TO_NATIVE_MAP` structures, each of which represents a mapping from an MSIL offset to a native offset.</span></span>  
  
 <span data-ttu-id="787b3-109">Il n’existe aucun classement dans le tableau d’éléments retournés.</span><span class="sxs-lookup"><span data-stu-id="787b3-109">There is no ordering to the array of elements returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="787b3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="787b3-110">Remarks</span></span>  
 <span data-ttu-id="787b3-111">Le `GetILToNativeMapping` méthode retourne des résultats significatifs uniquement si cette instance de « ICorDebugCode » représente le code natif qui a été compilé à partir du code MSIL juste-à-temps (JIT).</span><span class="sxs-lookup"><span data-stu-id="787b3-111">The `GetILToNativeMapping` method returns meaningful results only if this "ICorDebugCode" instance represents native code that was just-in-time (JIT) compiled from MSIL code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="787b3-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="787b3-112">Requirements</span></span>  
 <span data-ttu-id="787b3-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="787b3-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="787b3-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="787b3-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="787b3-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="787b3-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="787b3-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="787b3-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="787b3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="787b3-117">See also</span></span>

- [<span data-ttu-id="787b3-118">ICorDebugCode (Interface)</span><span class="sxs-lookup"><span data-stu-id="787b3-118">ICorDebugCode Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode-interface1.md)
