---
title: ICLRHostProtectionManager, interface
ms.date: 03/30/2017
api_name:
- ICLRHostProtectionManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRHostProtectionManager
helpviewer_keywords:
- ICLRHostProtectionManager interface [.NET Framework hosting]
ms.assetid: ce2770ae-23d0-45d9-8bcf-46504ac5020e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c630fcd4667c8b19c4e21335549674d32508e439
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33432834"
---
# <a name="iclrhostprotectionmanager-interface"></a>ICLRHostProtectionManager, interface
Permet à l’hôte bloquer les classes managées spécifiques, les méthodes, les propriétés et les champs de l’exécution dans du code partiellement fiable.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[SetEagerSerializeGrantSets](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-seteagerserializegrantsets-method.md)|Fournit une garantie que certaines conditions de concurrence peuvent erreurs irrécupérable langage common runtime (CLR) ne seront jamais se produire.|  
|[SetProtectedCategories, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-setprotectedcategories-method.md)|Spécifie les catégories de types managés et les membres qui ne doivent pas recevoir de s’exécuter dans du code partiellement fiable.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [EApiCategories, énumération](../../../../docs/framework/unmanaged-api/hosting/eapicategories-enumeration.md)  
 [ICLRControl, interface](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
