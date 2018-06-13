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
ms.openlocfilehash: 95cbda3729c02b95557f9f700f1ea7c68aa450a1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33438013"
---
# <a name="igcthreadcontrolsuspensionstarting-method"></a><span data-ttu-id="bc46b-102">IGCThreadControl::SuspensionStarting, méthode</span><span class="sxs-lookup"><span data-stu-id="bc46b-102">IGCThreadControl::SuspensionStarting Method</span></span>
<span data-ttu-id="bc46b-103">Avertit l’hôte que le runtime débute une suspension du thread pour un garbage collection ou une suspension.</span><span class="sxs-lookup"><span data-stu-id="bc46b-103">Notifies the host that the runtime is beginning a thread suspension for a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bc46b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc46b-104">Syntax</span></span>  
  
```  
HRESULT SuspensionStarting ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="bc46b-105">Notes</span><span class="sxs-lookup"><span data-stu-id="bc46b-105">Remarks</span></span>  
 <span data-ttu-id="bc46b-106">Ne replanifiez pas de threads pendant le `SuspensionStarting` rappel.</span><span class="sxs-lookup"><span data-stu-id="bc46b-106">Do not reschedule any threads during the `SuspensionStarting` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bc46b-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bc46b-107">Requirements</span></span>  
 <span data-ttu-id="bc46b-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bc46b-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bc46b-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="bc46b-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bc46b-110">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bc46b-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bc46b-111">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bc46b-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bc46b-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc46b-112">See Also</span></span>  
 [<span data-ttu-id="bc46b-113">IGCThreadControl, interface</span><span class="sxs-lookup"><span data-stu-id="bc46b-113">IGCThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md)
