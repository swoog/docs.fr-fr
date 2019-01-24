---
title: IActionOnCLREvent, interface
ms.date: 03/30/2017
api_name:
- IActionOnCLREvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IActionOnCLREvent
helpviewer_keywords:
- IActionOnCLREvent interface [.NET Framework hosting]
ms.assetid: b5f9b41e-7301-429c-911f-21d5422292b3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0f547d1bafa37c2cbb285a5d55cef8e1a6e29d0a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54688244"
---
# <a name="iactiononclrevent-interface"></a><span data-ttu-id="55eca-102">IActionOnCLREvent, interface</span><span class="sxs-lookup"><span data-stu-id="55eca-102">IActionOnCLREvent Interface</span></span>
<span data-ttu-id="55eca-103">Fournit le [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) (méthode), qui exécute des rappels sur les événements qui ont été enregistrés à l’aide d’un appel à la [ICLROnEventManager::RegisterActionOnEvent](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-registeractiononevent-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="55eca-103">Provides the [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) method, which performs callbacks on events that have been registered by using a call to the [ICLROnEventManager::RegisterActionOnEvent](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-registeractiononevent-method.md) method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="55eca-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="55eca-104">Methods</span></span>  
  
|<span data-ttu-id="55eca-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="55eca-105">Method</span></span>|<span data-ttu-id="55eca-106">Description</span><span class="sxs-lookup"><span data-stu-id="55eca-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="55eca-107">OnEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="55eca-107">OnEvent Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md)|<span data-ttu-id="55eca-108">Exécute un rappel pour un événement enregistré.</span><span class="sxs-lookup"><span data-stu-id="55eca-108">Performs a callback for a registered event.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="55eca-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="55eca-109">Requirements</span></span>  
 <span data-ttu-id="55eca-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="55eca-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="55eca-111">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="55eca-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="55eca-112">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="55eca-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="55eca-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="55eca-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="55eca-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55eca-114">See also</span></span>
- [<span data-ttu-id="55eca-115">EClrEvent, énumération</span><span class="sxs-lookup"><span data-stu-id="55eca-115">EClrEvent Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md)
- [<span data-ttu-id="55eca-116">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="55eca-116">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
- [<span data-ttu-id="55eca-117">ICLROnEventManager, interface</span><span class="sxs-lookup"><span data-stu-id="55eca-117">ICLROnEventManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-interface.md)
- [<span data-ttu-id="55eca-118">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="55eca-118">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
