---
title: ICorDebugVariableHome::GetLocationType (méthode)
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetLocationType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetLocationType
helpviewer_keywords:
- ICorDebugVariableHome::GetLocationType method [.NET Framework debugging]
- GetLocationType method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: 88027c55-8ec6-4f1e-a55b-7eefdbbc3515
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c04fa944f2a3da9b6548ada36443d5dda4725f21
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33421127"
---
# <a name="icordebugvariablehomegetlocationtype-method"></a><span data-ttu-id="9fb53-102">ICorDebugVariableHome::GetLocationType (méthode)</span><span class="sxs-lookup"><span data-stu-id="9fb53-102">ICorDebugVariableHome::GetLocationType Method</span></span>
<span data-ttu-id="9fb53-103">Obtient le type d’emplacement native de la variable.</span><span class="sxs-lookup"><span data-stu-id="9fb53-103">Gets the type of the variable's native location.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9fb53-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fb53-104">Syntax</span></span>  
  
```  
HRESULT GetLocationType(  
    [out] VariableLocationType *pLocationType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9fb53-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9fb53-105">Parameters</span></span>  
 `pLocationType`  
 <span data-ttu-id="9fb53-106">[out] Pointeur vers le type d’emplacement native de la variable.</span><span class="sxs-lookup"><span data-stu-id="9fb53-106">[out] A pointer to the type of the variable's native location.</span></span>  <span data-ttu-id="9fb53-107">Consultez le [VariableLocationType](../../../../docs/framework/unmanaged-api/debugging/variablelocationtype-enumeration.md) énumération pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9fb53-107">See the [VariableLocationType](../../../../docs/framework/unmanaged-api/debugging/variablelocationtype-enumeration.md) enumeration for more information.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9fb53-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9fb53-108">Requirements</span></span>  
 <span data-ttu-id="9fb53-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9fb53-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9fb53-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9fb53-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9fb53-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9fb53-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9fb53-112">**Versions du .NET framework :** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9fb53-112">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9fb53-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fb53-113">See Also</span></span>  
 [<span data-ttu-id="9fb53-114">ICorDebugVariableHome, interface</span><span class="sxs-lookup"><span data-stu-id="9fb53-114">ICorDebugVariableHome Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md)  
 [<span data-ttu-id="9fb53-115">VariableLocationType, énumération</span><span class="sxs-lookup"><span data-stu-id="9fb53-115">VariableLocationType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/variablelocationtype-enumeration.md)
