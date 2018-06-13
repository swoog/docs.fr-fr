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
ms.openlocfilehash: ad7230731775cbc56dd0f1eaed72df19512d3733
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33432594"
---
# <a name="iclrassemblyreferencelistisstringassemblyreferenceinlist-method"></a><span data-ttu-id="44c13-102">ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList, méthode</span><span class="sxs-lookup"><span data-stu-id="44c13-102">ICLRAssemblyReferenceList::IsStringAssemblyReferenceInList Method</span></span>
<span data-ttu-id="44c13-103">Obtient une valeur qui indique si le nom fourni correspond au nom d’un assembly dans la liste.</span><span class="sxs-lookup"><span data-stu-id="44c13-103">Gets a value that indicates whether the supplied name matches the name of an assembly in the list.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="44c13-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44c13-104">Syntax</span></span>  
  
```  
HRESULT IsStringAssemblyReferenceInList (  
    [in] LPCWSTR pwzAssemblyName  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="44c13-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44c13-105">Parameters</span></span>  
 `pwzAssemblyName`  
 <span data-ttu-id="44c13-106">[in] Le nom de l’assembly à rechercher.</span><span class="sxs-lookup"><span data-stu-id="44c13-106">[in] The name of the assembly for which to search.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="44c13-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="44c13-107">Return Value</span></span>  
  
|<span data-ttu-id="44c13-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="44c13-108">HRESULT</span></span>|<span data-ttu-id="44c13-109">Description</span><span class="sxs-lookup"><span data-stu-id="44c13-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="44c13-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="44c13-110">S_OK</span></span>|<span data-ttu-id="44c13-111">La chaîne apparaît dans la liste.</span><span class="sxs-lookup"><span data-stu-id="44c13-111">The string appears in the list.</span></span>|  
|<span data-ttu-id="44c13-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="44c13-112">S_FALSE</span></span>|<span data-ttu-id="44c13-113">La chaîne n’apparaît pas dans la liste.</span><span class="sxs-lookup"><span data-stu-id="44c13-113">The string does not appear in the list.</span></span>|  
|<span data-ttu-id="44c13-114">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="44c13-114">E_FAIL</span></span>|<span data-ttu-id="44c13-115">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="44c13-115">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="44c13-116">Une fois une méthode retourne E_FAIL, le common language runtime n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="44c13-116">After a method returns E_FAIL, the common language runtime is no longer usable within the process.</span></span> <span data-ttu-id="44c13-117">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="44c13-117">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="44c13-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="44c13-118">Requirements</span></span>  
 <span data-ttu-id="44c13-119">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="44c13-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="44c13-120">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="44c13-120">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="44c13-121">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="44c13-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="44c13-122">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="44c13-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44c13-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44c13-123">See Also</span></span>  
 [<span data-ttu-id="44c13-124">ICLRAssemblyIdentityManager, interface</span><span class="sxs-lookup"><span data-stu-id="44c13-124">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)  
 [<span data-ttu-id="44c13-125">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="44c13-125">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)  
 [<span data-ttu-id="44c13-126">IHostAssemblyManager, interface</span><span class="sxs-lookup"><span data-stu-id="44c13-126">IHostAssemblyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)  
 [<span data-ttu-id="44c13-127">IHostAssemblyStore, interface</span><span class="sxs-lookup"><span data-stu-id="44c13-127">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
