---
title: ICorRuntimeHost::LocksHeldByLogicalThread, méthode
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.LocksHeldByLogicalThread
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::LocksHeldByLogicalThread
helpviewer_keywords:
- ICorRuntimeHost::LocksHeldByLogicalThread method [.NET Framework hosting]
- LocksHeldByLogicalThread method [.NET Framework hosting]
ms.assetid: c3601255-d894-4d7c-b1df-c31334551700
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 90af015de4428f75330de89978a7fc0a4b26750b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59144194"
---
# <a name="icorruntimehostlocksheldbylogicalthread-method"></a><span data-ttu-id="5af15-102">ICorRuntimeHost::LocksHeldByLogicalThread, méthode</span><span class="sxs-lookup"><span data-stu-id="5af15-102">ICorRuntimeHost::LocksHeldByLogicalThread Method</span></span>
<span data-ttu-id="5af15-103">Récupère le nombre de verrous que le thread actif détient.</span><span class="sxs-lookup"><span data-stu-id="5af15-103">Retrieves the number of locks that current thread holds.</span></span>  
  
 <span data-ttu-id="5af15-104">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="5af15-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5af15-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5af15-105">Syntax</span></span>  
  
```  
HRESULT LocksHeldByLogicalThread(  
    [out] DWORD *pCount  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5af15-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5af15-106">Parameters</span></span>  
 `pCount`  
 <span data-ttu-id="5af15-107">[out] Pointeur vers le nombre de verrous maintenus par le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="5af15-107">[out] A pointer to the number of locks that the current thread holds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5af15-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5af15-108">Requirements</span></span>  
 <span data-ttu-id="5af15-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5af15-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5af15-110">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="5af15-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5af15-111">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5af15-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5af15-112">**Versions du .NET framework :** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="5af15-112">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5af15-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5af15-113">See also</span></span>

- [<span data-ttu-id="5af15-114">ICorRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="5af15-114">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
