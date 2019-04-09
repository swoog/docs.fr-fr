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
ms.openlocfilehash: 60a1546068ae6a8c8be1c0af1ef3c7d770c23d70
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59128674"
---
# <a name="icordebugunmanagedcallback-interface"></a><span data-ttu-id="bcc94-102">ICorDebugUnmanagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="bcc94-102">ICorDebugUnmanagedCallback Interface</span></span>
<span data-ttu-id="bcc94-103">Fournit une notification des événements natifs qui ne sont pas directement liées pour le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="bcc94-103">Provides notification of native events that are not directly related to the common language runtime (CLR).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="bcc94-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bcc94-104">Methods</span></span>  
  
|<span data-ttu-id="bcc94-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="bcc94-105">Method</span></span>|<span data-ttu-id="bcc94-106">Description</span><span class="sxs-lookup"><span data-stu-id="bcc94-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="bcc94-107">DebugEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="bcc94-107">DebugEvent Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugunmanagedcallback-debugevent-method.md)|<span data-ttu-id="bcc94-108">Notifie le débogueur qu’un événement natif a été déclenché.</span><span class="sxs-lookup"><span data-stu-id="bcc94-108">Notifies the debugger that a native event has been fired.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bcc94-109">Notes</span><span class="sxs-lookup"><span data-stu-id="bcc94-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="bcc94-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="bcc94-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bcc94-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcc94-111">Requirements</span></span>  
 <span data-ttu-id="bcc94-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bcc94-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bcc94-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bcc94-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bcc94-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bcc94-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="bcc94-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="bcc94-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="bcc94-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcc94-116">See also</span></span>

- [<span data-ttu-id="bcc94-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="bcc94-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
