---
title: ICorThreadpool::CorDeleteTimer, méthode
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorDeleteTimer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorDeleteTimer
helpviewer_keywords:
- ICorThreadpool::CorDeleteTimer method [.NET Framework hosting]
- CorDeleteTimer method [.NET Framework hosting]
ms.assetid: 74847c35-7ca1-466a-b750-b25e7b03d100
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 098c23dd0ddff4342aa4cefbaa4e149ed95a1cb3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59178345"
---
# <a name="icorthreadpoolcordeletetimer-method"></a><span data-ttu-id="2880a-102">ICorThreadpool::CorDeleteTimer, méthode</span><span class="sxs-lookup"><span data-stu-id="2880a-102">ICorThreadpool::CorDeleteTimer Method</span></span>
<span data-ttu-id="2880a-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="2880a-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2880a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2880a-104">Syntax</span></span>  
  
```  
HRESULT CorDeleteTimer (  
    [in]  HANDLE Timer,  
    [in]  HANDLE CompletionEvent,  
    [out] BOOL*  result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="2880a-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2880a-105">Requirements</span></span>  
 <span data-ttu-id="2880a-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2880a-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2880a-107">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="2880a-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2880a-108">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2880a-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="2880a-109">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="2880a-109">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="2880a-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2880a-110">See also</span></span>

- [<span data-ttu-id="2880a-111">ICorThreadpool, interface</span><span class="sxs-lookup"><span data-stu-id="2880a-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
