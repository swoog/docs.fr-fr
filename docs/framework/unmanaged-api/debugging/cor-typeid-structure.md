---
title: COR_TYPEID, structure
ms.date: 03/30/2017
api_name:
- COR_TYPEID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_TYPEID
helpviewer_keywords:
- COR_TYPEID structure [.NET Framework debugging]
ms.assetid: 1e172b14-ee22-4943-b3b8-3740e7bdcd2e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b905d3b5de39057cba384ea7bca917bc3476623f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54700648"
---
# <a name="cortypeid-structure"></a>COR_TYPEID, structure
Contient un identificateur de type.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef struct COR_TYPEID{  
    UINT64 token1;  
    UINT64 token2;  
} COR_TYPEID;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`token1`|Le premier jeton.|  
|`token2`|Le deuxième jeton.|  
  
## <a name="remarks"></a>Notes  
 Le `COR_TYPEID` structure est retournée par un nombre de méthodes de débogage qui fournissent des informations sur les objets de garbage collection. Elle peut ensuite être transmise en tant qu’argument à d’autres méthodes de débogage qui fournissent des informations supplémentaires sur cet élément. Par exemple, en énumérant un [ICorDebugHeapEnum](../../../../docs/framework/unmanaged-api/debugging/icordebugheapenum-interface.md) de l’objet, vous pouvez récupérer des [COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md) objets qui représentent des objets individuels sur le tas managé. Vous pouvez ensuite passer le `COR_TYPEID` valeur à partir de la `COR_HEAPOBJECT.type` champ la [ICorDebugProcess5::GetTypeForTypeID](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-gettypefortypeid-method.md) méthode pour récupérer un objet ICorDebugType qui fournit des informations de type sur l’objet.  
  
 Un `COR_TYPEID` objet est destiné à être opaque. Ses champs individuels ne doivent pas accessibles ou manipulés. Son utilisation exclusive est celui d’identificateur qui est fourni comme un `out` paramètre dans un appel de méthode et qui peut, à son tour, être transmis à d’autres méthodes pour fournir des informations supplémentaires.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Structures de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
