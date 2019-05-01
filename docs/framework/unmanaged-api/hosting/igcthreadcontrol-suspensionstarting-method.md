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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61992756"
---
# <a name="igcthreadcontrolsuspensionstarting-method"></a><span data-ttu-id="a4ff2-102">IGCThreadControl::SuspensionStarting, méthode</span><span class="sxs-lookup"><span data-stu-id="a4ff2-102">IGCThreadControl::SuspensionStarting Method</span></span>
<span data-ttu-id="a4ff2-103">Avertit l’hôte que le runtime débute une suspension du thread pour un garbage collection ou une suspension.</span><span class="sxs-lookup"><span data-stu-id="a4ff2-103">Notifies the host that the runtime is beginning a thread suspension for a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a4ff2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4ff2-104">Syntax</span></span>  
  
```  
HRESULT SuspensionStarting ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="a4ff2-105">Notes</span><span class="sxs-lookup"><span data-stu-id="a4ff2-105">Remarks</span></span>  
 <span data-ttu-id="a4ff2-106">Ne replanifiez pas de threads pendant le `SuspensionStarting` rappel.</span><span class="sxs-lookup"><span data-stu-id="a4ff2-106">Do not reschedule any threads during the `SuspensionStarting` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a4ff2-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4ff2-107">Requirements</span></span>  
 <span data-ttu-id="a4ff2-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a4ff2-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a4ff2-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a4ff2-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a4ff2-110">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a4ff2-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a4ff2-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a4ff2-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a4ff2-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4ff2-112">See also</span></span>

- [<span data-ttu-id="a4ff2-113">IGCThreadControl, interface</span><span class="sxs-lookup"><span data-stu-id="a4ff2-113">IGCThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md)
