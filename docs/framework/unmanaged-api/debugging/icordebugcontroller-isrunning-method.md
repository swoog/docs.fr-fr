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
ms.openlocfilehash: cd54792e37523ea5bf0c2e7a4082ee00c30d00ea
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54496294"
---
# <a name="icordebugcontrollerisrunning-method"></a><span data-ttu-id="86dbb-102">ICorDebugController::IsRunning, méthode</span><span class="sxs-lookup"><span data-stu-id="86dbb-102">ICorDebugController::IsRunning Method</span></span>
<span data-ttu-id="86dbb-103">Obtient une valeur qui indique si les threads dans le processus en cours d’exécution librement.</span><span class="sxs-lookup"><span data-stu-id="86dbb-103">Gets a value that indicates whether the threads in the process are currently running freely.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86dbb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86dbb-104">Syntax</span></span>  
  
```  
HRESULT IsRunning (  
    [out] BOOL *pbRunning  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="86dbb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86dbb-105">Parameters</span></span>  
 `pbRunning`  
 <span data-ttu-id="86dbb-106">[out] Un pointeur vers une valeur qui est `true` si les threads dans le processus sont en cours d’exécution librement ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="86dbb-106">[out] A pointer to a value that is `true` if the threads in the process are running freely; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="86dbb-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="86dbb-107">Requirements</span></span>  
 <span data-ttu-id="86dbb-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="86dbb-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="86dbb-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="86dbb-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="86dbb-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="86dbb-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="86dbb-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="86dbb-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86dbb-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86dbb-112">See also</span></span>

