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
ms.openlocfilehash: 321298ce942b35d11a861c87cdf6b8714179ea97
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59080835"
---
# <a name="icordebugterminate-method"></a><span data-ttu-id="0a862-102">ICorDebug::Terminate, méthode</span><span class="sxs-lookup"><span data-stu-id="0a862-102">ICorDebug::Terminate Method</span></span>
<span data-ttu-id="0a862-103">Met fin à la `ICorDebug` objet.</span><span class="sxs-lookup"><span data-stu-id="0a862-103">Terminates the `ICorDebug` object.</span></span>  
  
> [!NOTE]
>  `Terminate` <span data-ttu-id="0a862-104">ne doit pas être appelée jusqu'à un [ICorDebugManagedCallback::ExitProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md) rappel a été reçu pour tous les processus en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="0a862-104">should not be called until an [ICorDebugManagedCallback::ExitProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md) callback has been received for all processes being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a862-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a862-105">Syntax</span></span>  
  
```  
HRESULT Terminate ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="0a862-106">Notes</span><span class="sxs-lookup"><span data-stu-id="0a862-106">Remarks</span></span>  
 `Terminate` <span data-ttu-id="0a862-107">doit être appelé lorsque le `ICorDebug` objet n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0a862-107">must be called when the `ICorDebug` object is no longer needed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0a862-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a862-108">Requirements</span></span>  
 <span data-ttu-id="0a862-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0a862-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0a862-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0a862-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0a862-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0a862-111">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="0a862-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="0a862-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0a862-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a862-113">See also</span></span>

- [<span data-ttu-id="0a862-114">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="0a862-114">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
