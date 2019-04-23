---
title: ICorRuntimeHost::SwitchInLogicalThreadState, méthode
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.SwitchInLogicalThreadState
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::SwitchInLogicalThreadState
helpviewer_keywords:
- ICorRuntimeHost::SwitchInLogicalThreadState method [.NET Framework hosting]
- SwitchInLogicalThreadState method [.NET Framework hosting]
ms.assetid: 7df1e492-8014-43ea-80d1-a4743e9b1c17
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fc6cd8d2d0ab4648ad20392ef0968907917677e9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59209487"
---
# <a name="icorruntimehostswitchinlogicalthreadstate-method"></a><span data-ttu-id="6ce31-102">ICorRuntimeHost::SwitchInLogicalThreadState, méthode</span><span class="sxs-lookup"><span data-stu-id="6ce31-102">ICorRuntimeHost::SwitchInLogicalThreadState Method</span></span>
<span data-ttu-id="6ce31-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="6ce31-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6ce31-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ce31-104">Syntax</span></span>  
  
```  
HRESULT SwitchInLogicalThreadState(  
    [in] DWORD *pFiberCookie  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6ce31-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ce31-105">Parameters</span></span>  
 `pFiberCookie`  
 <span data-ttu-id="6ce31-106">[in] Cookie qui indique la fibre à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6ce31-106">[in] Cookie that indicates the fiber to use.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6ce31-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ce31-107">Requirements</span></span>  
 <span data-ttu-id="6ce31-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6ce31-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6ce31-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="6ce31-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6ce31-110">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6ce31-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6ce31-111">**Version du .NET framework :** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="6ce31-111">**.NET Framework Version:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6ce31-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ce31-112">See also</span></span>

- [<span data-ttu-id="6ce31-113">ICorRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="6ce31-113">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
