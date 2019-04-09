---
title: IHostAssemblyStore, interface
ms.date: 03/30/2017
api_name:
- IHostAssemblyStore
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAssemblyStore
helpviewer_keywords:
- IHostAssemblyStore interface [.NET Framework hosting]
ms.assetid: cccb650f-abe0-41e2-9fd1-b383788eb1f6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d4067c1fbcf99c903c892eaec58262d95569114b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59173418"
---
# <a name="ihostassemblystore-interface"></a><span data-ttu-id="a6be3-102">IHostAssemblyStore, interface</span><span class="sxs-lookup"><span data-stu-id="a6be3-102">IHostAssemblyStore Interface</span></span>
<span data-ttu-id="a6be3-103">Fournit des méthodes qui permettent à un hôte charger des assemblys et des modules indépendamment le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="a6be3-103">Provides methods that allow a host to load assemblies and modules independently of the common language runtime (CLR).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a6be3-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a6be3-104">Methods</span></span>  
  
|<span data-ttu-id="a6be3-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="a6be3-105">Method</span></span>|<span data-ttu-id="a6be3-106">Description</span><span class="sxs-lookup"><span data-stu-id="a6be3-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a6be3-107">ProvideAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="a6be3-107">ProvideAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-provideassembly-method.md)|<span data-ttu-id="a6be3-108">Obtient une référence à un assembly qui n’est pas référencé par le [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) retourné par un appel à [IHostAssemblyManager::GetNonHostStoreAssemblies](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-getnonhoststoreassemblies-method.md).</span><span class="sxs-lookup"><span data-stu-id="a6be3-108">Gets a reference to an assembly that is not referenced by the [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) returned from a call to [IHostAssemblyManager::GetNonHostStoreAssemblies](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-getnonhoststoreassemblies-method.md).</span></span>|  
|[<span data-ttu-id="a6be3-109">ProvideModule, méthode</span><span class="sxs-lookup"><span data-stu-id="a6be3-109">ProvideModule Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-providemodule-method.md)|<span data-ttu-id="a6be3-110">Résout un module dans un assembly ou un fichier de ressources (non incorporé) lié.</span><span class="sxs-lookup"><span data-stu-id="a6be3-110">Resolves a module within an assembly or a linked (not embedded) resource file.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a6be3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a6be3-111">Remarks</span></span>  
 `IHostAssemblyStore` <span data-ttu-id="a6be3-112">fournit un moyen pour un hôte de charger des assemblys efficacement en fonction de l’identité d’assembly.</span><span class="sxs-lookup"><span data-stu-id="a6be3-112">provides a way for a host to load assemblies efficiently based on assembly identity.</span></span> <span data-ttu-id="a6be3-113">L’hôte charge les assemblys en retournant `IStream` instances qui pointent directement vers les octets.</span><span class="sxs-lookup"><span data-stu-id="a6be3-113">The host loads assemblies by returning `IStream` instances that point directly at the bytes.</span></span>  
  
 <span data-ttu-id="a6be3-114">Le CLR détermine si un hôte a implémenté `IHostAssemblyStore` en appelant `IHostAssemblyManager::GetNonHostAssemblyStores` lors de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="a6be3-114">The CLR determines whether a host has implemented `IHostAssemblyStore` by calling `IHostAssemblyManager::GetNonHostAssemblyStores` upon initialization.</span></span> <span data-ttu-id="a6be3-115">Cela permet à l’hôte, par exemple, pour contrôler la liaison aux assemblys d’utilisateur, mais s’appuyer sur le runtime pour la liaison aux assemblys .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a6be3-115">This allows the host, for example, to control binding to user assemblies, but to rely on the runtime to bind to .NET Framework assemblies.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a6be3-116">Fournir une implémentation de `IHostAssemblyStore`, l’hôte spécifie son intention de résoudre tous les assemblys qui ne sont pas référencés par le `ICLRAssemblyReferenceList` retourné à partir de `IHostAssemblyManager::GetNonHostStoreAssemblies`.</span><span class="sxs-lookup"><span data-stu-id="a6be3-116">In providing an implementation of `IHostAssemblyStore`, the host specifies its intent to resolve all assemblies that are not referenced by the `ICLRAssemblyReferenceList` returned from `IHostAssemblyManager::GetNonHostStoreAssemblies`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a6be3-117">La version 2.0 du .NET Framework ne fournit pas un moyen pour l’hôte de charger l’image native d’un assembly, tel que fourni par le [Native Image Generator (Ngen.exe)](../../../../docs/framework/tools/ngen-exe-native-image-generator.md) utilitaire.</span><span class="sxs-lookup"><span data-stu-id="a6be3-117">The .NET Framework version 2.0 does not provide a way for the host to load the native image of an assembly, as provided by the [Native Image Generator (Ngen.exe)](../../../../docs/framework/tools/ngen-exe-native-image-generator.md) utility.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a6be3-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6be3-118">Requirements</span></span>  
 <span data-ttu-id="a6be3-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a6be3-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a6be3-120">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a6be3-120">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a6be3-121">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a6be3-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="a6be3-122">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="a6be3-122">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="a6be3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6be3-123">See also</span></span>

- [<span data-ttu-id="a6be3-124">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="a6be3-124">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="a6be3-125">IHostAssemblyManager, interface</span><span class="sxs-lookup"><span data-stu-id="a6be3-125">IHostAssemblyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)
- [<span data-ttu-id="a6be3-126">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="a6be3-126">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
