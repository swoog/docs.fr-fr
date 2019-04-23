---
title: ICLRAppDomainResourceMonitor::GetCurrentCpuTime, méthode
ms.date: 03/30/2017
api_name:
- ICLRAppDomainResourceMonitor.GetCurrentCpuTime
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAppDomainResourceMonitor::GetCurrentCpuTime
helpviewer_keywords:
- ICLRAppDomainResourceMonitor::GetCurrentCpuTime method [.NET Framework hosting]
- GetCurrentCpuTime method [.NET Framework hosting]
ms.assetid: ebc9cc33-fcd6-4cae-9ecb-ea21c51874e6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8022428c7f803f96e2fa150588edf95542bf19b3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59169856"
---
# <a name="iclrappdomainresourcemonitorgetcurrentcputime-method"></a><span data-ttu-id="0a634-102">ICLRAppDomainResourceMonitor::GetCurrentCpuTime, méthode</span><span class="sxs-lookup"><span data-stu-id="0a634-102">ICLRAppDomainResourceMonitor::GetCurrentCpuTime Method</span></span>
<span data-ttu-id="0a634-103">Obtient le temps processeur total utilisé par tous les threads lors de l’exécution dans le domaine d’application actuel, dans la mesure où le domaine d’application a été créé.</span><span class="sxs-lookup"><span data-stu-id="0a634-103">Gets the total processor time that has been used by all threads while executing in the current application domain, since the application domain was created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a634-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a634-104">Syntax</span></span>  
  
```  
HRESULT GetCurrentCpuTime([in]  DWORD dwAppDomainId,  
                          [out] ULONGLONG* pMilliseconds);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0a634-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a634-105">Parameters</span></span>  
 `dwAppDomainId`  
 <span data-ttu-id="0a634-106">[in] L’ID du domaine d’application demandée.</span><span class="sxs-lookup"><span data-stu-id="0a634-106">[in] The ID of the requested application domain.</span></span>  
  
 `pMilliseconds`  
 <span data-ttu-id="0a634-107">[out] Pointeur vers le temps processeur total utilisé par tous les threads lors de l’exécution dans le domaine d’application actuel dans la mesure où le domaine d’application a été créé.</span><span class="sxs-lookup"><span data-stu-id="0a634-107">[out] A pointer to the total processor time that has been used by all threads while executing in the current application domain since the application domain was created.</span></span> <span data-ttu-id="0a634-108">Ce paramètre peut être `null`.</span><span class="sxs-lookup"><span data-stu-id="0a634-108">This parameter can be `null`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0a634-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0a634-109">Return Value</span></span>  
  
|<span data-ttu-id="0a634-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="0a634-110">HRESULT</span></span>|<span data-ttu-id="0a634-111">Description</span><span class="sxs-lookup"><span data-stu-id="0a634-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0a634-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="0a634-112">S_OK</span></span>|<span data-ttu-id="0a634-113">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="0a634-113">The method completed successfully.</span></span>|  
|<span data-ttu-id="0a634-114">COR_E_APPDOMAINUNLOADED</span><span class="sxs-lookup"><span data-stu-id="0a634-114">COR_E_APPDOMAINUNLOADED</span></span>|<span data-ttu-id="0a634-115">Le domaine d’application a été déchargé ou n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="0a634-115">The application domain has been unloaded or does not exist.</span></span>|  
|<span data-ttu-id="0a634-116">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0a634-116">E_FAIL</span></span>|<span data-ttu-id="0a634-117">L’analyse de ressource de domaine d’application n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="0a634-117">Application domain resource monitoring is not enabled.</span></span><br /><br /> <span data-ttu-id="0a634-118">- ou -</span><span class="sxs-lookup"><span data-stu-id="0a634-118">-or-</span></span><br /><br /> <span data-ttu-id="0a634-119">Tous les autres défaillances.</span><span class="sxs-lookup"><span data-stu-id="0a634-119">All other failures.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0a634-120">Notes</span><span class="sxs-lookup"><span data-stu-id="0a634-120">Remarks</span></span>  
 <span data-ttu-id="0a634-121">Cette méthode est l’équivalent non managé de managé <xref:System.AppDomain.MonitoringTotalProcessorTime%2A?displayProperty=nameWithType> propriété.</span><span class="sxs-lookup"><span data-stu-id="0a634-121">This method is the unmanaged equivalent of the managed <xref:System.AppDomain.MonitoringTotalProcessorTime%2A?displayProperty=nameWithType> property.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0a634-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a634-122">Requirements</span></span>  
 <span data-ttu-id="0a634-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0a634-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0a634-124">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="0a634-124">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="0a634-125">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0a634-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0a634-126">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0a634-126">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0a634-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a634-127">See also</span></span>

- [<span data-ttu-id="0a634-128">ICLRAppDomainResourceMonitor, interface</span><span class="sxs-lookup"><span data-stu-id="0a634-128">ICLRAppDomainResourceMonitor Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrappdomainresourcemonitor-interface.md)
- [<span data-ttu-id="0a634-129">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="0a634-129">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="0a634-130">Analyse de ressource de domaine d'application</span><span class="sxs-lookup"><span data-stu-id="0a634-130">Application Domain Resource Monitoring</span></span>](../../../../docs/standard/garbage-collection/app-domain-resource-monitoring.md)
- [<span data-ttu-id="0a634-131">Hébergement</span><span class="sxs-lookup"><span data-stu-id="0a634-131">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
