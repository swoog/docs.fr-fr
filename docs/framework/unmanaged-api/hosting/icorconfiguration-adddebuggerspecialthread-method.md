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
ms.openlocfilehash: 067765fbf500b2d20d84273d8df70c8e05a6ddc4
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57485898"
---
# <a name="icorconfigurationadddebuggerspecialthread-method"></a><span data-ttu-id="76810-102">ICorConfiguration::AddDebuggerSpecialThread, méthode</span><span class="sxs-lookup"><span data-stu-id="76810-102">ICorConfiguration::AddDebuggerSpecialThread Method</span></span>
<span data-ttu-id="76810-103">Pour les services de débogage, indique qu’un thread particulier doit être autorisé à continuer à s’exécuter pendant que le débogueur arrête les scénarios de débogage managées ou une application.</span><span class="sxs-lookup"><span data-stu-id="76810-103">Indicates to the debugging services that a particular thread should be allowed to continue executing while the debugger has an application stopped during managed or unmanaged debugging scenarios.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="76810-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76810-104">Syntax</span></span>  
  
```  
HRESULT AddDebuggerSpecialThread (  
    [in] DWORD dwSpecialThreadId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="76810-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76810-105">Parameters</span></span>  
 `dwSpecialThreadId`  
 <span data-ttu-id="76810-106">[in] L’ID du thread qui doit être autorisée à se poursuivre l’exécution.</span><span class="sxs-lookup"><span data-stu-id="76810-106">[in] The ID of the thread that should be allowed to continue executing.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="76810-107">Notes</span><span class="sxs-lookup"><span data-stu-id="76810-107">Remarks</span></span>  
 <span data-ttu-id="76810-108">Le thread spécifié ne pas exécuter du code managé ou entrez le runtime en aucune façon.</span><span class="sxs-lookup"><span data-stu-id="76810-108">The specified thread will not be allowed to run managed code or enter the runtime in any way.</span></span> <span data-ttu-id="76810-109">Un exemple d’un tel thread serait un thread de processus pour prendre en charge les débogueurs de script hérité.</span><span class="sxs-lookup"><span data-stu-id="76810-109">An example of such a thread would be an in-process thread to support legacy script debuggers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="76810-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="76810-110">Requirements</span></span>  
 <span data-ttu-id="76810-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="76810-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="76810-112">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="76810-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="76810-113">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="76810-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="76810-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="76810-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76810-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76810-115">See also</span></span>
- [<span data-ttu-id="76810-116">ICorConfiguration, interface</span><span class="sxs-lookup"><span data-stu-id="76810-116">ICorConfiguration Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md)
