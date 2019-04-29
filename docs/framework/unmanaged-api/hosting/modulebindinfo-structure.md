---
title: ModuleBindInfo, structure
ms.date: 03/30/2017
api_name:
- ModuleBindInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ModuleBindInfo
helpviewer_keywords:
- ModuleBindInfo structure [.NET Framework hosting]
ms.assetid: 632d4adc-dbc9-4ce8-9397-abc3285c1c69
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f14d3dcaad1cc8cac11599b1647d61df3a793301
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61765178"
---
# <a name="modulebindinfo-structure"></a><span data-ttu-id="37ebc-102">ModuleBindInfo, structure</span><span class="sxs-lookup"><span data-stu-id="37ebc-102">ModuleBindInfo Structure</span></span>
<span data-ttu-id="37ebc-103">Fournit des informations détaillées sur le module référencé et l’assembly qui le contient.</span><span class="sxs-lookup"><span data-stu-id="37ebc-103">Provides detailed information about the referenced module and the assembly that contains it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="37ebc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37ebc-104">Syntax</span></span>  
  
```  
typedef struct _ModuleBindInfo {  
    DWORD    dwAppDomainId;  
    LPCWSTR  lpAssemblyIdentity;  
    LPCWSTR  lpModuleName  
} ModuleBindInfo;  
```  
  
## <a name="members"></a><span data-ttu-id="37ebc-105">Membres</span><span class="sxs-lookup"><span data-stu-id="37ebc-105">Members</span></span>  
  
|<span data-ttu-id="37ebc-106">Membre</span><span class="sxs-lookup"><span data-stu-id="37ebc-106">Member</span></span>|<span data-ttu-id="37ebc-107">Description</span><span class="sxs-lookup"><span data-stu-id="37ebc-107">Description</span></span>|  
|------------|-----------------|  
|`dwAppDomainId`|<span data-ttu-id="37ebc-108">Un identificateur unique pour le `IStream` qui est retourné par un appel à la [IHostAssemblyStore::ProvideModule](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-providemodule-method.md) (méthode) à partir duquel le module référencé doit être chargé.</span><span class="sxs-lookup"><span data-stu-id="37ebc-108">A unique identifier for the `IStream` that is returned by a call to the [IHostAssemblyStore::ProvideModule](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-providemodule-method.md) method from which the referenced module is to be loaded.</span></span>|  
|`lpAssemblyIdentity`|<span data-ttu-id="37ebc-109">Un identificateur unique pour l’assembly qui contient le module référencé.</span><span class="sxs-lookup"><span data-stu-id="37ebc-109">A unique identifier for the assembly that contains the referenced module.</span></span>|  
|`lpModuleName`|<span data-ttu-id="37ebc-110">Le nom du module référencé.</span><span class="sxs-lookup"><span data-stu-id="37ebc-110">The name of the referenced module.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="37ebc-111">Notes</span><span class="sxs-lookup"><span data-stu-id="37ebc-111">Remarks</span></span>  
 <span data-ttu-id="37ebc-112">`ModuleBindInfo` est passé en tant que paramètre à `IHostAssemblyStore::ProvideModule`.</span><span class="sxs-lookup"><span data-stu-id="37ebc-112">`ModuleBindInfo` is passed as a parameter to `IHostAssemblyStore::ProvideModule`.</span></span> <span data-ttu-id="37ebc-113">L’hôte fournit l’identificateur unique `dwAppDomainId` pour le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="37ebc-113">The host supplies the unique identifier `dwAppDomainId` to the common language runtime (CLR).</span></span> <span data-ttu-id="37ebc-114">Après un appel à la [IHostAssemblyStore::ProvideAssembly](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-provideassembly-method.md) méthode est retournée, le runtime utilise l’identificateur pour déterminer si le contenu de la `IStream` ont été mappés.</span><span class="sxs-lookup"><span data-stu-id="37ebc-114">After a call to the [IHostAssemblyStore::ProvideAssembly](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-provideassembly-method.md) method returns, the runtime uses the identifier to determine whether the contents of the `IStream` have been mapped.</span></span> <span data-ttu-id="37ebc-115">Dans ce cas, le runtime charge la copie existante plutôt que de remapper le flux.</span><span class="sxs-lookup"><span data-stu-id="37ebc-115">If so, the runtime loads the existing copy rather than remapping the stream.</span></span> <span data-ttu-id="37ebc-116">Le runtime utilise également cet identificateur en tant que clé de recherche pour les flux qui sont retournées à partir des appels à la `IHostAssemblyStore::ProvideAssembly` (méthode).</span><span class="sxs-lookup"><span data-stu-id="37ebc-116">The runtime also uses this identifier as a lookup key for streams that are returned from calls to the `IHostAssemblyStore::ProvideAssembly` method.</span></span> <span data-ttu-id="37ebc-117">Par conséquent, l’identificateur doit être unique pour les demandes de module, ainsi que pour les demandes de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="37ebc-117">Therefore, the identifier must be unique for module requests as well as for assembly requests.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="37ebc-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37ebc-118">Requirements</span></span>  
 <span data-ttu-id="37ebc-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="37ebc-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="37ebc-120">**En-tête :** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="37ebc-120">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="37ebc-121">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="37ebc-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="37ebc-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="37ebc-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37ebc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37ebc-123">See also</span></span>

- [<span data-ttu-id="37ebc-124">Structures d’hébergement</span><span class="sxs-lookup"><span data-stu-id="37ebc-124">Hosting Structures</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)
- [<span data-ttu-id="37ebc-125">AssemblyBindInfo, structure</span><span class="sxs-lookup"><span data-stu-id="37ebc-125">AssemblyBindInfo Structure</span></span>](../../../../docs/framework/unmanaged-api/hosting/assemblybindinfo-structure.md)
- [<span data-ttu-id="37ebc-126">ICLRAssemblyIdentityManager, interface</span><span class="sxs-lookup"><span data-stu-id="37ebc-126">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="37ebc-127">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="37ebc-127">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="37ebc-128">IHostAssemblyManager, interface</span><span class="sxs-lookup"><span data-stu-id="37ebc-128">IHostAssemblyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)
