---
title: ICorPublishProcessEnum, interface
ms.date: 03/30/2017
api_name:
- ICorPublishProcessEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcessEnum
helpviewer_keywords:
- ICorPublishProcessEnum interface [.NET Framework debugging]
ms.assetid: aac8fcf9-ac09-437c-bd5c-2fda14ae1007
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5186df61eb82b29fcfa9776408498b748068e122
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59173652"
---
# <a name="icorpublishprocessenum-interface"></a>ICorPublishProcessEnum, interface
Une sous-classe de la [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md) interface qui fournit des méthodes pour parcourir une collection de [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) objets.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Next, méthode](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-next-method.md)|Obtient le nombre spécifié de `ICorPublishProcess` instances à partir de la collection, en commençant à la position actuelle.|  
  
## <a name="remarks"></a>Notes  
 Le `ICorPublishProcessEnum` interface implémente les méthodes de l’interface abstraite, [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md).  
  
 Un `ICorPublishProcessEnum` instance est créée par le [ICorPublish::EnumProcesses](../../../../docs/framework/unmanaged-api/debugging/icorpublish-enumprocesses-method.md) (méthode). Le parcours de la collection de `ICorPublishProcess` objets est basée sur les critères de filtre fournis au moment où le `ICorPublishProcessEnum` instance a été créée.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorPub.idl, CorPub.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [CorpubPublish (coclasse)](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
