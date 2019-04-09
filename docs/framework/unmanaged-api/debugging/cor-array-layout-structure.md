---
title: COR_ARRAY_LAYOUT, structure
ms.date: 03/30/2017
api_name:
- COR_ARRAY_LAYOUT
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_ARRAY_LAYOUT
helpviewer_keywords:
- COR_DEBUG_IL_TO_NATIVE_MAP structure [.NET Framework debugging]
ms.assetid: aa20ac3d-6f60-4aa2-91c5-f3a86f82eba8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a3a5a5bb26912c87cdf37ba0d8f0cee1cf1ffa97
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59142010"
---
# <a name="corarraylayout-structure"></a>COR_ARRAY_LAYOUT, structure
Fournit des informations sur la disposition d'un objet Array en mémoire.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef struct COR_ARRAY_LAYOUT {  
    COR_TYPEID componentID;  
    CorElementType componentType;  
    ULONG32 firstElementOffset;  
    ULONG32 elementSize;  
    ULONG32 countOffset;   
    ULONG32 rankSize;   
    ULONG32 numRanks;   
    ULONG32 rankOffset;   
} COR_ARRAY_LAYOUT;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`componentID`|L’identificateur du type d’objets contenus dans le tableau.|  
|`componentType`|Une valeur d’énumération CorElementType qui indique si le composant est une référence de garbage collection, une classe value ou un type primitif.|  
|`firstElementOffset`|Le décalage vers le premier élément du tableau.|  
|`elementSize`|La taille de chaque élément.|  
|`countOffset`|Le décalage pour le nombre d’éléments dans le tableau.|  
|`rankSize`|La taille du rang, en octets.|  
|`numRanks`|Le nombre de rangées dans le tableau.|  
|`rankOffset`|L’offset auquel commencer les rangs.|  
  
## <a name="remarks"></a>Notes  
 Le `rankSize` champ spécifie la taille d’un rang dans un tableau multidimensionnel. Elle est précise dans les tableaux unidimensionnels également.  
  
 La valeur de `numRanks` est 1 pour un tableau unidimensionnel et `N` pour un tableau multidimensionnel de `N` dimensions.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Structures de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
