---
title: ICorRuntimeHost::SwitchOutLogicalThreadState, méthode
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.SwitchOutLogicalThreadState
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::SwitchOutLogicalThreadState
helpviewer_keywords:
- ICorRuntimeHost::SwitchOutLogicalThreadState method [.NET Framework hosting]
- SwitchOutLogicalThreadState method [.NET Framework hosting]
ms.assetid: e1968f0b-2675-4dc2-8507-46164e1df154
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ff3bd9345825b5e7a4ccb41cd260b447b74cede3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33437948"
---
# <a name="icorruntimehostswitchoutlogicalthreadstate-method"></a><span data-ttu-id="e0cb0-102">ICorRuntimeHost::SwitchOutLogicalThreadState, méthode</span><span class="sxs-lookup"><span data-stu-id="e0cb0-102">ICorRuntimeHost::SwitchOutLogicalThreadState Method</span></span>
<span data-ttu-id="e0cb0-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="e0cb0-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e0cb0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0cb0-104">Syntax</span></span>  
  
```  
HRESULT SwitchOutLogicalThreadState(  
    [out] DWORD **pFiberCookie  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e0cb0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0cb0-105">Parameters</span></span>  
 `pFiberCookie`  
 <span data-ttu-id="e0cb0-106">[out] Cookie qui indique la fibre en cours de basculement.</span><span class="sxs-lookup"><span data-stu-id="e0cb0-106">[out] Cookie that indicates the fiber being switched out.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e0cb0-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e0cb0-107">Requirements</span></span>  
 <span data-ttu-id="e0cb0-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e0cb0-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e0cb0-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e0cb0-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e0cb0-110">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e0cb0-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e0cb0-111">**Version du .NET framework :** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="e0cb0-111">**.NET Framework Version:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e0cb0-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0cb0-112">See Also</span></span>  
 [<span data-ttu-id="e0cb0-113">ICorRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="e0cb0-113">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
