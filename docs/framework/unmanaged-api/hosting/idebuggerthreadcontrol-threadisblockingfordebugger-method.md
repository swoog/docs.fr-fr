---
title: IDebuggerThreadControl::ThreadIsBlockingForDebugger, méthode
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl.ThreadIsBlockingForDebugger
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ThreadIsBlockingForDebugger
helpviewer_keywords:
- ThreadIsBlockingForDebugger method [.NET Framework hosting]
- IDebuggerThreadControl::ThreadIsBlockingForDebugger method [.NET Framework hosting]
ms.assetid: d4d7cb2d-69da-48b3-879a-1a8a68c9bfa8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: aa72c136e98f80df6d2868c447e1c535ae61af06
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54739626"
---
# <a name="idebuggerthreadcontrolthreadisblockingfordebugger-method"></a><span data-ttu-id="cb8ad-102">IDebuggerThreadControl::ThreadIsBlockingForDebugger, méthode</span><span class="sxs-lookup"><span data-stu-id="cb8ad-102">IDebuggerThreadControl::ThreadIsBlockingForDebugger Method</span></span>
<span data-ttu-id="cb8ad-103">Avertit l’hôte que le thread qui envoie ce rappel concerne à blocs dans les services de débogage.</span><span class="sxs-lookup"><span data-stu-id="cb8ad-103">Notifies the host that the thread that is sending this callback is about to block within the debugging services.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cb8ad-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb8ad-104">Syntax</span></span>  
  
```  
HRESULT ThreadIsBlockingForDebugger ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="cb8ad-105">Notes</span><span class="sxs-lookup"><span data-stu-id="cb8ad-105">Remarks</span></span>  
 <span data-ttu-id="cb8ad-106">Le `ThreadIsBlockingForDebugger` méthode est toujours appelée sur un thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="cb8ad-106">The `ThreadIsBlockingForDebugger` method will always be called on a runtime thread.</span></span>  
  
 <span data-ttu-id="cb8ad-107">Le `ThreadIsBlockingForDebugger` méthode donne à l’hôte une possibilité d’effectuer une autre action pendant que le thread bloque.</span><span class="sxs-lookup"><span data-stu-id="cb8ad-107">The `ThreadIsBlockingForDebugger` method gives the host an opportunity to perform another action while the thread blocks.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cb8ad-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cb8ad-108">Requirements</span></span>  
 <span data-ttu-id="cb8ad-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cb8ad-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cb8ad-110">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="cb8ad-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="cb8ad-111">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cb8ad-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cb8ad-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cb8ad-112">**NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cb8ad-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb8ad-113">See also</span></span>
- [<span data-ttu-id="cb8ad-114">IDebuggerThreadControl, interface</span><span class="sxs-lookup"><span data-stu-id="cb8ad-114">IDebuggerThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-interface.md)
