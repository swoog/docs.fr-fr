---
title: ICorDebugILFrame3, interface
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame3
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 15212cb5-93d4-4025-bec9-d4b9919eb1fe
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b46c74ec0bfc1fc44bcaca07439c472b0fd8393f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61946442"
---
# <a name="icordebugilframe3-interface"></a><span data-ttu-id="18a9a-102">ICorDebugILFrame3, interface</span><span class="sxs-lookup"><span data-stu-id="18a9a-102">ICorDebugILFrame3 Interface</span></span>
<span data-ttu-id="18a9a-103">Fournit une méthode qui encapsule la valeur de retour d'une fonction.</span><span class="sxs-lookup"><span data-stu-id="18a9a-103">Provides a method that encapsulates the return value of a function.</span></span> <span data-ttu-id="18a9a-104">`ICorDebugILFrame3` est une extension logique des interfaces ICorDebugILFrame et ICorDebugILFrame2.</span><span class="sxs-lookup"><span data-stu-id="18a9a-104">`ICorDebugILFrame3` is a logical extension of the ICorDebugILFrame and ICorDebugILFrame2 interfaces.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="18a9a-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="18a9a-105">Methods</span></span>  
  
|<span data-ttu-id="18a9a-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="18a9a-106">Method</span></span>|<span data-ttu-id="18a9a-107">Description</span><span class="sxs-lookup"><span data-stu-id="18a9a-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="18a9a-108">GetReturnValueForILOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="18a9a-108">GetReturnValueForILOffset Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe3-getreturnvalueforiloffset-method.md)|<span data-ttu-id="18a9a-109">Obtient un objet ICorDebugValue qui encapsule la valeur de retour d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="18a9a-109">Gets an ICorDebugValue object that encapsulates the return value of a function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="18a9a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="18a9a-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="18a9a-111">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="18a9a-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="18a9a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18a9a-112">Requirements</span></span>  
 <span data-ttu-id="18a9a-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="18a9a-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="18a9a-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="18a9a-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="18a9a-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="18a9a-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="18a9a-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="18a9a-116">**.NET Framework Versions:** [!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="18a9a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18a9a-117">See also</span></span>

- [<span data-ttu-id="18a9a-118">ICorDebugCode3, interface</span><span class="sxs-lookup"><span data-stu-id="18a9a-118">ICorDebugCode3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode3-interface.md)
- [<span data-ttu-id="18a9a-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="18a9a-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
