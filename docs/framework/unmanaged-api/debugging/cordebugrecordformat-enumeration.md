---
title: CorDebugRecordFormat, énumération
ms.date: 03/30/2017
api_name:
- CorDebugRecordFormat
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: d680c1c0-16ab-4ccc-9444-39cf8e0e05ee
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 45278b116ce1ea1a910d806df408c8692338d9a9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54634374"
---
# <a name="cordebugrecordformat-enumeration"></a>CorDebugRecordFormat, énumération
Décrit le format des données dans un tableau d'octets qui contient des informations sur un événement de débogage d'exception native.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorDebugRecordFormat {  
    FORMAT_WINDOWS_EXCEPTIONRECORD32 = 1,  
    FORMAT_WINDOWS_EXCEPTIONRECORD64 = 2,  
} CorDebugRecordFormat;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`FORMAT_WINDOWS_EXCEPTIONRECORD32`|Les données correspondent à un enregistrement d'exception Windows 32 bits.|  
|`FORMAT_WINDOWS_EXCEPTIONRECORD64`|Les données correspondent à un enregistrement d'exception Windows 64 bits.|  
  
## <a name="remarks"></a>Notes  
 Un membre de la `CorDebugRecordFormat` énumération est passée à la [DecodeEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-decodeevent-method.md) méthode pour indiquer le format du tableau d’octets dans son `pRecord` argument.  
  
> [!NOTE]
>  Cette énumération est destinée à une utilisation dans des scénarios de débogage .NET Native uniquement.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Énumérations de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
