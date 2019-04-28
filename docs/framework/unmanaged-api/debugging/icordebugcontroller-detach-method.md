---
title: ICorDebugController::Detach, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugController.Detach
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::Detach
helpviewer_keywords:
- Detach method, ICorDebugController interface [.NET Framework debugging]
- ICorDebugController::Detach method [.NET Framework debugging]
ms.assetid: 06fae364-f2c6-4a50-aa7e-3da9f2684dc3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 85a9bde77f7c393756ec1d3e7d30b96392aa6a94
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61749629"
---
# <a name="icordebugcontrollerdetach-method"></a><span data-ttu-id="1217a-102">ICorDebugController::Detach, méthode</span><span class="sxs-lookup"><span data-stu-id="1217a-102">ICorDebugController::Detach Method</span></span>
<span data-ttu-id="1217a-103">Détache le débogueur du processus ou domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="1217a-103">Detaches the debugger from the process or application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1217a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1217a-104">Syntax</span></span>  
  
```  
HRESULT Detach ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="1217a-105">Notes</span><span class="sxs-lookup"><span data-stu-id="1217a-105">Remarks</span></span>  
 <span data-ttu-id="1217a-106">Le processus ou domaine d’application exécution poursuit normalement, mais l’objet « ICorDebugProcess » ou « ICorDebugAppDomain » n’est plus valide et aucun autre rappel ne se produit.</span><span class="sxs-lookup"><span data-stu-id="1217a-106">The process or application domain continues execution normally, but the "ICorDebugProcess" or "ICorDebugAppDomain" object is no longer valid and no further callbacks will occur.</span></span>  
  
 <span data-ttu-id="1217a-107">Dans le .NET Framework version 2.0, si le débogage non managé est activé, cette méthode échoue en raison des limitations du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1217a-107">In the .NET Framework version 2.0, if unmanaged debugging is enabled, this method will fail due to operating system limitations.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1217a-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1217a-108">Requirements</span></span>  
 <span data-ttu-id="1217a-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1217a-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1217a-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1217a-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1217a-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1217a-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1217a-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1217a-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1217a-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1217a-113">See also</span></span>
