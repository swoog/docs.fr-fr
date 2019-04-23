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
ms.openlocfilehash: 2143fc13db1757ac2fa8a9c5a43f104a0c519ca0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59218561"
---
# <a name="corruntimehost-coclass"></a><span data-ttu-id="15715-102">CorRuntimeHost, coclasse</span><span class="sxs-lookup"><span data-stu-id="15715-102">CorRuntimeHost Coclass</span></span>
<span data-ttu-id="15715-103">Fournit des interfaces pour la gestion des applications qui sont en cours d’exécution par le common language runtime.</span><span class="sxs-lookup"><span data-stu-id="15715-103">Provides interfaces for managing applications that are being executed by the common language runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="15715-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15715-104">Syntax</span></span>  
  
```  
coclass CorRuntimeHost {  
    [default] interface ICorRuntimeHost;  
    interface IGCHost;  
    interface ICorConfiguration;  
    interface IValidator;  
    interface IDebuggerInfo;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="15715-105">Interfaces</span><span class="sxs-lookup"><span data-stu-id="15715-105">Interfaces</span></span>  
  
|<span data-ttu-id="15715-106">Interface</span><span class="sxs-lookup"><span data-stu-id="15715-106">Interface</span></span>|<span data-ttu-id="15715-107">Description</span><span class="sxs-lookup"><span data-stu-id="15715-107">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="15715-108">ICorConfiguration, interface</span><span class="sxs-lookup"><span data-stu-id="15715-108">ICorConfiguration Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md)|<span data-ttu-id="15715-109">Fournit des méthodes pour configurer le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="15715-109">Provides methods for configuring the common language runtime (CLR).</span></span>|  
|[<span data-ttu-id="15715-110">ICorRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="15715-110">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)|<span data-ttu-id="15715-111">Fournit des méthodes qui permettent à l’hôte démarrer et arrêter le common language runtime explicitement, pour créer et configurer des domaines d’application, pour accéder au domaine par défaut et d’énumérer tous les domaines en cours d’exécution dans le processus.</span><span class="sxs-lookup"><span data-stu-id="15715-111">Provides methods that enable the host to start and stop the common language runtime explicitly, to create and configure application domains, to access the default domain, and to enumerate all domains running in the process.</span></span>|  
|[<span data-ttu-id="15715-112">IDebuggerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="15715-112">IDebuggerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/idebuggerinfo-interface.md)|<span data-ttu-id="15715-113">Fournit des méthodes pour obtenir des informations sur l’état des services de débogage.</span><span class="sxs-lookup"><span data-stu-id="15715-113">Provides methods for obtaining information about the state of the debugging services.</span></span>|  
|[<span data-ttu-id="15715-114">IGCHost, interface</span><span class="sxs-lookup"><span data-stu-id="15715-114">IGCHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)|<span data-ttu-id="15715-115">Fournit des méthodes pour obtenir des informations sur le système de garbage collection et contrôler certains aspects du garbage collection.</span><span class="sxs-lookup"><span data-stu-id="15715-115">Provides methods for obtaining information about the garbage collection system and for controlling some aspects of garbage collection.</span></span>|  
|<span data-ttu-id="15715-116">« IValidator »</span><span class="sxs-lookup"><span data-stu-id="15715-116">"IValidator"</span></span>|<span data-ttu-id="15715-117">Fournit des méthodes pour la validation d’images exécutables portables et des rapports détaillés d’erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="15715-117">Provides methods for validation of portable executable images and detailed reporting of validation errors.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="15715-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15715-118">Requirements</span></span>  
 <span data-ttu-id="15715-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="15715-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="15715-120">**En-tête :** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="15715-120">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="15715-121">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="15715-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="15715-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="15715-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="15715-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15715-123">See also</span></span>

- [<span data-ttu-id="15715-124">Coclasses d’hébergement</span><span class="sxs-lookup"><span data-stu-id="15715-124">Hosting Coclasses</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-coclasses.md)
