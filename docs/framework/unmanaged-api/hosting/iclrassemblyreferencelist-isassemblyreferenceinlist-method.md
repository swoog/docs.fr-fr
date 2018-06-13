---
title: ICLRAssemblyReferenceList::IsAssemblyReferenceInList, méthode
ms.date: 03/30/2017
api_name:
- ICLRAssemblyReferenceList.IsAssemblyReferenceInList
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyReferenceList::IsAssemblyReferenceInList
helpviewer_keywords:
- ICLRAssemblyReferenceList::IsAssemblyReferenceInList method [.NET Framework hosting]
- IsAssemblyReferenceInList method [.NET Framework hosting]
ms.assetid: 8a570813-21be-407e-92a6-7ae8de3bc728
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0b7eeadd532e5a53c693cc1cde59150777d7edc2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33433865"
---
# <a name="iclrassemblyreferencelistisassemblyreferenceinlist-method"></a><span data-ttu-id="1ae73-102">ICLRAssemblyReferenceList::IsAssemblyReferenceInList, méthode</span><span class="sxs-lookup"><span data-stu-id="1ae73-102">ICLRAssemblyReferenceList::IsAssemblyReferenceInList Method</span></span>
<span data-ttu-id="1ae73-103">Obtient une valeur qui indique si le pointeur fourni fait référence à un assembly dans la liste.</span><span class="sxs-lookup"><span data-stu-id="1ae73-103">Gets a value that indicates whether the supplied pointer refers to an assembly in the list.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ae73-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ae73-104">Syntax</span></span>  
  
```  
HRESULT IsAssemblyReferenceInList (  
    [in] IUnknown *pName  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1ae73-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ae73-105">Parameters</span></span>  
 `pName`  
 <span data-ttu-id="1ae73-106">[in] Un pointeur d’interface à l’assembly à rechercher.</span><span class="sxs-lookup"><span data-stu-id="1ae73-106">[in] An interface pointer to the assembly for which to search.</span></span> <span data-ttu-id="1ae73-107">Les valeurs valides sont de type `IAssemblyName` ou `IReferenceIdentity`.</span><span class="sxs-lookup"><span data-stu-id="1ae73-107">Valid values are of type `IAssemblyName` or `IReferenceIdentity`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1ae73-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1ae73-108">Return Value</span></span>  
  
|<span data-ttu-id="1ae73-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1ae73-109">HRESULT</span></span>|<span data-ttu-id="1ae73-110">Description</span><span class="sxs-lookup"><span data-stu-id="1ae73-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1ae73-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ae73-111">S_OK</span></span>|<span data-ttu-id="1ae73-112">La chaîne apparaît dans la liste.</span><span class="sxs-lookup"><span data-stu-id="1ae73-112">The string appears in the list.</span></span>|  
|<span data-ttu-id="1ae73-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="1ae73-113">S_FALSE</span></span>|<span data-ttu-id="1ae73-114">La chaîne n’apparaît pas dans la liste.</span><span class="sxs-lookup"><span data-stu-id="1ae73-114">The string does not appear in the list.</span></span>|  
|<span data-ttu-id="1ae73-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="1ae73-115">E_FAIL</span></span>|<span data-ttu-id="1ae73-116">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1ae73-116">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="1ae73-117">Une fois une méthode retourne E_FAIL, le common language runtime n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="1ae73-117">After a method returns E_FAIL, the common language runtime is no longer usable within the process.</span></span> <span data-ttu-id="1ae73-118">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="1ae73-118">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1ae73-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1ae73-119">Requirements</span></span>  
 <span data-ttu-id="1ae73-120">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1ae73-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1ae73-121">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="1ae73-121">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1ae73-122">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1ae73-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1ae73-123">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1ae73-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1ae73-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ae73-124">See Also</span></span>  
 [<span data-ttu-id="1ae73-125">ICLRAssemblyIdentityManager, interface</span><span class="sxs-lookup"><span data-stu-id="1ae73-125">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)  
 [<span data-ttu-id="1ae73-126">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="1ae73-126">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)  
 [<span data-ttu-id="1ae73-127">IHostAssemblyManager, interface</span><span class="sxs-lookup"><span data-stu-id="1ae73-127">IHostAssemblyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)  
 [<span data-ttu-id="1ae73-128">IHostAssemblyStore, interface</span><span class="sxs-lookup"><span data-stu-id="1ae73-128">IHostAssemblyStore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)
