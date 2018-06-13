---
title: ICLRErrorReportingManager, interface
ms.date: 03/30/2017
api_name:
- ICLRErrorReportingManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRErrorReportingManager
helpviewer_keywords:
- ICLRErrorReportingManager interface [.NET Framework hosting]
ms.assetid: ea8af0d5-4133-4472-8a1f-50570d7e85fa
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bf9e04ed1d3a68fed120c4c13ad992af1f777244
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33433794"
---
# <a name="iclrerrorreportingmanager-interface"></a><span data-ttu-id="e5466-102">ICLRErrorReportingManager, interface</span><span class="sxs-lookup"><span data-stu-id="e5466-102">ICLRErrorReportingManager Interface</span></span>
<span data-ttu-id="e5466-103">Fournit des méthodes qui permettent à l’hôte configurer des vidages de pile personnalisé pour le rapport d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="e5466-103">Provides methods that allow the host to configure custom stack dumps for error reporting.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e5466-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e5466-104">Methods</span></span>  
  
|<span data-ttu-id="e5466-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="e5466-105">Method</span></span>|<span data-ttu-id="e5466-106">Description</span><span class="sxs-lookup"><span data-stu-id="e5466-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e5466-107">BeginCustomDump, méthode</span><span class="sxs-lookup"><span data-stu-id="e5466-107">BeginCustomDump Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-begincustomdump-method.md)|<span data-ttu-id="e5466-108">Spécifie la configuration de vidages de pile personnalisé pour le rapport d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="e5466-108">Specifies the configuration of custom stack dumps for error reporting.</span></span>|  
|[<span data-ttu-id="e5466-109">EndCustomDump, méthode</span><span class="sxs-lookup"><span data-stu-id="e5466-109">EndCustomDump Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-endcustomdump-method.md)|<span data-ttu-id="e5466-110">Efface la configuration du vidage de pile personnalisée qui a été définie par un appel précédent à `BeginCustomDump`.</span><span class="sxs-lookup"><span data-stu-id="e5466-110">Clears the custom stack dump configuration that was set by an earlier call to `BeginCustomDump`.</span></span>|  
|[<span data-ttu-id="e5466-111">GetBucketParametersForCurrentException, méthode</span><span class="sxs-lookup"><span data-stu-id="e5466-111">GetBucketParametersForCurrentException Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-getbucketparametersforcurrentexception-method.md)|<span data-ttu-id="e5466-112">Obtient le compartiment Watson de l’exception actuelle sur le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="e5466-112">Gets the Watson bucket for the current exception on the calling thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e5466-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e5466-113">Remarks</span></span>  
 <span data-ttu-id="e5466-114">Le `BeginCustomDump` méthode définit la configuration de vidage de pile personnalisée.</span><span class="sxs-lookup"><span data-stu-id="e5466-114">The `BeginCustomDump` method sets custom stack dump configuration.</span></span> <span data-ttu-id="e5466-115">Le `EndCustomDump` méthode efface la configuration de vidage de pile personnalisée et libère tout état associé.</span><span class="sxs-lookup"><span data-stu-id="e5466-115">The `EndCustomDump` method clears the custom stack dump configuration and frees any associated state.</span></span> <span data-ttu-id="e5466-116">Il doit être appelée une fois que le dump personnalisé est terminé.</span><span class="sxs-lookup"><span data-stu-id="e5466-116">It should be called after the custom dump is complete.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="e5466-117">Échec d’appel `EndCustomDump` provoque une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e5466-117">Failure to call `EndCustomDump` causes memory to leak.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e5466-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e5466-118">Requirements</span></span>  
 <span data-ttu-id="e5466-119">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e5466-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5466-120">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e5466-120">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e5466-121">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e5466-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e5466-122">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e5466-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5466-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5466-123">See Also</span></span>  
 [<span data-ttu-id="e5466-124">ECustomDumpItemKind, énumération</span><span class="sxs-lookup"><span data-stu-id="e5466-124">ECustomDumpItemKind Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpitemkind-enumeration.md)  
 [<span data-ttu-id="e5466-125">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="e5466-125">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
