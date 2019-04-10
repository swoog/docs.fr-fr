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
ms.openlocfilehash: a5eae9e14bcd0ca430f03a873818246896438463
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59227091"
---
# <a name="icordebugcontrollerisrunning-method"></a><span data-ttu-id="ce092-102">ICorDebugController::IsRunning, méthode</span><span class="sxs-lookup"><span data-stu-id="ce092-102">ICorDebugController::IsRunning Method</span></span>
<span data-ttu-id="ce092-103">Obtient une valeur qui indique si les threads dans le processus en cours d’exécution librement.</span><span class="sxs-lookup"><span data-stu-id="ce092-103">Gets a value that indicates whether the threads in the process are currently running freely.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ce092-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce092-104">Syntax</span></span>  
  
```  
HRESULT IsRunning (  
    [out] BOOL *pbRunning  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ce092-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce092-105">Parameters</span></span>  
 `pbRunning`  
 <span data-ttu-id="ce092-106">[out] Un pointeur vers une valeur qui est `true` si les threads dans le processus sont en cours d’exécution librement ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="ce092-106">[out] A pointer to a value that is `true` if the threads in the process are running freely; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ce092-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce092-107">Requirements</span></span>  
 <span data-ttu-id="ce092-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ce092-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ce092-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ce092-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ce092-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ce092-110">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="ce092-111">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="ce092-111">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="ce092-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce092-112">See also</span></span>
