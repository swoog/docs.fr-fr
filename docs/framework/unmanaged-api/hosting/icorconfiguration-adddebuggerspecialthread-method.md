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
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59218587"
---
# <a name="icorconfigurationadddebuggerspecialthread-method"></a><span data-ttu-id="9d1af-102">ICorConfiguration::AddDebuggerSpecialThread, méthode</span><span class="sxs-lookup"><span data-stu-id="9d1af-102">ICorConfiguration::AddDebuggerSpecialThread Method</span></span>
<span data-ttu-id="9d1af-103">Pour les services de débogage, indique qu’un thread particulier doit être autorisé à continuer à s’exécuter pendant que le débogueur arrête les scénarios de débogage managées ou une application.</span><span class="sxs-lookup"><span data-stu-id="9d1af-103">Indicates to the debugging services that a particular thread should be allowed to continue executing while the debugger has an application stopped during managed or unmanaged debugging scenarios.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9d1af-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d1af-104">Syntax</span></span>  
  
```  
HRESULT AddDebuggerSpecialThread (  
    [in] DWORD dwSpecialThreadId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9d1af-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d1af-105">Parameters</span></span>  
 `dwSpecialThreadId`  
 <span data-ttu-id="9d1af-106">[in] L’ID du thread qui doit être autorisée à se poursuivre l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9d1af-106">[in] The ID of the thread that should be allowed to continue executing.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9d1af-107">Notes</span><span class="sxs-lookup"><span data-stu-id="9d1af-107">Remarks</span></span>  
 <span data-ttu-id="9d1af-108">Le thread spécifié ne pas exécuter du code managé ou entrez le runtime en aucune façon.</span><span class="sxs-lookup"><span data-stu-id="9d1af-108">The specified thread will not be allowed to run managed code or enter the runtime in any way.</span></span> <span data-ttu-id="9d1af-109">Un exemple d’un tel thread serait un thread de processus pour prendre en charge les débogueurs de script hérité.</span><span class="sxs-lookup"><span data-stu-id="9d1af-109">An example of such a thread would be an in-process thread to support legacy script debuggers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9d1af-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d1af-110">Requirements</span></span>  
 <span data-ttu-id="9d1af-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9d1af-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9d1af-112">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="9d1af-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9d1af-113">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9d1af-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9d1af-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9d1af-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d1af-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d1af-115">See also</span></span>

- [<span data-ttu-id="9d1af-116">ICorConfiguration, interface</span><span class="sxs-lookup"><span data-stu-id="9d1af-116">ICorConfiguration Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md)
