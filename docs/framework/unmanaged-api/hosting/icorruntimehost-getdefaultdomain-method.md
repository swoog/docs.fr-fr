---
title: ICorRuntimeHost::GetDefaultDomain, méthode
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.GetDefaultDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::GetDefaultDomain
helpviewer_keywords:
- ICorRuntimeHost::GetDefaultDomain method [.NET Framework hosting]
- GetDefaultDomain method [.NET Framework hosting]
ms.assetid: 5e17a6fc-f335-4aae-9bb0-c3e1271a9426
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 41a6c5ee73cad77368e83792d11d455d8fb163fc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61937027"
---
# <a name="icorruntimehostgetdefaultdomain-method"></a><span data-ttu-id="458bd-102">ICorRuntimeHost::GetDefaultDomain, méthode</span><span class="sxs-lookup"><span data-stu-id="458bd-102">ICorRuntimeHost::GetDefaultDomain Method</span></span>
<span data-ttu-id="458bd-103">Obtient un pointeur d’interface de type <xref:System._AppDomain?displayProperty=nameWithType> qui représente le domaine par défaut pour le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="458bd-103">Gets an interface pointer of type <xref:System._AppDomain?displayProperty=nameWithType> that represents the default domain for the current process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="458bd-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="458bd-104">Syntax</span></span>  
  
```  
HRESULT GetDefaultDomain (  
    [out] IUnknown** pAppDomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="458bd-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="458bd-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="458bd-106">[out] Un pointeur d’interface de type <xref:System._AppDomain?displayProperty=nameWithType> à la <xref:System.AppDomain> instance qui représente le domaine d’application par défaut pour le processus.</span><span class="sxs-lookup"><span data-stu-id="458bd-106">[out] An interface pointer of type <xref:System._AppDomain?displayProperty=nameWithType> to the <xref:System.AppDomain> instance that represents the default application domain for the process.</span></span>  
  
 <span data-ttu-id="458bd-107">Ce pointeur est tapé `IUnknown`, de sorte que les appelants doivent généralement appeler `QueryInterface` pour obtenir un pointeur d’interface de type <xref:System._AppDomain?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="458bd-107">This pointer is typed `IUnknown`, so callers should generally call `QueryInterface` to obtain an interface pointer of type <xref:System._AppDomain?displayProperty=nameWithType>.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="458bd-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="458bd-108">Return Value</span></span>  
  
|<span data-ttu-id="458bd-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="458bd-109">HRESULT</span></span>|<span data-ttu-id="458bd-110">Description</span><span class="sxs-lookup"><span data-stu-id="458bd-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="458bd-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="458bd-111">S_OK</span></span>|<span data-ttu-id="458bd-112">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="458bd-112">The operation was successful.</span></span>|  
|<span data-ttu-id="458bd-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="458bd-113">S_FALSE</span></span>|<span data-ttu-id="458bd-114">L’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="458bd-114">The operation failed to complete.</span></span>|  
|<span data-ttu-id="458bd-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="458bd-115">E_FAIL</span></span>|<span data-ttu-id="458bd-116">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="458bd-116">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="458bd-117">Si une méthode retourne E_FAIL, le common language runtime (CLR) n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="458bd-117">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="458bd-118">Les appels suivants à toute API d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="458bd-118">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="458bd-119">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="458bd-119">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="458bd-120">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="458bd-120">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="458bd-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="458bd-121">Requirements</span></span>  
 <span data-ttu-id="458bd-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="458bd-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="458bd-123">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="458bd-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="458bd-124">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="458bd-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="458bd-125">**Versions du .NET framework :** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="458bd-125">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="458bd-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="458bd-126">See also</span></span>

- <xref:System._AppDomain>
- <xref:System.AppDomain>
- [<span data-ttu-id="458bd-127">ICorRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="458bd-127">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
