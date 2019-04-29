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
ms.openlocfilehash: 7486a094deab16ebbc05f19f1b652126479ce11c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61638578"
---
# <a name="iclroneventmanager-interface"></a><span data-ttu-id="e4d83-102">ICLROnEventManager, interface</span><span class="sxs-lookup"><span data-stu-id="e4d83-102">ICLROnEventManager Interface</span></span>
<span data-ttu-id="e4d83-103">Fournit des méthodes qui permettent à l’hôte inscrire et désinscrire des rappels pour les événements du common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="e4d83-103">Provides methods that allow the host to register and unregister callbacks for common language runtime (CLR) events.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e4d83-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e4d83-104">Methods</span></span>  
  
|<span data-ttu-id="e4d83-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="e4d83-105">Method</span></span>|<span data-ttu-id="e4d83-106">Description</span><span class="sxs-lookup"><span data-stu-id="e4d83-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e4d83-107">RegisterActionOnEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="e4d83-107">RegisterActionOnEvent Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-registeractiononevent-method.md)|<span data-ttu-id="e4d83-108">Enregistre un pointeur de rappel pour l’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="e4d83-108">Registers a callback pointer for the specified event.</span></span>|  
|[<span data-ttu-id="e4d83-109">UnregisterActionOnEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="e4d83-109">UnregisterActionOnEvent Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-unregisteractiononevent-method.md)|<span data-ttu-id="e4d83-110">Annule l’inscription d’un pointeur de rappel précédemment enregistré pour l’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="e4d83-110">Unregisters a previously registered callback pointer for the specified event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e4d83-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e4d83-111">Remarks</span></span>  
 <span data-ttu-id="e4d83-112">Pour inscrire et annuler l’inscription des rappels d’événement, l’hôte obtient une référence à `ICLROnEventManager` en appelant le [ICLRControl::GetCLRManager](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="e4d83-112">To register and unregister event callbacks, the host gets a reference to `ICLROnEventManager` by calling the [ICLRControl::GetCLRManager](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e4d83-113">Les événements décrits par [EClrEvent](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md) peut être déclenché plusieurs fois et à partir de threads différents pour signaler le déchargement ou la désactivation du CLR.</span><span class="sxs-lookup"><span data-stu-id="e4d83-113">The events described by [EClrEvent](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md) can be fired more than once and from different threads to signal an unload or the disabling of the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4d83-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4d83-114">Requirements</span></span>  
 <span data-ttu-id="e4d83-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e4d83-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4d83-116">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e4d83-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e4d83-117">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e4d83-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e4d83-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4d83-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4d83-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4d83-119">See also</span></span>

- [<span data-ttu-id="e4d83-120">EClrEvent, énumération</span><span class="sxs-lookup"><span data-stu-id="e4d83-120">EClrEvent Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md)
- [<span data-ttu-id="e4d83-121">IActionOnCLREvent, interface</span><span class="sxs-lookup"><span data-stu-id="e4d83-121">IActionOnCLREvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-interface.md)
- [<span data-ttu-id="e4d83-122">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="e4d83-122">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
- [<span data-ttu-id="e4d83-123">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="e4d83-123">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
