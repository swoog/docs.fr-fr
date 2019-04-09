---
title: ICorRuntimeHost::EnumDomains, méthode
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.EnumDomains
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::EnumDomains
helpviewer_keywords:
- ICorRuntimeHost::EnumDomains method [.NET Framework hosting]
- EnumDomains method [.NET Framework hosting]
ms.assetid: 96b74995-0cde-4876-b6df-7fc164e6a5d1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 69fcc862e98e305105a6f17ca49940bd10cef39c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59072556"
---
# <a name="icorruntimehostenumdomains-method"></a><span data-ttu-id="594d4-102">ICorRuntimeHost::EnumDomains, méthode</span><span class="sxs-lookup"><span data-stu-id="594d4-102">ICorRuntimeHost::EnumDomains Method</span></span>
<span data-ttu-id="594d4-103">Obtient un énumérateur pour les domaines dans le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="594d4-103">Gets an enumerator for the domains in the current process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="594d4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="594d4-104">Syntax</span></span>  
  
```  
HRESULT EnumDomains (  
    [out] HCORENUM *hEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="594d4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="594d4-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="594d4-106">[out] Un énumérateur pour les domaines.</span><span class="sxs-lookup"><span data-stu-id="594d4-106">[out] An enumerator for the domains.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="594d4-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="594d4-107">Return Value</span></span>  
  
|<span data-ttu-id="594d4-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="594d4-108">HRESULT</span></span>|<span data-ttu-id="594d4-109">Description</span><span class="sxs-lookup"><span data-stu-id="594d4-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="594d4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="594d4-110">S_OK</span></span>|<span data-ttu-id="594d4-111">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="594d4-111">The operation was successful.</span></span>|  
|<span data-ttu-id="594d4-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="594d4-112">S_FALSE</span></span>|<span data-ttu-id="594d4-113">L’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="594d4-113">The operation failed to complete.</span></span>|  
|<span data-ttu-id="594d4-114">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="594d4-114">E_FAIL</span></span>|<span data-ttu-id="594d4-115">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="594d4-115">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="594d4-116">Si une méthode retourne E_FAIL, le common language runtime (CLR) n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="594d4-116">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="594d4-117">Les appels suivants à toute API d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="594d4-117">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="594d4-118">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="594d4-118">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="594d4-119">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="594d4-119">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="594d4-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="594d4-120">Requirements</span></span>  
 <span data-ttu-id="594d4-121">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="594d4-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="594d4-122">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="594d4-122">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="594d4-123">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="594d4-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="594d4-124">**Version du .NET framework :** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="594d4-124">**.NET Framework Version:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="594d4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="594d4-125">See also</span></span>

- [<span data-ttu-id="594d4-126">ICorRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="594d4-126">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
