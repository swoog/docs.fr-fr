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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59169856"
---
# <a name="iclrappdomainresourcemonitorgetcurrentcputime-method"></a>ICLRAppDomainResourceMonitor::GetCurrentCpuTime, méthode
Obtient le temps processeur total utilisé par tous les threads lors de l’exécution dans le domaine d’application actuel, dans la mesure où le domaine d’application a été créé.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetCurrentCpuTime([in]  DWORD dwAppDomainId,  
                          [out] ULONGLONG* pMilliseconds);  
```  
  
## <a name="parameters"></a>Paramètres  
 `dwAppDomainId`  
 [in] L’ID du domaine d’application demandée.  
  
 `pMilliseconds`  
 [out] Pointeur vers le temps processeur total utilisé par tous les threads lors de l’exécution dans le domaine d’application actuel dans la mesure où le domaine d’application a été créé. Ce paramètre peut être `null`.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|La commande s'est correctement terminée.|  
|COR_E_APPDOMAINUNLOADED|Le domaine d’application a été déchargé ou n’existe pas.|  
|E_FAIL|L’analyse de ressource de domaine d’application n’est pas activée.<br /><br /> - ou -<br /><br /> Tous les autres défaillances.|  
  
## <a name="remarks"></a>Notes  
 Cette méthode est l’équivalent non managé de managé <xref:System.AppDomain.MonitoringTotalProcessorTime%2A?displayProperty=nameWithType> propriété.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MetaHost.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICLRAppDomainResourceMonitor, interface](../../../../docs/framework/unmanaged-api/hosting/iclrappdomainresourcemonitor-interface.md)
- [Interfaces d'hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [Analyse de ressource de domaine d'application](../../../../docs/standard/garbage-collection/app-domain-resource-monitoring.md)
- [Hébergement](../../../../docs/framework/unmanaged-api/hosting/index.md)
