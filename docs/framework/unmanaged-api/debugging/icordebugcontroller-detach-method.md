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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59151799"
---
# <a name="icordebugcontrollerdetach-method"></a><span data-ttu-id="f107d-102">ICorDebugController::Detach, méthode</span><span class="sxs-lookup"><span data-stu-id="f107d-102">ICorDebugController::Detach Method</span></span>
<span data-ttu-id="f107d-103">Détache le débogueur du processus ou domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="f107d-103">Detaches the debugger from the process or application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f107d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f107d-104">Syntax</span></span>  
  
```  
HRESULT Detach ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="f107d-105">Notes</span><span class="sxs-lookup"><span data-stu-id="f107d-105">Remarks</span></span>  
 <span data-ttu-id="f107d-106">Le processus ou domaine d’application exécution poursuit normalement, mais l’objet « ICorDebugProcess » ou « ICorDebugAppDomain » n’est plus valide et aucun autre rappel ne se produit.</span><span class="sxs-lookup"><span data-stu-id="f107d-106">The process or application domain continues execution normally, but the "ICorDebugProcess" or "ICorDebugAppDomain" object is no longer valid and no further callbacks will occur.</span></span>  
  
 <span data-ttu-id="f107d-107">Dans le .NET Framework version 2.0, si le débogage non managé est activé, cette méthode échoue en raison des limitations du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f107d-107">In the .NET Framework version 2.0, if unmanaged debugging is enabled, this method will fail due to operating system limitations.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f107d-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f107d-108">Requirements</span></span>  
 <span data-ttu-id="f107d-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f107d-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f107d-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f107d-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f107d-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f107d-111">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="f107d-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="f107d-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="f107d-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f107d-113">See also</span></span>
