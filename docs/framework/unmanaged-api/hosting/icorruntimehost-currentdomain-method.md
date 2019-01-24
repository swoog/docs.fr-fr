---
title: ICorRuntimeHost::CurrentDomain, méthode
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.CurrentDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::CurrentDomain
helpviewer_keywords:
- ICorRuntimeHost::CreateDomain method [.NET Framework hosting]
- CurrentDomain method [.NET Framework hosting]
ms.assetid: dd2afb38-675b-4c3c-a9f3-8ab3b133eb02
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3c62eba75759755f74e7b81393dced0d8433ba3b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54606278"
---
# <a name="icorruntimehostcurrentdomain-method"></a><span data-ttu-id="0bda3-102">ICorRuntimeHost::CurrentDomain, méthode</span><span class="sxs-lookup"><span data-stu-id="0bda3-102">ICorRuntimeHost::CurrentDomain Method</span></span>
<span data-ttu-id="0bda3-103">Obtient un pointeur d’interface de type <xref:System.AppDomain?displayProperty=nameWithType> qui représente le domaine chargé sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="0bda3-103">Gets an interface pointer of type <xref:System.AppDomain?displayProperty=nameWithType> that represents the domain loaded on the current thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0bda3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bda3-104">Syntax</span></span>  
  
```  
HRESULT CurrentDomain (  
    [out] IUnknown** pAppDomain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0bda3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0bda3-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="0bda3-106">[out] Un pointeur de type <xref:System.AppDomain?displayProperty=nameWithType> qui représente le domaine d’application actuel du thread.</span><span class="sxs-lookup"><span data-stu-id="0bda3-106">[out] A pointer of type <xref:System.AppDomain?displayProperty=nameWithType> that represents the thread's current application domain.</span></span> <span data-ttu-id="0bda3-107">Ce pointeur est tapé `IUnknown`, de sorte que les appelants doivent généralement appeler `QueryInterface` pour obtenir un pointeur de type <xref:System._AppDomain>.</span><span class="sxs-lookup"><span data-stu-id="0bda3-107">This pointer is typed `IUnknown`, so callers should generally call `QueryInterface` to obtain a pointer of type <xref:System._AppDomain>.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0bda3-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0bda3-108">Return Value</span></span>  
  
|<span data-ttu-id="0bda3-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="0bda3-109">HRESULT</span></span>|<span data-ttu-id="0bda3-110">Description</span><span class="sxs-lookup"><span data-stu-id="0bda3-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0bda3-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="0bda3-111">S_OK</span></span>|<span data-ttu-id="0bda3-112">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="0bda3-112">The operation was successful.</span></span>|  
|<span data-ttu-id="0bda3-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="0bda3-113">S_FALSE</span></span>|<span data-ttu-id="0bda3-114">L’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="0bda3-114">The operation failed to complete.</span></span>|  
|<span data-ttu-id="0bda3-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0bda3-115">E_FAIL</span></span>|<span data-ttu-id="0bda3-116">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0bda3-116">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="0bda3-117">Si une méthode retourne E_FAIL, le common language runtime (CLR) n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="0bda3-117">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="0bda3-118">Les appels suivants à toute API d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="0bda3-118">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="0bda3-119">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="0bda3-119">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="0bda3-120">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="0bda3-120">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0bda3-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0bda3-121">Requirements</span></span>  
 <span data-ttu-id="0bda3-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0bda3-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0bda3-123">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="0bda3-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0bda3-124">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0bda3-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0bda3-125">**Versions du .NET framework :** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="0bda3-125">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0bda3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bda3-126">See also</span></span>
- <xref:System._AppDomain>
- <xref:System.AppDomain>
- [<span data-ttu-id="0bda3-127">ICorRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="0bda3-127">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
