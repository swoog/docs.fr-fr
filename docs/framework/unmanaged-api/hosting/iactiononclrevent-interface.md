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
ms.openlocfilehash: 864a8a4dd9f96da2fd0e0025848a910b4f8b0a70
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61985528"
---
# <a name="iactiononclrevent-interface"></a><span data-ttu-id="fc748-102">IActionOnCLREvent, interface</span><span class="sxs-lookup"><span data-stu-id="fc748-102">IActionOnCLREvent Interface</span></span>
<span data-ttu-id="fc748-103">Fournit le [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) (méthode), qui exécute des rappels sur les événements qui ont été enregistrés à l’aide d’un appel à la [ICLROnEventManager::RegisterActionOnEvent](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-registeractiononevent-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="fc748-103">Provides the [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) method, which performs callbacks on events that have been registered by using a call to the [ICLROnEventManager::RegisterActionOnEvent](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-registeractiononevent-method.md) method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="fc748-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fc748-104">Methods</span></span>  
  
|<span data-ttu-id="fc748-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="fc748-105">Method</span></span>|<span data-ttu-id="fc748-106">Description</span><span class="sxs-lookup"><span data-stu-id="fc748-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="fc748-107">OnEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="fc748-107">OnEvent Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md)|<span data-ttu-id="fc748-108">Exécute un rappel pour un événement enregistré.</span><span class="sxs-lookup"><span data-stu-id="fc748-108">Performs a callback for a registered event.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fc748-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc748-109">Requirements</span></span>  
 <span data-ttu-id="fc748-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fc748-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fc748-111">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="fc748-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fc748-112">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fc748-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fc748-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fc748-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fc748-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc748-114">See also</span></span>

- [<span data-ttu-id="fc748-115">EClrEvent, énumération</span><span class="sxs-lookup"><span data-stu-id="fc748-115">EClrEvent Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md)
- [<span data-ttu-id="fc748-116">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="fc748-116">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
- [<span data-ttu-id="fc748-117">ICLROnEventManager, interface</span><span class="sxs-lookup"><span data-stu-id="fc748-117">ICLROnEventManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-interface.md)
- [<span data-ttu-id="fc748-118">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="fc748-118">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
