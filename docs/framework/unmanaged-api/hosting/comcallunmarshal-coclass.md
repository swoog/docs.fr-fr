---
title: Coclasse ComCallUnmarshal
ms.date: 03/30/2017
api_name:
- ComCallUnmarshal Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ComCallUnmarshal
helpviewer_keywords:
- ComCallUnmarshal coclass [.NET Framework hosting]
ms.assetid: 2adb5827-2268-4914-a1c6-f62b61880a45
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2f17a88a90905006432ae8c5dc040277124c947b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59166879"
---
# <a name="comcallunmarshal-coclass"></a>Coclasse ComCallUnmarshal
Fournit des interfaces pour gérer le marshaling de pointeurs d’interface.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
coclass ComCallUnmarshal {  
    [default] interface IMarshal;  
};  
```  
  
## <a name="interfaces"></a>Interfaces  
  
|Interface|Description|  
|---------------|-----------------|  
|`IMarshal`|Fournit des méthodes pour créer, de l’initialisation et de gérer un proxy dans un processus client.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.idl  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Hébergement des coclasses](../../../../docs/framework/unmanaged-api/hosting/hosting-coclasses.md)
