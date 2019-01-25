---
title: ICorDebugProcess5::GetTypeLayout, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5.GetTypeLayout
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::GetTypeLayout
helpviewer_keywords:
- ICorDebugProcess5::GetTypeLayout method [.NET Framework debugging]
- GetTypeLayout method, ICorDebugProcess5 interface [.NET Framework debugging]
ms.assetid: bd62f5d1-e874-41f1-81e5-a29a7572c15d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f12398a2423e7e0081556dbdb279e4a2f23c3af7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54723418"
---
# <a name="icordebugprocess5gettypelayout-method"></a><span data-ttu-id="4bae4-102">ICorDebugProcess5::GetTypeLayout, méthode</span><span class="sxs-lookup"><span data-stu-id="4bae4-102">ICorDebugProcess5::GetTypeLayout Method</span></span>
<span data-ttu-id="4bae4-103">Obtient des informations sur la disposition d’un objet en mémoire en fonction de son identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="4bae4-103">Gets information about the layout of an object in memory based on its type identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4bae4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bae4-104">Syntax</span></span>  
  
```  
HRESULT GetTypeLayout(    [in] COR_TYPEID id,     [out] COR_TYPE_LAYOUT *pLayout);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4bae4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4bae4-105">Parameters</span></span>  
 `id`  
 <span data-ttu-id="4bae4-106">[in] Un [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) jeton qui spécifie le type dont la disposition est souhaitée.</span><span class="sxs-lookup"><span data-stu-id="4bae4-106">[in] A [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) token that specifies the type whose layout is desired.</span></span>  
  
 `pLayout`  
 <span data-ttu-id="4bae4-107">[out] Un pointeur vers un [COR_TYPE_LAYOUT](../../../../docs/framework/unmanaged-api/debugging/cor-type-layout-structure.md) structure qui contient des informations sur la disposition de l’objet en mémoire.</span><span class="sxs-lookup"><span data-stu-id="4bae4-107">[out] A pointer to a [COR_TYPE_LAYOUT](../../../../docs/framework/unmanaged-api/debugging/cor-type-layout-structure.md) structure that contains information about the layout of the object in memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4bae4-108">Notes</span><span class="sxs-lookup"><span data-stu-id="4bae4-108">Remarks</span></span>  
 <span data-ttu-id="4bae4-109">Le `ICorDebugProcess5::GetTypeLayout` méthode fournit des informations sur un objet basé sur son [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md), qui est retourné par un nombre d’autres [ICorDebugProcess5](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-interface.md) méthodes.</span><span class="sxs-lookup"><span data-stu-id="4bae4-109">The `ICorDebugProcess5::GetTypeLayout` method provides information about an object based on its [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md), which is returned by a number of other [ICorDebugProcess5](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-interface.md) methods.</span></span> <span data-ttu-id="4bae4-110">Les informations sont fournies par un [COR_TYPE_LAYOUT](../../../../docs/framework/unmanaged-api/debugging/cor-type-layout-structure.md) structure est remplie par la méthode.</span><span class="sxs-lookup"><span data-stu-id="4bae4-110">The information is provided by a [COR_TYPE_LAYOUT](../../../../docs/framework/unmanaged-api/debugging/cor-type-layout-structure.md) structure that is populated by the method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4bae4-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4bae4-111">Requirements</span></span>  
 <span data-ttu-id="4bae4-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4bae4-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4bae4-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4bae4-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4bae4-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4bae4-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4bae4-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4bae4-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4bae4-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bae4-116">See also</span></span>
- [<span data-ttu-id="4bae4-117">COR_TYPE_LAYOUT, structure</span><span class="sxs-lookup"><span data-stu-id="4bae4-117">COR_TYPE_LAYOUT Structure</span></span>](../../../../docs/framework/unmanaged-api/debugging/cor-type-layout-structure.md)
- [<span data-ttu-id="4bae4-118">ICorDebugProcess5, interface</span><span class="sxs-lookup"><span data-stu-id="4bae4-118">ICorDebugProcess5 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-interface.md)
- [<span data-ttu-id="4bae4-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="4bae4-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
