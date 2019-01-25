---
title: ICorDebugGuidToTypeEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugGuidToTypeEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGuidToTypeEnum::Next
helpviewer_keywords:
- ICorDebugGuidToTypeEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugGuidToTypeEnum interface [.NET Framework debugging]
ms.assetid: c9937666-8e18-484d-9fe0-b9ac95199530
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4b6e129b4ea5e6042a4ce41ed20b76f4a0e75fd6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54676729"
---
# <a name="icordebugguidtotypeenumnext-method"></a><span data-ttu-id="9c03b-102">ICorDebugGuidToTypeEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="9c03b-102">ICorDebugGuidToTypeEnum::Next Method</span></span>
<span data-ttu-id="9c03b-103">Obtient le nombre spécifié de [CorDebugGuidToTypeMapping](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md) instances qui mappent des GUID vers le type d’informations.</span><span class="sxs-lookup"><span data-stu-id="9c03b-103">Gets the specified number of [CorDebugGuidToTypeMapping](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md) instances that map GUIDs to type information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9c03b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c03b-104">Syntax</span></span>  
  
```  
HRESULT Next(  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched] CorDebugGuidToTypeMapping values[  ],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9c03b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c03b-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="9c03b-106">[in] Le nombre d’objets de mappage de type-GUID à récupérer.</span><span class="sxs-lookup"><span data-stu-id="9c03b-106">[in] The number of GUID-to-type mapping objects to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="9c03b-107">[out] Un tableau de pointeurs, chacun d’eux pointe vers un [CorDebugGuidToTypeMapping](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md) objet qui mappe un [!INCLUDE[wrt](../../../../includes/wrt-md.md)] GUID à son objet ICorDebugType correspondant.</span><span class="sxs-lookup"><span data-stu-id="9c03b-107">[out] An array of pointers, each of which points to a [CorDebugGuidToTypeMapping](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md) object that maps a [!INCLUDE[wrt](../../../../includes/wrt-md.md)] GUID to its corresponding ICorDebugType object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="9c03b-108">[out] Un pointeur vers le nombre de [CorDebugGuidToTypeMapping](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md) réellement retournés dans des objets `values`.</span><span class="sxs-lookup"><span data-stu-id="9c03b-108">[out] A pointer to the number of [CorDebugGuidToTypeMapping](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md) objects actually returned in `values`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9c03b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9c03b-109">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9c03b-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9c03b-110">Requirements</span></span>  
 <span data-ttu-id="9c03b-111">**Plateformes :** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9c03b-111">**Platforms:** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]</span></span>  
  
 <span data-ttu-id="9c03b-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9c03b-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9c03b-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9c03b-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9c03b-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9c03b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c03b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c03b-115">See also</span></span>
- [<span data-ttu-id="9c03b-116">ICorDebugGuidToTypeEnum, interface</span><span class="sxs-lookup"><span data-stu-id="9c03b-116">ICorDebugGuidToTypeEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugguidtotypeenum-interface.md)
- [<span data-ttu-id="9c03b-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="9c03b-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
