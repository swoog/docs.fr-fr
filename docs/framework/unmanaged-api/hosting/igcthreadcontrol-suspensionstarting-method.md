---
title: IGCThreadControl::SuspensionStarting, méthode
ms.date: 03/30/2017
api_name:
- IGCThreadControl.SuspensionStarting
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SuspensionStarting
helpviewer_keywords:
- IGCThreadControl::SuspensionStarting method [.NET Framework hosting]
- SuspensionStarting method, IGCThreadControl interface [.NET Framework hosting]
ms.assetid: 0af312af-98e9-415e-b182-42e80a1aee51
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7613bc744ad4c2e172fc4f6dd7bf282fb3d9072c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59179749"
---
# <a name="igcthreadcontrolsuspensionstarting-method"></a><span data-ttu-id="8a44a-102">IGCThreadControl::SuspensionStarting, méthode</span><span class="sxs-lookup"><span data-stu-id="8a44a-102">IGCThreadControl::SuspensionStarting Method</span></span>
<span data-ttu-id="8a44a-103">Avertit l’hôte que le runtime débute une suspension du thread pour un garbage collection ou une suspension.</span><span class="sxs-lookup"><span data-stu-id="8a44a-103">Notifies the host that the runtime is beginning a thread suspension for a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a44a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a44a-104">Syntax</span></span>  
  
```  
HRESULT SuspensionStarting ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="8a44a-105">Notes</span><span class="sxs-lookup"><span data-stu-id="8a44a-105">Remarks</span></span>  
 <span data-ttu-id="8a44a-106">Ne replanifiez pas de threads pendant le `SuspensionStarting` rappel.</span><span class="sxs-lookup"><span data-stu-id="8a44a-106">Do not reschedule any threads during the `SuspensionStarting` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a44a-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a44a-107">Requirements</span></span>  
 <span data-ttu-id="8a44a-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8a44a-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8a44a-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="8a44a-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8a44a-110">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8a44a-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8a44a-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8a44a-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8a44a-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a44a-112">See also</span></span>

- [<span data-ttu-id="8a44a-113">IGCThreadControl, interface</span><span class="sxs-lookup"><span data-stu-id="8a44a-113">IGCThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md)
