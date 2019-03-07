---
title: ICorConfiguration::SetGCHostControl, méthode
ms.date: 03/30/2017
api_name:
- ICorConfiguration.SetGCHostControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SetGCHostControl
helpviewer_keywords:
- ICorConfiguration::SetGCHostControl method [.NET Framework hosting]
- SetGCHostControl method [.NET Framework hosting]
ms.assetid: bca6bd79-e288-475a-aa46-6bf81541d966
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a64922e1fe069d682f7ebc51040d06231a8b49c3
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57484353"
---
# <a name="icorconfigurationsetgchostcontrol-method"></a>ICorConfiguration::SetGCHostControl, méthode
Définit l’interface de rappel à utiliser par le garbage collector de demander à l’hôte de modifier les limites de mémoire virtuelle.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetGCHostControl (  
    [in] IGCHostControl* pGCHostControl  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pGCHostControl`  
 [in] Un pointeur vers un [IGCHostControl](../../../../docs/framework/unmanaged-api/hosting/igchostcontrol-interface.md) objet qui permet au garbage collector de demander à l’hôte de modifier les limites de mémoire virtuelle.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorConfiguration, interface](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md)
