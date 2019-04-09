---
title: IAssemblyCache, interface
ms.date: 03/30/2017
api_name:
- IAssemblyCache
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCache
helpviewer_keywords:
- IAssemblyCache interface [.NET Framework fusion]
ms.assetid: 71ea170f-872d-4fc5-81b6-27da1dec9b19
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9fc5f3a3d5bc5699a596bcc648a7153190c130f0
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59075630"
---
# <a name="iassemblycache-interface"></a><span data-ttu-id="f21a0-102">IAssemblyCache, interface</span><span class="sxs-lookup"><span data-stu-id="f21a0-102">IAssemblyCache Interface</span></span>
<span data-ttu-id="f21a0-103">Représente le global assembly cache pour une utilisation par la technologie de fusion.</span><span class="sxs-lookup"><span data-stu-id="f21a0-103">Represents the global assembly cache for use by the fusion technology.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f21a0-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f21a0-104">Methods</span></span>  
  
|<span data-ttu-id="f21a0-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="f21a0-105">Method</span></span>|<span data-ttu-id="f21a0-106">Description</span><span class="sxs-lookup"><span data-stu-id="f21a0-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f21a0-107">CreateAssemblyCacheItem, méthode</span><span class="sxs-lookup"><span data-stu-id="f21a0-107">CreateAssemblyCacheItem Method</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-createassemblycacheitem-method.md)|<span data-ttu-id="f21a0-108">Obtient une référence à un nouveau [IAssemblyCacheItem](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md).</span><span class="sxs-lookup"><span data-stu-id="f21a0-108">Gets a reference to a new [IAssemblyCacheItem](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md).</span></span>|  
|[<span data-ttu-id="f21a0-109">CreateAssemblyScavenger, méthode</span><span class="sxs-lookup"><span data-stu-id="f21a0-109">CreateAssemblyScavenger Method</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-createassemblyscavenger-method.md)|<span data-ttu-id="f21a0-110">Réservé à un usage interne par la technologie de fusion.</span><span class="sxs-lookup"><span data-stu-id="f21a0-110">Reserved for internal use by the fusion technology.</span></span>|  
|[<span data-ttu-id="f21a0-111">InstallAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="f21a0-111">InstallAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-installassembly-method.md)|<span data-ttu-id="f21a0-112">Installe l’assembly spécifié dans le global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="f21a0-112">Installs the specified assembly in the global assembly cache.</span></span>|  
|[<span data-ttu-id="f21a0-113">QueryAssemblyInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="f21a0-113">QueryAssemblyInfo Method</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-queryassemblyinfo-method.md)|<span data-ttu-id="f21a0-114">Obtient les données demandées sur l’assembly spécifié.</span><span class="sxs-lookup"><span data-stu-id="f21a0-114">Gets the requested data about the specified assembly.</span></span>|  
|[<span data-ttu-id="f21a0-115">UninstallAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="f21a0-115">UninstallAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-uninstallassembly-method.md)|<span data-ttu-id="f21a0-116">Désinstalle l’assembly spécifié du global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="f21a0-116">Uninstalls the specified assembly from the global assembly cache.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f21a0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f21a0-117">Requirements</span></span>  
 <span data-ttu-id="f21a0-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f21a0-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f21a0-119">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="f21a0-119">**Header:** Fusion.h</span></span>  
  
 **<span data-ttu-id="f21a0-120">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="f21a0-120">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="f21a0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f21a0-121">See also</span></span>

- [<span data-ttu-id="f21a0-122">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="f21a0-122">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [<span data-ttu-id="f21a0-123">Global Assembly Cache</span><span class="sxs-lookup"><span data-stu-id="f21a0-123">Global Assembly Cache</span></span>](../../../../docs/framework/app-domains/gac.md)
