---
title: ICorDebugVariableHome::GetOffset (méthode)
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetOffset
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetOffset
helpviewer_keywords:
- ICorDebugVariableHome::GetOffset method [.NET Framework debugging]
- GetOffset method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: f025c2e5-3f6c-4be8-9ffe-c8b214617dfe
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9a2ea7273fec62654c168d6786d3644b184ff7f3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33419567"
---
# <a name="icordebugvariablehomegetoffset-method"></a><span data-ttu-id="9ceb2-102">ICorDebugVariableHome::GetOffset (méthode)</span><span class="sxs-lookup"><span data-stu-id="9ceb2-102">ICorDebugVariableHome::GetOffset Method</span></span>
<span data-ttu-id="9ceb2-103">Obtient le décalage à partir du Registre de base d’une variable.</span><span class="sxs-lookup"><span data-stu-id="9ceb2-103">Gets the offset from the base register for a variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ceb2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ceb2-104">Syntax</span></span>  
  
```  
HRESULT GetOffset(  
    [out] LONG *pOffset  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9ceb2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ceb2-105">Parameters</span></span>  
 `pOffset`  
 <span data-ttu-id="9ceb2-106">[out] Le décalage à partir du Registre de base.</span><span class="sxs-lookup"><span data-stu-id="9ceb2-106">[out] The offset from the base register.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9ceb2-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9ceb2-107">Return Value</span></span>  
 <span data-ttu-id="9ceb2-108">La méthode retourne les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="9ceb2-108">The method returns the following values:</span></span>  
  
|<span data-ttu-id="9ceb2-109">Value</span><span class="sxs-lookup"><span data-stu-id="9ceb2-109">Value</span></span>|<span data-ttu-id="9ceb2-110">Description</span><span class="sxs-lookup"><span data-stu-id="9ceb2-110">Description</span></span>|  
|-----------|-----------------|  
|`S_OK`|<span data-ttu-id="9ceb2-111">La variable est dans un emplacement de mémoire relative au Registre.</span><span class="sxs-lookup"><span data-stu-id="9ceb2-111">The variable is in a register-relative memory location.</span></span>|  
|`E_FAIL`|<span data-ttu-id="9ceb2-112">La variable n’est pas dans un emplacement de mémoire relative au Registre.</span><span class="sxs-lookup"><span data-stu-id="9ceb2-112">The variable is not in a register-relative memory location.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9ceb2-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9ceb2-113">Requirements</span></span>  
 <span data-ttu-id="9ceb2-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9ceb2-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ceb2-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9ceb2-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9ceb2-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9ceb2-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9ceb2-117">**Versions du .NET framework :** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ceb2-117">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ceb2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ceb2-118">See Also</span></span>  
 [<span data-ttu-id="9ceb2-119">ICorDebugVariableHome, interface</span><span class="sxs-lookup"><span data-stu-id="9ceb2-119">ICorDebugVariableHome Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md)
