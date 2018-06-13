---
title: WriteableMetadataUpdateMode, énumération
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- WriteableMetadataUpdateMode
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 6758f4d3-6bc7-4c99-8582-e9be00566784
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2fbf9a24c350dd4c33bb50b0add8817c8922925f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33435998"
---
# <a name="writeablemetadataupdatemode-enumeration"></a>WriteableMetadataUpdateMode, énumération
[Pris en charge dans .NET Framework 4.5.2 et ultérieur]  
  
 Fournit des valeurs qui spécifient si les mises à jour en mémoire apportées aux métadonnées sont visibles par un débogueur.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp
typedef enum WriteableMetadataUpdateMode {  
   LegacyCompatPolicy,  
   AlwaysShowUpdates  
} WriteableMetadataUpdateMode;  
```  
  
## <a name="members"></a>Membres  
  
|Nom de membre|Description|  
|-----------------|-----------------|  
|`LegacyCompatPolicy`|Maintient la compatibilité avec les versions antérieures de .NET Framework lors de la mise à jour en mémoire de métadonnées visibles. Pour plus d'informations, consultez la section Notes.|  
|`AlwaysShowUpdates`|Rend les mises à jour en mémoire apportées aux métadonnées visibles par le débogueur.|  
  
## <a name="remarks"></a>Notes  
 Un membre de la `WriteableMetadataUpdateMode` énumération peut être passée à la [SetWriteableMetadataUpdateMode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess7-setwriteablemetadataupdatemode-method.md) méthode pour contrôler si en mémoire des mises à jour aux métadonnées dans le processus cible sont visibles par le débogueur.  
  
 L'option `LegacyCompatPolicy` force le même comportement que dans les versions de .NET Framework antérieures à 4.5.2. Cela signifie souvent que les métadonnées provenant des mises à jour ne sont pas visibles. Cependant, les appels à certaines méthodes de débogage forcent implicitement le débogueur à rendre visibles les mises à jour. Par exemple, si le débogueur passe [ICorDebugILFrame::GetLocalVariable](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-getlocalvariable-method.md) l’index d’une variable introuvable dans les métadonnées d’origine de la méthode, toutes les métadonnées pour le module est mis à jour d’un instantané correspondant à l’état actuel de la processus. En d'autres termes, avec l'option `LegacyCompatPolicy`, le débogueur peut voir aucune, certaines ou toutes les mises à jour des métadonnées disponibles, selon la façon dont il utilise les autres parties de l'API de débogage non managée.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Énumérations de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)  
 [SetWriteableMetadataUpdateMode, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess7-setwriteablemetadataupdatemode-method.md)
