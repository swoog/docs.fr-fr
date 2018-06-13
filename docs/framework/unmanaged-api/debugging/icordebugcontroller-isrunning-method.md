---
title: ICorDebugController::IsRunning, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugController.IsRunning
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::IsRunning
helpviewer_keywords:
- IsRunning method [.NET Framework debugging]
- ICorDebugController::IsRunning method [.NET Framework debugging]
ms.assetid: b33ff059-40c4-4dfe-9cb2-21bfed2de0b0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4605b893169ccfc592aae0d07dc032f455314cc5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33412730"
---
# <a name="icordebugcontrollerisrunning-method"></a><span data-ttu-id="3452d-102">ICorDebugController::IsRunning, méthode</span><span class="sxs-lookup"><span data-stu-id="3452d-102">ICorDebugController::IsRunning Method</span></span>
<span data-ttu-id="3452d-103">Obtient une valeur qui indique si les threads dans le processus en cours d’exécution librement.</span><span class="sxs-lookup"><span data-stu-id="3452d-103">Gets a value that indicates whether the threads in the process are currently running freely.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3452d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3452d-104">Syntax</span></span>  
  
```  
HRESULT IsRunning (  
    [out] BOOL *pbRunning  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3452d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3452d-105">Parameters</span></span>  
 `pbRunning`  
 <span data-ttu-id="3452d-106">[out] Un pointeur vers une valeur qui est `true` si les threads dans le processus sont exécutent librement ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="3452d-106">[out] A pointer to a value that is `true` if the threads in the process are running freely; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3452d-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3452d-107">Requirements</span></span>  
 <span data-ttu-id="3452d-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3452d-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3452d-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3452d-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3452d-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3452d-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3452d-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3452d-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3452d-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3452d-112">See Also</span></span>  
 
