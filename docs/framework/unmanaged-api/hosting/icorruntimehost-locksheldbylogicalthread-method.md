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
ms.openlocfilehash: d46881b76685fd04f8bc5e3a67830e58f85cd774
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33436674"
---
# <a name="icorruntimehostlocksheldbylogicalthread-method"></a><span data-ttu-id="9d9fb-102">ICorRuntimeHost::LocksHeldByLogicalThread, méthode</span><span class="sxs-lookup"><span data-stu-id="9d9fb-102">ICorRuntimeHost::LocksHeldByLogicalThread Method</span></span>
<span data-ttu-id="9d9fb-103">Récupère le nombre de verrous que le thread actif détient.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-103">Retrieves the number of locks that current thread holds.</span></span>  
  
 <span data-ttu-id="9d9fb-104">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9d9fb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d9fb-105">Syntax</span></span>  
  
```  
HRESULT LocksHeldByLogicalThread(  
    [out] DWORD *pCount  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9d9fb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d9fb-106">Parameters</span></span>  
 `pCount`  
 <span data-ttu-id="9d9fb-107">[out] Pointeur vers le nombre de verrous maintenus par le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-107">[out] A pointer to the number of locks that the current thread holds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9d9fb-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9d9fb-108">Requirements</span></span>  
 <span data-ttu-id="9d9fb-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9d9fb-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9d9fb-110">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="9d9fb-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9d9fb-111">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9d9fb-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9d9fb-112">**Versions du .NET framework :** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="9d9fb-112">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d9fb-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d9fb-113">See Also</span></span>  
 [<span data-ttu-id="9d9fb-114">ICorRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="9d9fb-114">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
