---
title: ICLROnEventManager, interface
ms.date: 03/30/2017
api_name:
- ICLROnEventManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLROnEventManager
helpviewer_keywords:
- ICLROnEventManager interface [.NET Framework hosting]
ms.assetid: 9e15a0c1-8ab6-43d0-ae28-6ec7a4edd913
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c22dfa99d8069c060a525a9ae2cbef73d6625898
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33434101"
---
# <a name="iclroneventmanager-interface"></a><span data-ttu-id="a715b-102">ICLROnEventManager, interface</span><span class="sxs-lookup"><span data-stu-id="a715b-102">ICLROnEventManager Interface</span></span>
<span data-ttu-id="a715b-103">Fournit des méthodes qui permettent à l’hôte inscrire et désinscrire des rappels pour les événements du common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="a715b-103">Provides methods that allow the host to register and unregister callbacks for common language runtime (CLR) events.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a715b-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a715b-104">Methods</span></span>  
  
|<span data-ttu-id="a715b-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="a715b-105">Method</span></span>|<span data-ttu-id="a715b-106">Description</span><span class="sxs-lookup"><span data-stu-id="a715b-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a715b-107">RegisterActionOnEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="a715b-107">RegisterActionOnEvent Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-registeractiononevent-method.md)|<span data-ttu-id="a715b-108">Enregistre un pointeur de rappel pour l’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="a715b-108">Registers a callback pointer for the specified event.</span></span>|  
|[<span data-ttu-id="a715b-109">UnregisterActionOnEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="a715b-109">UnregisterActionOnEvent Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-unregisteractiononevent-method.md)|<span data-ttu-id="a715b-110">Annule l’inscription d’un pointeur de rappel précédemment enregistré pour l’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="a715b-110">Unregisters a previously registered callback pointer for the specified event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a715b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a715b-111">Remarks</span></span>  
 <span data-ttu-id="a715b-112">Pour enregistrer et annuler l’inscription du rappel d’événement, l’hôte obtient une référence à `ICLROnEventManager` en appelant le [ICLRControl::GetCLRManager](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="a715b-112">To register and unregister event callbacks, the host gets a reference to `ICLROnEventManager` by calling the [ICLRControl::GetCLRManager](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a715b-113">Les événements décrits par [EClrEvent](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md) peuvent être déclenchés plusieurs fois et à partir de threads différents pour signaler le déchargement ou la désactivation du CLR.</span><span class="sxs-lookup"><span data-stu-id="a715b-113">The events described by [EClrEvent](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md) can be fired more than once and from different threads to signal an unload or the disabling of the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a715b-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a715b-114">Requirements</span></span>  
 <span data-ttu-id="a715b-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a715b-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a715b-116">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a715b-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a715b-117">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a715b-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a715b-118">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a715b-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a715b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a715b-119">See Also</span></span>  
 [<span data-ttu-id="a715b-120">EClrEvent, énumération</span><span class="sxs-lookup"><span data-stu-id="a715b-120">EClrEvent Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md)  
 [<span data-ttu-id="a715b-121">IActionOnCLREvent, interface</span><span class="sxs-lookup"><span data-stu-id="a715b-121">IActionOnCLREvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-interface.md)  
 [<span data-ttu-id="a715b-122">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="a715b-122">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)  
 [<span data-ttu-id="a715b-123">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="a715b-123">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
