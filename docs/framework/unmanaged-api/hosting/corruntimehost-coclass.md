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
ms.openlocfilehash: b9b9b8a728932caa085bba1665dc97faf02be8fe
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33431378"
---
# <a name="corruntimehost-coclass"></a><span data-ttu-id="d8bd4-102">CorRuntimeHost, coclasse</span><span class="sxs-lookup"><span data-stu-id="d8bd4-102">CorRuntimeHost Coclass</span></span>
<span data-ttu-id="d8bd4-103">Fournit des interfaces de gestion des applications qui sont en cours d’exécution par le common language runtime.</span><span class="sxs-lookup"><span data-stu-id="d8bd4-103">Provides interfaces for managing applications that are being executed by the common language runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d8bd4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8bd4-104">Syntax</span></span>  
  
```  
coclass CorRuntimeHost {  
    [default] interface ICorRuntimeHost;  
    interface IGCHost;  
    interface ICorConfiguration;  
    interface IValidator;  
    interface IDebuggerInfo;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="d8bd4-105">Interfaces</span><span class="sxs-lookup"><span data-stu-id="d8bd4-105">Interfaces</span></span>  
  
|<span data-ttu-id="d8bd4-106">Interface</span><span class="sxs-lookup"><span data-stu-id="d8bd4-106">Interface</span></span>|<span data-ttu-id="d8bd4-107">Description</span><span class="sxs-lookup"><span data-stu-id="d8bd4-107">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="d8bd4-108">ICorConfiguration, interface</span><span class="sxs-lookup"><span data-stu-id="d8bd4-108">ICorConfiguration Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md)|<span data-ttu-id="d8bd4-109">Fournit des méthodes pour configurer le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="d8bd4-109">Provides methods for configuring the common language runtime (CLR).</span></span>|  
|[<span data-ttu-id="d8bd4-110">ICorRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="d8bd4-110">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)|<span data-ttu-id="d8bd4-111">Fournit des méthodes qui permettent à l’hôte démarrer et arrêter le common language runtime explicitement, pour créer et configurer des domaines d’application, pour accéder au domaine par défaut et d’énumérer tous les domaines en cours d’exécution dans le processus.</span><span class="sxs-lookup"><span data-stu-id="d8bd4-111">Provides methods that enable the host to start and stop the common language runtime explicitly, to create and configure application domains, to access the default domain, and to enumerate all domains running in the process.</span></span>|  
|[<span data-ttu-id="d8bd4-112">IDebuggerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="d8bd4-112">IDebuggerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/idebuggerinfo-interface.md)|<span data-ttu-id="d8bd4-113">Fournit des méthodes pour obtenir des informations sur l’état des services de débogage.</span><span class="sxs-lookup"><span data-stu-id="d8bd4-113">Provides methods for obtaining information about the state of the debugging services.</span></span>|  
|[<span data-ttu-id="d8bd4-114">IGCHost, interface</span><span class="sxs-lookup"><span data-stu-id="d8bd4-114">IGCHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)|<span data-ttu-id="d8bd4-115">Fournit des méthodes pour obtenir des informations sur le système de garbage collection et contrôler certains aspects du garbage collection.</span><span class="sxs-lookup"><span data-stu-id="d8bd4-115">Provides methods for obtaining information about the garbage collection system and for controlling some aspects of garbage collection.</span></span>|  
|<span data-ttu-id="d8bd4-116">« IValidator »</span><span class="sxs-lookup"><span data-stu-id="d8bd4-116">"IValidator"</span></span>|<span data-ttu-id="d8bd4-117">Fournit des méthodes pour la validation d’images exécutables portables et la génération de rapports détaillés des erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="d8bd4-117">Provides methods for validation of portable executable images and detailed reporting of validation errors.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d8bd4-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d8bd4-118">Requirements</span></span>  
 <span data-ttu-id="d8bd4-119">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d8bd4-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d8bd4-120">**En-tête :** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="d8bd4-120">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="d8bd4-121">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d8bd4-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d8bd4-122">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d8bd4-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d8bd4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8bd4-123">See Also</span></span>  
 [<span data-ttu-id="d8bd4-124">Coclasses d’hébergement</span><span class="sxs-lookup"><span data-stu-id="d8bd4-124">Hosting Coclasses</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-coclasses.md)
