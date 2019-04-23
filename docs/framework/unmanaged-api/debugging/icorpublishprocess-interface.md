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
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59182960"
---
# <a name="icorpublishprocess-interface"></a><span data-ttu-id="4d207-102">ICorPublishProcess, interface</span><span class="sxs-lookup"><span data-stu-id="4d207-102">ICorPublishProcess Interface</span></span>
<span data-ttu-id="4d207-103">Fournit des méthodes qui accèdent aux informations à afficher sur un processus.</span><span class="sxs-lookup"><span data-stu-id="4d207-103">Provides methods that access information to be displayed about a process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4d207-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4d207-104">Methods</span></span>  
  
|<span data-ttu-id="4d207-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="4d207-105">Method</span></span>|<span data-ttu-id="4d207-106">Description</span><span class="sxs-lookup"><span data-stu-id="4d207-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4d207-107">EnumAppDomains, méthode</span><span class="sxs-lookup"><span data-stu-id="4d207-107">EnumAppDomains Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-enumappdomains-method.md)|<span data-ttu-id="4d207-108">Obtient un [ICorPublishAppDomainEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-interface.md) instance qui contient les domaines d’application dans le processus référencé par ce `ICorPublishProcess`.</span><span class="sxs-lookup"><span data-stu-id="4d207-108">Gets an [ICorPublishAppDomainEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-interface.md) instance that contains the application domains in the process referenced by this `ICorPublishProcess`.</span></span>|  
|[<span data-ttu-id="4d207-109">GetDisplayName, méthode</span><span class="sxs-lookup"><span data-stu-id="4d207-109">GetDisplayName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-getdisplayname-method.md)|<span data-ttu-id="4d207-110">Obtient le chemin d’accès complet du fichier exécutable pour le processus référencé par ce `ICorPublishProcess`.</span><span class="sxs-lookup"><span data-stu-id="4d207-110">Gets the full path of the executable for the process referenced by this `ICorPublishProcess`.</span></span>|  
|[<span data-ttu-id="4d207-111">GetProcessID, méthode</span><span class="sxs-lookup"><span data-stu-id="4d207-111">GetProcessID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-getprocessid-method.md)|<span data-ttu-id="4d207-112">Obtient l’identificateur de système d’exploitation pour le processus référencé par ce `ICorPublishProcess`.</span><span class="sxs-lookup"><span data-stu-id="4d207-112">Gets the operating system identifier for the process referenced by this `ICorPublishProcess`.</span></span>|  
|[<span data-ttu-id="4d207-113">IsManaged, méthode</span><span class="sxs-lookup"><span data-stu-id="4d207-113">IsManaged Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-ismanaged-method.md)|<span data-ttu-id="4d207-114">Obtient une valeur qui indique si le processus référencé par ce `ICorPublishProcess` est connu pour être en cours d’exécution du code managé.</span><span class="sxs-lookup"><span data-stu-id="4d207-114">Gets a value that indicates whether the process referenced by this `ICorPublishProcess` is known to be running managed code.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="4d207-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d207-115">Requirements</span></span>  
 <span data-ttu-id="4d207-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4d207-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4d207-117">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="4d207-117">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="4d207-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4d207-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4d207-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4d207-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4d207-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d207-120">See also</span></span>

- [<span data-ttu-id="4d207-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="4d207-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="4d207-122">CorpubPublish, coclasse</span><span class="sxs-lookup"><span data-stu-id="4d207-122">CorpubPublish Coclass</span></span>](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
