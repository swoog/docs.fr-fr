---
title: ICorDebugManagedCallback::CreateAppDomain, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.CreateAppDomain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::CreateAppDomain
helpviewer_keywords:
- CreateAppDomain method [.NET Framework debugging]
- ICorDebugManagedCallback::CreateAppDomain method [.NET Framework debugging]
ms.assetid: 48d410d7-6749-4125-a8fd-f9562c7088e9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bdac4b5b7a4a64a5fc939a7d35718ef276717fe7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33415426"
---
# <a name="icordebugmanagedcallbackcreateappdomain-method"></a><span data-ttu-id="9946a-102">ICorDebugManagedCallback::CreateAppDomain, méthode</span><span class="sxs-lookup"><span data-stu-id="9946a-102">ICorDebugManagedCallback::CreateAppDomain Method</span></span>
<span data-ttu-id="9946a-103">Notifie le débogueur qu’un domaine d’application a été créé.</span><span class="sxs-lookup"><span data-stu-id="9946a-103">Notifies the debugger that an application domain has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9946a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9946a-104">Syntax</span></span>  
  
```  
HRESULT CreateAppDomain (  
    [in] ICorDebugProcess   *pProcess,  
    [in] ICorDebugAppDomain *pAppDomain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9946a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9946a-105">Parameters</span></span>  
 `pProcess`  
 <span data-ttu-id="9946a-106">[in] Pointeur vers un objet ICorDebugProcess qui représente le processus dans lequel le domaine d’application a été créé.</span><span class="sxs-lookup"><span data-stu-id="9946a-106">[in] A pointer to an ICorDebugProcess object that represents the process in which the application domain was created.</span></span>  
  
 `pAppDomain`  
 <span data-ttu-id="9946a-107">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="9946a-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that has been created.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9946a-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9946a-108">Requirements</span></span>  
 <span data-ttu-id="9946a-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9946a-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9946a-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9946a-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9946a-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9946a-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9946a-112">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9946a-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9946a-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9946a-113">See Also</span></span>  
 [<span data-ttu-id="9946a-114">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="9946a-114">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
