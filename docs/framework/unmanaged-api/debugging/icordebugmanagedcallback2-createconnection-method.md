---
title: ICorDebugManagedCallback2::CreateConnection, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback2.CreateConnection
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback2::CreateConnection
helpviewer_keywords:
- CreateConnection method [.NET Framework debugging]
- ICorDebugManagedCallback2::CreateConnection method [.NET Framework debugging]
ms.assetid: 49e647be-9d63-4250-9d11-704e2a400d1b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f5035cd22ed099cec5e327c6957b13bcee52c766
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59191122"
---
# <a name="icordebugmanagedcallback2createconnection-method"></a><span data-ttu-id="0b5b6-102">ICorDebugManagedCallback2::CreateConnection, méthode</span><span class="sxs-lookup"><span data-stu-id="0b5b6-102">ICorDebugManagedCallback2::CreateConnection Method</span></span>
<span data-ttu-id="0b5b6-103">Notifie le débogueur qu’une nouvelle connexion a été créée.</span><span class="sxs-lookup"><span data-stu-id="0b5b6-103">Notifies the debugger that a new connection has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0b5b6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b5b6-104">Syntax</span></span>  
  
```  
HRESULT CreateConnection (  
    [in] ICorDebugProcess     *pProcess,  
    [in] CONNID               dwConnectionId,  
    [in] WCHAR                *pConnName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0b5b6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b5b6-105">Parameters</span></span>  
 `pProcess`  
 <span data-ttu-id="0b5b6-106">[in] Un pointeur vers un objet « ICorDebugProcess » qui représente le processus dans lequel la connexion a été créée</span><span class="sxs-lookup"><span data-stu-id="0b5b6-106">[in] A pointer to an "ICorDebugProcess" object that represents the process in which the connection was created</span></span>  
  
 `dwConnectionId`  
 <span data-ttu-id="0b5b6-107">[in] ID de la nouvelle connexion.</span><span class="sxs-lookup"><span data-stu-id="0b5b6-107">[in] The ID of the new connection.</span></span>  
  
 `pConnName`  
 <span data-ttu-id="0b5b6-108">[in] Un pointeur vers le nom de la nouvelle connexion.</span><span class="sxs-lookup"><span data-stu-id="0b5b6-108">[in] A pointer to the name of the new connection.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0b5b6-109">Notes</span><span class="sxs-lookup"><span data-stu-id="0b5b6-109">Remarks</span></span>  
 <span data-ttu-id="0b5b6-110">Un `CreateConnection` rappel est déclenché dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="0b5b6-110">A `CreateConnection` callback will be fired in either of the following cases:</span></span>  
  
-   <span data-ttu-id="0b5b6-111">Quand un débogueur est attaché à un processus qui contient les connexions.</span><span class="sxs-lookup"><span data-stu-id="0b5b6-111">When a debugger attaches to a process that contains connections.</span></span> <span data-ttu-id="0b5b6-112">Dans ce cas, le runtime générer et distribuer un `CreateConnection` événement et un [ICorDebugManagedCallback2::ChangeConnection](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-changeconnection-method.md) événement pour chaque connexion dans le processus.</span><span class="sxs-lookup"><span data-stu-id="0b5b6-112">In this case, the runtime will generate and dispatch a `CreateConnection` event and a [ICorDebugManagedCallback2::ChangeConnection](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-changeconnection-method.md) event for each connection in the process.</span></span>  
  
-   <span data-ttu-id="0b5b6-113">Lorsqu’un hôte appelle [ICLRDebugManager::BeginConnection](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-beginconnection-method.md) dans le [API d’hébergement](../../../../docs/framework/unmanaged-api/hosting/index.md).</span><span class="sxs-lookup"><span data-stu-id="0b5b6-113">When a host calls [ICLRDebugManager::BeginConnection](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-beginconnection-method.md) in the [Hosting API](../../../../docs/framework/unmanaged-api/hosting/index.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0b5b6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b5b6-114">Requirements</span></span>  
 <span data-ttu-id="0b5b6-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0b5b6-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0b5b6-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0b5b6-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0b5b6-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0b5b6-117">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="0b5b6-118">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="0b5b6-118">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0b5b6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b5b6-119">See also</span></span>

- [<span data-ttu-id="0b5b6-120">ICorDebugManagedCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="0b5b6-120">ICorDebugManagedCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md)
- [<span data-ttu-id="0b5b6-121">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="0b5b6-121">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
