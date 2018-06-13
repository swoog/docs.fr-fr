---
title: ICLRAppDomainResourceMonitor::GetCurrentSurvived, méthode
ms.date: 03/30/2017
api_name:
- ICLRAppDomainResourceMonitor.GetCurrentSurvived
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAppDomainResourceMonitor::GetCurrentSurvived
helpviewer_keywords:
- ICLRAppDomainResourceMonitor::GetCurrentSurvived method [.NET Framework hosting]
- GetCurrentSurvived method [.NET Framework hosting]
ms.assetid: 392e9009-40ef-40e3-ad4d-7ce93a989e78
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7c179ba23be07e8ff77e1397ed753d4287b22440
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33435283"
---
# <a name="iclrappdomainresourcemonitorgetcurrentsurvived-method"></a>ICLRAppDomainResourceMonitor::GetCurrentSurvived, méthode
Obtient le nombre d’octets qui ont survécu à la dernière complète, le garbage collection de blocage et qui sont référencés par le domaine d’application actuel.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT STDMETHODCALLTYPE GetCurrentSurvived(  
             [in]  DWORD dwAppDomainId,  
             [out] ULONGLONG *pAppDomainBytesSurvived,  
             [out] ULONGLONG *pTotalBytesSurvived);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `dwAppDomainId`  
 [in] L’ID du domaine d’application demandé.  
  
 `pAppDomainBytesSurvived`  
 [out] Pointeur vers le nombre d’octets ayant survécu après le dernier garbage collection et qui sont détenues par ce domaine d’application. Après une collection complète, ce nombre est exact et complet. Après une collection éphémère, ce nombre est potentiellement incomplet. Ce paramètre peut être `null`.  
  
 `pRuntimeBytesSurvived`  
 [out] Pointeur vers le nombre total d’octets qui ont survécu à partir du dernier garbage collection. Après une collection complète, ce nombre représente le nombre d’octets qui sont conservées dans les tas managés. Après une collection éphémère, ce nombre représente le nombre d’octets qui sont maintenus actifs dans les générations éphémères. Ce paramètre peut être `null`.  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|La commande s'est correctement terminée.|  
|COR_E_APPDOMAINUNLOADED|Le domaine d’application a été déchargé ou n’existe pas.|  
  
## <a name="remarks"></a>Notes  
 Les statistiques sont mises à jour uniquement après un garbage collection de ; de blocage complet Autrement dit, une collection qui inclut toutes les générations et qui arrête l’application lors de la collection se produit. Par exemple, le <xref:System.GC.Collect?displayProperty=nameWithType> surcharge de méthode effectue un collection de blocage complet. Le garbage collection simultané se produit en arrière-plan et ne bloque pas l’application.  
  
 Le `GetCurrentSurvived` méthode est l’équivalent non managé de managé <xref:System.AppDomain.MonitoringSurvivedMemorySize%2A?displayProperty=nameWithType> propriété.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MetaHost.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICLRAppDomainResourceMonitor, interface](../../../../docs/framework/unmanaged-api/hosting/iclrappdomainresourcemonitor-interface.md)  
 [Analyse de ressource de domaine d'application](../../../../docs/standard/garbage-collection/app-domain-resource-monitoring.md)  
 [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [Hébergement](../../../../docs/framework/unmanaged-api/hosting/index.md)
