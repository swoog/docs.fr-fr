---
title: CorRuntimeHost, coclasse
ms.date: 03/30/2017
api_name:
- CorRuntimeHost Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorRuntimeHost
helpviewer_keywords:
- CoRuntimeHost coclass [.NET Framework hosting]
ms.assetid: 5833740b-7d67-44b4-865c-b5bf45e291e3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7c81a39acee31986421c810e2814a4f7e6c4d970
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54597526"
---
# <a name="corruntimehost-coclass"></a><span data-ttu-id="186a5-102">CorRuntimeHost, coclasse</span><span class="sxs-lookup"><span data-stu-id="186a5-102">CorRuntimeHost Coclass</span></span>
<span data-ttu-id="186a5-103">Fournit des interfaces pour la gestion des applications qui sont en cours d’exécution par le common language runtime.</span><span class="sxs-lookup"><span data-stu-id="186a5-103">Provides interfaces for managing applications that are being executed by the common language runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="186a5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="186a5-104">Syntax</span></span>  
  
```  
coclass CorRuntimeHost {  
    [default] interface ICorRuntimeHost;  
    interface IGCHost;  
    interface ICorConfiguration;  
    interface IValidator;  
    interface IDebuggerInfo;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="186a5-105">Interfaces</span><span class="sxs-lookup"><span data-stu-id="186a5-105">Interfaces</span></span>  
  
|<span data-ttu-id="186a5-106">Interface</span><span class="sxs-lookup"><span data-stu-id="186a5-106">Interface</span></span>|<span data-ttu-id="186a5-107">Description</span><span class="sxs-lookup"><span data-stu-id="186a5-107">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="186a5-108">ICorConfiguration, interface</span><span class="sxs-lookup"><span data-stu-id="186a5-108">ICorConfiguration Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md)|<span data-ttu-id="186a5-109">Fournit des méthodes pour configurer le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="186a5-109">Provides methods for configuring the common language runtime (CLR).</span></span>|  
|[<span data-ttu-id="186a5-110">ICorRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="186a5-110">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)|<span data-ttu-id="186a5-111">Fournit des méthodes qui permettent à l’hôte démarrer et arrêter le common language runtime explicitement, pour créer et configurer des domaines d’application, pour accéder au domaine par défaut et d’énumérer tous les domaines en cours d’exécution dans le processus.</span><span class="sxs-lookup"><span data-stu-id="186a5-111">Provides methods that enable the host to start and stop the common language runtime explicitly, to create and configure application domains, to access the default domain, and to enumerate all domains running in the process.</span></span>|  
|[<span data-ttu-id="186a5-112">IDebuggerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="186a5-112">IDebuggerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/idebuggerinfo-interface.md)|<span data-ttu-id="186a5-113">Fournit des méthodes pour obtenir des informations sur l’état des services de débogage.</span><span class="sxs-lookup"><span data-stu-id="186a5-113">Provides methods for obtaining information about the state of the debugging services.</span></span>|  
|[<span data-ttu-id="186a5-114">IGCHost, interface</span><span class="sxs-lookup"><span data-stu-id="186a5-114">IGCHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)|<span data-ttu-id="186a5-115">Fournit des méthodes pour obtenir des informations sur le système de garbage collection et contrôler certains aspects du garbage collection.</span><span class="sxs-lookup"><span data-stu-id="186a5-115">Provides methods for obtaining information about the garbage collection system and for controlling some aspects of garbage collection.</span></span>|  
|<span data-ttu-id="186a5-116">« IValidator »</span><span class="sxs-lookup"><span data-stu-id="186a5-116">"IValidator"</span></span>|<span data-ttu-id="186a5-117">Fournit des méthodes pour la validation d’images exécutables portables et des rapports détaillés d’erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="186a5-117">Provides methods for validation of portable executable images and detailed reporting of validation errors.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="186a5-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="186a5-118">Requirements</span></span>  
 <span data-ttu-id="186a5-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="186a5-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="186a5-120">**En-tête :** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="186a5-120">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="186a5-121">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="186a5-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="186a5-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="186a5-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="186a5-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="186a5-123">See also</span></span>
- [<span data-ttu-id="186a5-124">Coclasses d’hébergement</span><span class="sxs-lookup"><span data-stu-id="186a5-124">Hosting Coclasses</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-coclasses.md)
