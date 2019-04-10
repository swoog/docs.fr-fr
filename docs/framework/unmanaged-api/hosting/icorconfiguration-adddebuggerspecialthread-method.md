---
title: ICorConfiguration::AddDebuggerSpecialThread, méthode
ms.date: 03/30/2017
api_name:
- ICorConfiguration.AddDebuggerSpecialThread
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- AddDebuggerSpecialThread
helpviewer_keywords:
- AddDebuggerSpecialThread method [.NET Framework hosting]
- ICorConfiguration::AddDebuggerSpecialThread method [.NET Framework hosting]
ms.assetid: 1f1e3239-438e-4be9-a3bb-7d0722d3a76d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: db1b19c1499f7e8a126933b4d0635a0ab73e72a8
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59218587"
---
# <a name="icorconfigurationadddebuggerspecialthread-method"></a><span data-ttu-id="f5b46-102">ICorConfiguration::AddDebuggerSpecialThread, méthode</span><span class="sxs-lookup"><span data-stu-id="f5b46-102">ICorConfiguration::AddDebuggerSpecialThread Method</span></span>
<span data-ttu-id="f5b46-103">Pour les services de débogage, indique qu’un thread particulier doit être autorisé à continuer à s’exécuter pendant que le débogueur arrête les scénarios de débogage managées ou une application.</span><span class="sxs-lookup"><span data-stu-id="f5b46-103">Indicates to the debugging services that a particular thread should be allowed to continue executing while the debugger has an application stopped during managed or unmanaged debugging scenarios.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5b46-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5b46-104">Syntax</span></span>  
  
```  
HRESULT AddDebuggerSpecialThread (  
    [in] DWORD dwSpecialThreadId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f5b46-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5b46-105">Parameters</span></span>  
 `dwSpecialThreadId`  
 <span data-ttu-id="f5b46-106">[in] L’ID du thread qui doit être autorisée à se poursuivre l’exécution.</span><span class="sxs-lookup"><span data-stu-id="f5b46-106">[in] The ID of the thread that should be allowed to continue executing.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f5b46-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f5b46-107">Remarks</span></span>  
 <span data-ttu-id="f5b46-108">Le thread spécifié ne pas exécuter du code managé ou entrez le runtime en aucune façon.</span><span class="sxs-lookup"><span data-stu-id="f5b46-108">The specified thread will not be allowed to run managed code or enter the runtime in any way.</span></span> <span data-ttu-id="f5b46-109">Un exemple d’un tel thread serait un thread de processus pour prendre en charge les débogueurs de script hérité.</span><span class="sxs-lookup"><span data-stu-id="f5b46-109">An example of such a thread would be an in-process thread to support legacy script debuggers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f5b46-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5b46-110">Requirements</span></span>  
 <span data-ttu-id="f5b46-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f5b46-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f5b46-112">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f5b46-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f5b46-113">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f5b46-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="f5b46-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="f5b46-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="f5b46-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5b46-115">See also</span></span>

- [<span data-ttu-id="f5b46-116">ICorConfiguration, interface</span><span class="sxs-lookup"><span data-stu-id="f5b46-116">ICorConfiguration Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md)
