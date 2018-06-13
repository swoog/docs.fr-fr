---
title: IAppDomainBinding::OnAppDomain, méthode
ms.date: 03/30/2017
api_name:
- IAppDomainBinding.OnAppDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- OnAppDomain
helpviewer_keywords:
- IAppDomainBinding::OnAppDomain method [.NET Framework hosting]
- OnAppDomain method [.NET Framework hosting]
ms.assetid: b419dcc9-e8aa-484b-af0d-0f40358edb99
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5db040f6db078b211043c547eed823c9b495ac97
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33431320"
---
# <a name="iappdomainbindingonappdomain-method"></a><span data-ttu-id="a9f84-102">IAppDomainBinding::OnAppDomain, méthode</span><span class="sxs-lookup"><span data-stu-id="a9f84-102">IAppDomainBinding::OnAppDomain Method</span></span>
<span data-ttu-id="a9f84-103">Appelé par le common language runtime (CLR) pour notifier l’hôte qu’un domaine d’application a été créé.</span><span class="sxs-lookup"><span data-stu-id="a9f84-103">Called by the common language runtime (CLR) to notify the host that an application domain has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a9f84-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9f84-104">Syntax</span></span>  
  
```  
HRESULT OnAppDomain (  
    [in] IUnknown* pAppdomain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a9f84-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9f84-105">Parameters</span></span>  
 `pAppdomain`  
 <span data-ttu-id="a9f84-106">[in] Un pointeur vers un [IUnknown](https://msdn.microsoft.com/library/94as6ehy(v=vs.110).aspx) objet d’interface qui représente le nouveau domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="a9f84-106">[in] A pointer to an [IUnknown](https://msdn.microsoft.com/library/94as6ehy(v=vs.110).aspx) interface object that represents the new application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a9f84-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a9f84-107">Requirements</span></span>  
 <span data-ttu-id="a9f84-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a9f84-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a9f84-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a9f84-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a9f84-110">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a9f84-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a9f84-111">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a9f84-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9f84-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9f84-112">See Also</span></span>  
 [<span data-ttu-id="a9f84-113">IAppDomainBinding, interface</span><span class="sxs-lookup"><span data-stu-id="a9f84-113">IAppDomainBinding Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iappdomainbinding-interface.md)
