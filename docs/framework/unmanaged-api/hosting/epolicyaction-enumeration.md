---
title: EPolicyAction, énumération
ms.date: 03/30/2017
api_name:
- EPolicyAction
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EPolicyAction
helpviewer_keywords:
- EPolicyAction enumeration [.NET Framework hosting]
ms.assetid: 72dd76ba-239e-45ac-9ded-318fb07d6c6d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 75bd7da67cbac958f0b34c8295454a719962c7ed
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59201726"
---
# <a name="epolicyaction-enumeration"></a>EPolicyAction, énumération
Décrit les actions de stratégie que l’hôte peut définir pour les opérations décrites par [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) et les échecs décrits par [EClrFailure](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum {  
    eNoAction,  
    eThrowException,  
    eAbortThread,  
    eRudeAbortThread,  
    eUnloadAppDomain,  
    eRudeUnloadAppDomain,  
    eExitProcess,  
    eFastExitProcess,  
    eRudeExitProcess,  
    eDisableRuntime  
} EPolicyAction;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`eAbortThread`|Spécifie que le common language runtime (CLR) doit abandonner le thread normalement. Un abandon correct implique des tentatives d’exécution de tous les `finally` bloque les `catch` blocs liés aux abandons de thread et les finaliseurs.|  
|`eDisableRuntime`|Spécifie que le CLR doit entrer dans un état désactivé. Aucun autre code managé peut être exécuté dans le processus affecté et les threads sont bloqués de pénétrer dans le CLR.|  
|`eExitProcess`|Spécifie que le CLR doit tenter une sortie normale du processus, notamment l’exécution des finaliseurs et effectuer des opérations de journalisation et de nettoyage.|  
|`eFastExitProcess`|Spécifie que le CLR doit quitter le processus immédiatement, sans exécuter les finaliseurs ou effectuer des opérations de nettoyage et la journalisation. Toutefois, la notification est envoyée au débogueur.|  
|`eNoAction`|Spécifie qu’aucune action à entreprendre.|  
|`eRudeAbortThread`|Spécifie que le CLR doit effectuer un abandon de thread brutal. Seuls les `catch` et `finally` blocs marqués avec <xref:System.EnterpriseServices.MustRunInClientContextAttribute> sont exécutées.|  
|`eRudeExitProcess`|Spécifie que le CLR doit quitter le processus sans exécuter des finaliseurs ou la journalisation des opérations.|  
|`eRudeUnloadAppDomain`|Spécifie que le CLR doit effectuer un déchargement brutal du <xref:System.AppDomain>. Seuls les finaliseurs marqués avec <xref:System.EnterpriseServices.MustRunInClientContextAttribute> sont exécutées. De même, tous les threads avec cette <xref:System.AppDomain> dans leur pile reçoivent un `ThreadAbortException`, mais uniquement ceux `catch` et `finally` blocs marqués avec <xref:System.EnterpriseServices.MustRunInClientContextAttribute> sont exécutées.|  
|`eThrowException`|Spécifie qu’une exception appropriée à la condition, par exemple une mémoire insuffisante, un dépassement de tampon, etc., doit être levée.|  
|`eUnloadAppDomain`|Spécifie que le <xref:System.AppDomain> doit être déchargée. Le CLR tente d’exécuter des finaliseurs.|  
  
## <a name="remarks"></a>Notes  
 L’hôte définit les actions de stratégie en appelant des méthodes de la [ICLRPolicyManager](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md) interface. Pour plus d’informations sur les abandons brutaux et sans perte de données, consultez le [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) énumération.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [EClrFailure, énumération](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md)
- [ICLRPolicyManager, interface](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)
- [IHostPolicyManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihostpolicymanager-interface.md)
- [Énumérations d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
