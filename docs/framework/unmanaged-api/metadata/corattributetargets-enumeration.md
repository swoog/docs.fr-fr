---
title: CorAttributeTargets, énumération
ms.date: 03/30/2017
api_name:
- CorAttributeTargets
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorAttributeTargets
helpviewer_keywords:
- CorAttributeTargets enumeration [.NET Framework metadata]
ms.assetid: 694c0fa0-7011-41a9-9dfd-f0e16ea574b5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 49784a0eba0458a7b9ddbcd58cbe1a187c3c779a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61905825"
---
# <a name="corattributetargets-enumeration"></a>CorAttributeTargets, énumération
Spécifie les éléments de l'application auxquels un attribut peut être appliqué.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorAttributeTargets  
{  
    catAssembly            = 0x0001,  
    catModule              = 0x0002,  
    catClass               = 0x0004,  
    catStruct              = 0x0008,  
    catEnum                = 0x0010,  
    catConstructor         = 0x0020,  
    catMethod              = 0x0040,  
    catProperty            = 0x0080,  
    catField               = 0x0100,  
    catEvent               = 0x0200,  
    catInterface           = 0x0400,  
    catParameter           = 0x0800,  
    catDelegate            = 0x1000,  
    catGenericParameter    = 0x4000,  
  
    catAll                 =   
        catAssembly | catModule | catClass | catStruct |   
        catEnum | catConstructor | catMethod | catProperty |   
        catField | catEvent | catInterface | catParameter |   
        catDelegate | catGenericParameter,  
  
    catClassMembers        =   
        catClass | catStruct | catEnum | catConstructor |   
        catMethod | catProperty | catField | catEvent |   
        catDelegate | catInterface  
  
} CorAttributeTargets;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`catAssembly`|Attribut peut être appliqué à un assembly.|  
|`catModule`|Attribut peut être appliqué à un module (.dll ou .exe) exécutable portable.|  
|`catClass`|Attribut peut être appliqué à une classe.|  
|`catStruct`|Attribut peut être appliqué à une structure ; Autrement dit, une valeur de type.|  
|`catEnum`|Attribut peut être appliqué à une énumération.|  
|`catConstructor`|Attribut peut être appliqué à un constructeur.|  
|`catMethod`|Attribut peut être appliqué à une méthode.|  
|`catProperty`|Attribut peut être appliqué à une propriété.|  
|`catField`|Attribut peut être appliqué à un champ.|  
|`catEvent`|Attribut peut être appliqué à un événement.|  
|`catInterface`|Attribut peut être appliqué à une interface.|  
|`catParameter`|Attribut peut être appliqué à un paramètre.|  
|`catDelegate`|Attribut peut être appliqué à un délégué.|  
|`catGenericParameter`|Attribut peut être appliqué à un paramètre générique.|  
|`catAll`|Attribut peut être appliqué à n’importe quel élément d’application.|  
|`catClassMembers`|Attribut peut être appliqué à un membre d’une classe.|  
  
## <a name="remarks"></a>Notes  
 Le `CorAttributeTargets` valeurs d’énumération peuvent être combinées avec une opération OR au niveau du bit pour obtenir la combinaison souhaitée.  
  
 Le `CorAttributeTargets` en parallèle managé <xref:System.AttributeTargets?displayProperty=nameWithType> énumération.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorHdr.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
