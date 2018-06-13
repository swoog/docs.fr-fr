---
title: IGCThreadControl::ThreadIsBlockingForSuspension, méthode
ms.date: 03/30/2017
api_name:
- IGCThreadControl.ThreadIsBlockingForSuspension
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ThreadIsBlockingForSuspension
helpviewer_keywords:
- IGCThreadControl::ThreadIsBlockingForSuspension method [.NET Framework hosting]
- ThreadIsBlockingForSuspension method [.NET Framework hosting]
ms.assetid: ed5b5b58-7db7-46b5-9e2c-278db7159cee
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6f4b767fe7134833ee2e404be30bb51bf1385ec9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33437035"
---
# <a name="igcthreadcontrolthreadisblockingforsuspension-method"></a><span data-ttu-id="2b9be-102">IGCThreadControl::ThreadIsBlockingForSuspension, méthode</span><span class="sxs-lookup"><span data-stu-id="2b9be-102">IGCThreadControl::ThreadIsBlockingForSuspension Method</span></span>
<span data-ttu-id="2b9be-103">Avertit l’hôte que le thread qui effectue l’appel va bloquer, peut-être pour un garbage collection ou une suspension.</span><span class="sxs-lookup"><span data-stu-id="2b9be-103">Notifies the host that the thread that is making the call is about to block, perhaps for a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b9be-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b9be-104">Syntax</span></span>  
  
```  
HRESULT ThreadIsBlockingForSuspension ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="2b9be-105">Notes</span><span class="sxs-lookup"><span data-stu-id="2b9be-105">Remarks</span></span>  
 <span data-ttu-id="2b9be-106">L’hôte peut choisir dans le `ThreadIsBlockingForSuspension` rappel de replanifier un thread.</span><span class="sxs-lookup"><span data-stu-id="2b9be-106">The host may choose within the `ThreadIsBlockingForSuspension` callback whether to reschedule a thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2b9be-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2b9be-107">Requirements</span></span>  
 <span data-ttu-id="2b9be-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2b9be-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2b9be-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="2b9be-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2b9be-110">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2b9be-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2b9be-111">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2b9be-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b9be-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b9be-112">See Also</span></span>  
 [<span data-ttu-id="2b9be-113">IGCThreadControl, interface</span><span class="sxs-lookup"><span data-stu-id="2b9be-113">IGCThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md)
