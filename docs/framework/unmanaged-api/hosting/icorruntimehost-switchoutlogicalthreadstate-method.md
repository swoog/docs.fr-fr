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
ms.openlocfilehash: 291fb64bd86c1670945136e5ec7f586496f77d49
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54730215"
---
# <a name="icorruntimehostswitchoutlogicalthreadstate-method"></a><span data-ttu-id="8efde-102">ICorRuntimeHost::SwitchOutLogicalThreadState, méthode</span><span class="sxs-lookup"><span data-stu-id="8efde-102">ICorRuntimeHost::SwitchOutLogicalThreadState Method</span></span>
<span data-ttu-id="8efde-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="8efde-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8efde-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8efde-104">Syntax</span></span>  
  
```  
HRESULT SwitchOutLogicalThreadState(  
    [out] DWORD **pFiberCookie  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8efde-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8efde-105">Parameters</span></span>  
 `pFiberCookie`  
 <span data-ttu-id="8efde-106">[out] Cookie qui indique la fibre en cours de basculement.</span><span class="sxs-lookup"><span data-stu-id="8efde-106">[out] Cookie that indicates the fiber being switched out.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8efde-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8efde-107">Requirements</span></span>  
 <span data-ttu-id="8efde-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8efde-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8efde-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="8efde-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8efde-110">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8efde-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8efde-111">**Version du .NET framework :** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="8efde-111">**.NET Framework Version:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8efde-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8efde-112">See also</span></span>
- [<span data-ttu-id="8efde-113">ICorRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="8efde-113">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
