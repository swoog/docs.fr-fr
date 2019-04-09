---
title: ICorPublishProcess, interface
ms.date: 03/30/2017
api_name:
- ICorPublishProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess
helpviewer_keywords:
- ICorPublishProcess interface [.NET Framework debugging]
ms.assetid: 6d1dc41b-8aa2-4889-bb00-1cbccc00c123
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 08dfa3ddbfd9cffdb0cb88d0325e5703a854668a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59182960"
---
# <a name="icorpublishprocess-interface"></a><span data-ttu-id="ab8bf-102">ICorPublishProcess, interface</span><span class="sxs-lookup"><span data-stu-id="ab8bf-102">ICorPublishProcess Interface</span></span>
<span data-ttu-id="ab8bf-103">Fournit des méthodes qui accèdent aux informations à afficher sur un processus.</span><span class="sxs-lookup"><span data-stu-id="ab8bf-103">Provides methods that access information to be displayed about a process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ab8bf-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ab8bf-104">Methods</span></span>  
  
|<span data-ttu-id="ab8bf-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="ab8bf-105">Method</span></span>|<span data-ttu-id="ab8bf-106">Description</span><span class="sxs-lookup"><span data-stu-id="ab8bf-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ab8bf-107">EnumAppDomains, méthode</span><span class="sxs-lookup"><span data-stu-id="ab8bf-107">EnumAppDomains Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-enumappdomains-method.md)|<span data-ttu-id="ab8bf-108">Obtient un [ICorPublishAppDomainEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-interface.md) instance qui contient les domaines d’application dans le processus référencé par ce `ICorPublishProcess`.</span><span class="sxs-lookup"><span data-stu-id="ab8bf-108">Gets an [ICorPublishAppDomainEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-interface.md) instance that contains the application domains in the process referenced by this `ICorPublishProcess`.</span></span>|  
|[<span data-ttu-id="ab8bf-109">GetDisplayName, méthode</span><span class="sxs-lookup"><span data-stu-id="ab8bf-109">GetDisplayName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-getdisplayname-method.md)|<span data-ttu-id="ab8bf-110">Obtient le chemin d’accès complet du fichier exécutable pour le processus référencé par ce `ICorPublishProcess`.</span><span class="sxs-lookup"><span data-stu-id="ab8bf-110">Gets the full path of the executable for the process referenced by this `ICorPublishProcess`.</span></span>|  
|[<span data-ttu-id="ab8bf-111">GetProcessID, méthode</span><span class="sxs-lookup"><span data-stu-id="ab8bf-111">GetProcessID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-getprocessid-method.md)|<span data-ttu-id="ab8bf-112">Obtient l’identificateur de système d’exploitation pour le processus référencé par ce `ICorPublishProcess`.</span><span class="sxs-lookup"><span data-stu-id="ab8bf-112">Gets the operating system identifier for the process referenced by this `ICorPublishProcess`.</span></span>|  
|[<span data-ttu-id="ab8bf-113">IsManaged, méthode</span><span class="sxs-lookup"><span data-stu-id="ab8bf-113">IsManaged Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-ismanaged-method.md)|<span data-ttu-id="ab8bf-114">Obtient une valeur qui indique si le processus référencé par ce `ICorPublishProcess` est connu pour être en cours d’exécution du code managé.</span><span class="sxs-lookup"><span data-stu-id="ab8bf-114">Gets a value that indicates whether the process referenced by this `ICorPublishProcess` is known to be running managed code.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ab8bf-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab8bf-115">Requirements</span></span>  
 <span data-ttu-id="ab8bf-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ab8bf-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ab8bf-117">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="ab8bf-117">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="ab8bf-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ab8bf-118">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="ab8bf-119">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="ab8bf-119">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="ab8bf-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab8bf-120">See also</span></span>

- [<span data-ttu-id="ab8bf-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="ab8bf-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="ab8bf-122">CorpubPublish (coclasse)</span><span class="sxs-lookup"><span data-stu-id="ab8bf-122">CorpubPublish Coclass</span></span>](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
