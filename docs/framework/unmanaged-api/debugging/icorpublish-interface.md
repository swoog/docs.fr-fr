---
title: ICorPublish, interface
ms.date: 03/30/2017
api_name:
- ICorPublish
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublish
helpviewer_keywords:
- ICorPublish interface [.NET Framework debugging]
ms.assetid: 87c4fcb2-7703-4a2e-afb6-42973381b960
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e1dea8cc54c68db333c409e3bd7b3e4211bd52ac
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54713965"
---
# <a name="icorpublish-interface"></a>ICorPublish, interface
Sert d’interface générale pour la publication d’informations sur les processus et des informations sur les domaines d’application dans ces processus.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[EnumProcesses, méthode](../../../../docs/framework/unmanaged-api/debugging/icorpublish-enumprocesses-method.md)|Obtient un [ICorPublishProcessEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-interface.md) instance qui contient les processus gérés en cours d’exécution sur cet ordinateur.|  
|[GetProcess, méthode](../../../../docs/framework/unmanaged-api/debugging/icorpublish-getprocess-method.md)|Obtient un [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) instance qui représente le processus avec l’identificateur spécifié.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorPub.idl, CorPub.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [CorpubPublish, coclasse](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
