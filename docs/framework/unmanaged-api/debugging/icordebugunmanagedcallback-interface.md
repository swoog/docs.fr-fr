---
title: ICorDebugUnmanagedCallback, interface
ms.date: 03/30/2017
api_name:
- ICorDebugUnmanagedCallback
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugUnmanagedCallback
helpviewer_keywords:
- ICorDebugUnmanagedCallback interface [.NET Framework debugging]
ms.assetid: bc71cbca-7d73-40e5-84dd-2109fade3c2a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5b55b27d45ef3efea10215c8a4163b5981f9d145
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33422849"
---
# <a name="icordebugunmanagedcallback-interface"></a><span data-ttu-id="c3d02-102">ICorDebugUnmanagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="c3d02-102">ICorDebugUnmanagedCallback Interface</span></span>
<span data-ttu-id="c3d02-103">Fournit une notification des événements natifs qui ne sont pas directement liées pour le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="c3d02-103">Provides notification of native events that are not directly related to the common language runtime (CLR).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c3d02-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c3d02-104">Methods</span></span>  
  
|<span data-ttu-id="c3d02-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="c3d02-105">Method</span></span>|<span data-ttu-id="c3d02-106">Description</span><span class="sxs-lookup"><span data-stu-id="c3d02-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c3d02-107">DebugEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="c3d02-107">DebugEvent Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugunmanagedcallback-debugevent-method.md)|<span data-ttu-id="c3d02-108">Notifie le débogueur qu’un événement natif a été déclenché.</span><span class="sxs-lookup"><span data-stu-id="c3d02-108">Notifies the debugger that a native event has been fired.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c3d02-109">Notes</span><span class="sxs-lookup"><span data-stu-id="c3d02-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c3d02-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="c3d02-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c3d02-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c3d02-111">Requirements</span></span>  
 <span data-ttu-id="c3d02-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c3d02-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c3d02-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c3d02-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c3d02-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c3d02-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c3d02-115">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c3d02-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c3d02-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3d02-116">See Also</span></span>  
 [<span data-ttu-id="c3d02-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="c3d02-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
