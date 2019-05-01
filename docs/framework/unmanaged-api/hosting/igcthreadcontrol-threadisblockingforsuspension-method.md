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
ms.openlocfilehash: 7cd6c1dff30bce8857b9fb4092670667109932c3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61984449"
---
# <a name="igcthreadcontrolthreadisblockingforsuspension-method"></a><span data-ttu-id="813e7-102">IGCThreadControl::ThreadIsBlockingForSuspension, méthode</span><span class="sxs-lookup"><span data-stu-id="813e7-102">IGCThreadControl::ThreadIsBlockingForSuspension Method</span></span>
<span data-ttu-id="813e7-103">Avertit l’hôte que le thread qui effectue l’appel va bloquer, peut-être pour une opération garbage collection ou une suspension.</span><span class="sxs-lookup"><span data-stu-id="813e7-103">Notifies the host that the thread that is making the call is about to block, perhaps for a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="813e7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="813e7-104">Syntax</span></span>  
  
```  
HRESULT ThreadIsBlockingForSuspension ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="813e7-105">Notes</span><span class="sxs-lookup"><span data-stu-id="813e7-105">Remarks</span></span>  
 <span data-ttu-id="813e7-106">L’hôte peut choisir dans le `ThreadIsBlockingForSuspension` rappel s’il faut replanifier un thread.</span><span class="sxs-lookup"><span data-stu-id="813e7-106">The host may choose within the `ThreadIsBlockingForSuspension` callback whether to reschedule a thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="813e7-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="813e7-107">Requirements</span></span>  
 <span data-ttu-id="813e7-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="813e7-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="813e7-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="813e7-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="813e7-110">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="813e7-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="813e7-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="813e7-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="813e7-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="813e7-112">See also</span></span>

- [<span data-ttu-id="813e7-113">IGCThreadControl, interface</span><span class="sxs-lookup"><span data-stu-id="813e7-113">IGCThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md)
