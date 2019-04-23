---
title: ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList, méthode
ms.date: 03/30/2017
api_name:
- ICLRAssemblyReferenceList.IsStringAssemblyReferenceInList
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList
helpviewer_keywords:
- ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList method [.NET Framework hosting]
- IsStringAssemblyReferenceInList method [.NET Framework hosting]
ms.assetid: e6121cc3-2f11-42c7-bdae-47808581ff71
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: de17a91b5093372579a4d9435532a95406addd0a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59216897"
---
# <a name="iclrassemblyreferencelistisstringassemblyreferenceinlist-method"></a><span data-ttu-id="64d02-102">ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList, méthode</span><span class="sxs-lookup"><span data-stu-id="64d02-102">ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList Method</span></span>
<span data-ttu-id="64d02-103">Obtient une valeur qui indique si le nom fourni correspond au nom d’un assembly dans la liste.</span><span class="sxs-lookup"><span data-stu-id="64d02-103">Gets a value that indicates whether the supplied name matches the name of an assembly in the list.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64d02-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64d02-104">Syntax</span></span>  
  
```  
HRESULT IsStringAssemblyReferenceInList (  
    [in] LPCWSTR pwzAssemblyName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="64d02-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64d02-105">Parameters</span></span>  
 `pwzAssemblyName`  
 <span data-ttu-id="64d02-106">[in] Le nom de l’assembly à rechercher.</span><span class="sxs-lookup"><span data-stu-id="64d02-106">[in] The name of the assembly for which to search.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="64d02-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="64d02-107">Return Value</span></span>  
  
|<span data-ttu-id="64d02-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="64d02-108">HRESULT</span></span>|<span data-ttu-id="64d02-109">Description</span><span class="sxs-lookup"><span data-stu-id="64d02-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="64d02-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="64d02-110">S_OK</span></span>|<span data-ttu-id="64d02-111">La chaîne apparaît dans la liste.</span><span class="sxs-lookup"><span data-stu-id="64d02-111">The string appears in the list.</span></span>|  
|<span data-ttu-id="64d02-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="64d02-112">S_FALSE</span></span>|<span data-ttu-id="64d02-113">La chaîne n’apparaît pas dans la liste.</span><span class="sxs-lookup"><span data-stu-id="64d02-113">The string does not appear in the list.</span></span>|  
|<span data-ttu-id="64d02-114">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="64d02-114">E_FAIL</span></span>|<span data-ttu-id="64d02-115">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="64d02-115">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="64d02-116">Une fois une méthode retourne E_FAIL, le common language runtime n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="64d02-116">After a method returns E_FAIL, the common language runtime is no longer usable within the process.</span></span> <span data-ttu-id="64d02-117">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="64d02-117">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="64d02-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64d02-118">Requirements</span></span>  
 <span data-ttu-id="64d02-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="64d02-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="64d02-120">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="64d02-120">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="64d02-121">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="64d02-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="64d02-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="64d02-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="64d02-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64d02-123">See also</span></span>

- [<span data-ttu-id="64d02-124">ICLRAssemblyIdentityManager, interface</span><span class="sxs-lookup"><span data-stu-id="64d02-124">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="64d02-125">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="64d02-125">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="64d02-126">IHostAssemblyManager, interface</span><span class="sxs-lookup"><span data-stu-id="64d02-126">IHostAssemblyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)
- [<span data-ttu-id="64d02-127">IHostAssemblyStore, interface</span><span class="sxs-lookup"><span data-stu-id="64d02-127">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
