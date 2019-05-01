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
ms.openlocfilehash: a20b79dd5eda9c431511cc49e7e3adaa9486b2aa
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61969829"
---
# <a name="iclrerrorreportingmanager-interface"></a><span data-ttu-id="6dcbc-102">ICLRErrorReportingManager, interface</span><span class="sxs-lookup"><span data-stu-id="6dcbc-102">ICLRErrorReportingManager Interface</span></span>
<span data-ttu-id="6dcbc-103">Fournit des méthodes qui permettent à l’hôte configurer des vidages de pile personnalisé pour le rapport d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-103">Provides methods that allow the host to configure custom stack dumps for error reporting.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="6dcbc-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6dcbc-104">Methods</span></span>  
  
|<span data-ttu-id="6dcbc-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="6dcbc-105">Method</span></span>|<span data-ttu-id="6dcbc-106">Description</span><span class="sxs-lookup"><span data-stu-id="6dcbc-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6dcbc-107">BeginCustomDump, méthode</span><span class="sxs-lookup"><span data-stu-id="6dcbc-107">BeginCustomDump Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-begincustomdump-method.md)|<span data-ttu-id="6dcbc-108">Spécifie la configuration de vidages de pile personnalisé pour le rapport d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-108">Specifies the configuration of custom stack dumps for error reporting.</span></span>|  
|[<span data-ttu-id="6dcbc-109">EndCustomDump, méthode</span><span class="sxs-lookup"><span data-stu-id="6dcbc-109">EndCustomDump Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-endcustomdump-method.md)|<span data-ttu-id="6dcbc-110">Efface la configuration du vidage de pile personnalisée qui a été définie par un appel antérieur à `BeginCustomDump`.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-110">Clears the custom stack dump configuration that was set by an earlier call to `BeginCustomDump`.</span></span>|  
|[<span data-ttu-id="6dcbc-111">GetBucketParametersForCurrentException, méthode</span><span class="sxs-lookup"><span data-stu-id="6dcbc-111">GetBucketParametersForCurrentException Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-getbucketparametersforcurrentexception-method.md)|<span data-ttu-id="6dcbc-112">Obtient le compartiment Watson pour l’exception actuelle sur le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-112">Gets the Watson bucket for the current exception on the calling thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6dcbc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6dcbc-113">Remarks</span></span>  
 <span data-ttu-id="6dcbc-114">Le `BeginCustomDump` méthode définit la configuration de vidage de pile personnalisé.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-114">The `BeginCustomDump` method sets custom stack dump configuration.</span></span> <span data-ttu-id="6dcbc-115">Le `EndCustomDump` méthode efface la configuration de vidage de pile personnalisée et libère tout état associé.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-115">The `EndCustomDump` method clears the custom stack dump configuration and frees any associated state.</span></span> <span data-ttu-id="6dcbc-116">Il doit être appelée une fois l’image personnalisée est terminée.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-116">It should be called after the custom dump is complete.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="6dcbc-117">Échec d’appel `EndCustomDump` entraîne une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="6dcbc-117">Failure to call `EndCustomDump` causes memory to leak.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6dcbc-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6dcbc-118">Requirements</span></span>  
 <span data-ttu-id="6dcbc-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6dcbc-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6dcbc-120">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="6dcbc-120">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6dcbc-121">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6dcbc-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6dcbc-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6dcbc-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6dcbc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6dcbc-123">See also</span></span>

- [<span data-ttu-id="6dcbc-124">ECustomDumpItemKind, énumération</span><span class="sxs-lookup"><span data-stu-id="6dcbc-124">ECustomDumpItemKind Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpitemkind-enumeration.md)
- [<span data-ttu-id="6dcbc-125">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="6dcbc-125">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
