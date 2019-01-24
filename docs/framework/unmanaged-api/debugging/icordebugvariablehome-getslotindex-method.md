---
title: ICorDebugVariableHome::GetSlotIndex (méthode)
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetSlotIndex
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetSlotIndex
helpviewer_keywords:
- ICorDebugVariableHome::GetSlotIndex method [.NET Framework debugging]
- GetSlotIndex method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: 966da50d-5665-4fff-bf7b-1c72bbadd9a4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3534160e14c46bc3f8f5da81c4c14a3191a6238b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54553190"
---
# <a name="icordebugvariablehomegetslotindex-method"></a><span data-ttu-id="ec8e2-102">ICorDebugVariableHome::GetSlotIndex (méthode)</span><span class="sxs-lookup"><span data-stu-id="ec8e2-102">ICorDebugVariableHome::GetSlotIndex Method</span></span>
<span data-ttu-id="ec8e2-103">Obtient l’index emplacement managé d’une variable locale.</span><span class="sxs-lookup"><span data-stu-id="ec8e2-103">Gets the managed slot-index of a local variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ec8e2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec8e2-104">Syntax</span></span>  
  
```  
HRESULT GetSlotIndex(  
    [out] ULONG32 *pSlotIndex  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ec8e2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec8e2-105">Parameters</span></span>  
 `pSlotIndex`  
 <span data-ttu-id="ec8e2-106">[out] Pointeur vers l’index d’emplacement d’une variable locale.</span><span class="sxs-lookup"><span data-stu-id="ec8e2-106">[out] A pointer to the slot-index of a local variable.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ec8e2-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ec8e2-107">Return Value</span></span>  
 <span data-ttu-id="ec8e2-108">La méthode retourne les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ec8e2-108">The method returns the following values.</span></span>  
  
|<span data-ttu-id="ec8e2-109">Value</span><span class="sxs-lookup"><span data-stu-id="ec8e2-109">Value</span></span>|<span data-ttu-id="ec8e2-110">Description</span><span class="sxs-lookup"><span data-stu-id="ec8e2-110">Description</span></span>|  
|-----------|-----------------|  
|`S_OK`|<span data-ttu-id="ec8e2-111">L’appel de méthode a retourné une valeur d’index de l’emplacement dans `pSlotIndex`.</span><span class="sxs-lookup"><span data-stu-id="ec8e2-111">The method call returned a slot-index value in `pSlotIndex`.</span></span>|  
|`E_FAIL`|<span data-ttu-id="ec8e2-112">Actuel [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instance représente un argument de fonction.</span><span class="sxs-lookup"><span data-stu-id="ec8e2-112">The current [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instance represents a function argument.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ec8e2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ec8e2-113">Remarks</span></span>  
 <span data-ttu-id="ec8e2-114">L’index de l’emplacement peut être utilisé pour récupérer les métadonnées pour cette variable locale.</span><span class="sxs-lookup"><span data-stu-id="ec8e2-114">The slot-index can be used to retrieve the metadata for this local variable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ec8e2-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ec8e2-115">Requirements</span></span>  
 <span data-ttu-id="ec8e2-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ec8e2-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ec8e2-117">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ec8e2-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ec8e2-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ec8e2-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ec8e2-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ec8e2-119">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ec8e2-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec8e2-120">See also</span></span>
- [<span data-ttu-id="ec8e2-121">ICorDebugVariableHome, interface</span><span class="sxs-lookup"><span data-stu-id="ec8e2-121">ICorDebugVariableHome Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md)
