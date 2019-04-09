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
ms.openlocfilehash: afd8bd76f8d738c9eaa3a8e3d490e175e408b92b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59204300"
---
# <a name="icordebugmanagedcallbackcreateappdomain-method"></a><span data-ttu-id="9dac7-102">ICorDebugManagedCallback::CreateAppDomain, méthode</span><span class="sxs-lookup"><span data-stu-id="9dac7-102">ICorDebugManagedCallback::CreateAppDomain Method</span></span>
<span data-ttu-id="9dac7-103">Notifie le débogueur qu’un domaine d’application a été créé.</span><span class="sxs-lookup"><span data-stu-id="9dac7-103">Notifies the debugger that an application domain has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9dac7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9dac7-104">Syntax</span></span>  
  
```  
HRESULT CreateAppDomain (  
    [in] ICorDebugProcess   *pProcess,  
    [in] ICorDebugAppDomain *pAppDomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9dac7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9dac7-105">Parameters</span></span>  
 `pProcess`  
 <span data-ttu-id="9dac7-106">[in] Pointeur vers un objet ICorDebugProcess qui représente le processus dans lequel le domaine d’application a été créé.</span><span class="sxs-lookup"><span data-stu-id="9dac7-106">[in] A pointer to an ICorDebugProcess object that represents the process in which the application domain was created.</span></span>  
  
 `pAppDomain`  
 <span data-ttu-id="9dac7-107">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="9dac7-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that has been created.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9dac7-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9dac7-108">Requirements</span></span>  
 <span data-ttu-id="9dac7-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9dac7-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9dac7-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9dac7-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9dac7-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9dac7-111">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="9dac7-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="9dac7-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="9dac7-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dac7-113">See also</span></span>

- [<span data-ttu-id="9dac7-114">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="9dac7-114">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
