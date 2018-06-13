---
title: ICorDebug::Terminate, méthode
ms.date: 03/30/2017
api_name:
- ICorDebug.Terminate
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::Terminate
helpviewer_keywords:
- Terminate method, ICorDebug interface [.NET Framework debugging]
- ICorDebug::Terminate method [.NET Framework debugging]
ms.assetid: fffe5616-0896-4426-ab5e-21869b514883
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2c2b590e7402bf29ffeb5bd14fc383edae41a04e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33403992"
---
# <a name="icordebugterminate-method"></a><span data-ttu-id="234d6-102">ICorDebug::Terminate, méthode</span><span class="sxs-lookup"><span data-stu-id="234d6-102">ICorDebug::Terminate Method</span></span>
<span data-ttu-id="234d6-103">Met fin à la `ICorDebug` objet.</span><span class="sxs-lookup"><span data-stu-id="234d6-103">Terminates the `ICorDebug` object.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="234d6-104">`Terminate` ne doit pas être appelé qu’une [ICorDebugManagedCallback::ExitProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md) rappel a été reçu pour tous les processus en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="234d6-104">`Terminate` should not be called until an [ICorDebugManagedCallback::ExitProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md) callback has been received for all processes being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="234d6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="234d6-105">Syntax</span></span>  
  
```  
HRESULT Terminate ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="234d6-106">Notes</span><span class="sxs-lookup"><span data-stu-id="234d6-106">Remarks</span></span>  
 <span data-ttu-id="234d6-107">`Terminate` doit être appelé lorsque le `ICorDebug` objet n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="234d6-107">`Terminate` must be called when the `ICorDebug` object is no longer needed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="234d6-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="234d6-108">Requirements</span></span>  
 <span data-ttu-id="234d6-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="234d6-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="234d6-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="234d6-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="234d6-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="234d6-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="234d6-112">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="234d6-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="234d6-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="234d6-113">See Also</span></span>  
 [<span data-ttu-id="234d6-114">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="234d6-114">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
