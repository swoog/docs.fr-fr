---
title: ICorPublishAppDomainEnum, interface
ms.date: 03/30/2017
api_name:
- ICorPublishAppDomainEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishAppDomainEnum
helpviewer_keywords:
- ICorPublishAppDomainEnum interface [.NET Framework debugging]
ms.assetid: bb798c56-042e-475d-a245-b6fac36d0c07
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 610f62274aea88c1d5f9bbe1456685aa1d3bca68
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33423739"
---
# <a name="icorpublishappdomainenum-interface"></a><span data-ttu-id="d3859-102">ICorPublishAppDomainEnum, interface</span><span class="sxs-lookup"><span data-stu-id="d3859-102">ICorPublishAppDomainEnum Interface</span></span>
<span data-ttu-id="d3859-103">Une sous-classe de la [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md) interface qui fournit des méthodes pour parcourir une collection de [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md) les objets qui existent actuellement dans un processus.</span><span class="sxs-lookup"><span data-stu-id="d3859-103">A subclass of the [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md) interface that provides methods to traverse a collection of [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md) objects that currently exist within a process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d3859-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d3859-104">Methods</span></span>  
  
|<span data-ttu-id="d3859-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="d3859-105">Method</span></span>|<span data-ttu-id="d3859-106">Description</span><span class="sxs-lookup"><span data-stu-id="d3859-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d3859-107">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="d3859-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-next-method.md)|<span data-ttu-id="d3859-108">Obtient le nombre spécifié de `ICorPublishAppDomain` les instances de la collection, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="d3859-108">Gets the specified number of `ICorPublishAppDomain` instances from the collection, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d3859-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d3859-109">Remarks</span></span>  
 <span data-ttu-id="d3859-110">Le `ICorPublishAppDomainEnum` interface implémente les méthodes de l’interface abstraite [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md).</span><span class="sxs-lookup"><span data-stu-id="d3859-110">The `ICorPublishAppDomainEnum` interface implements the methods of the abstract interface, [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d3859-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d3859-111">Requirements</span></span>  
 <span data-ttu-id="d3859-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d3859-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d3859-113">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="d3859-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="d3859-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d3859-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d3859-115">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d3859-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d3859-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3859-116">See Also</span></span>  
 [<span data-ttu-id="d3859-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d3859-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="d3859-118">CorpubPublish, coclasse</span><span class="sxs-lookup"><span data-stu-id="d3859-118">CorpubPublish Coclass</span></span>](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
