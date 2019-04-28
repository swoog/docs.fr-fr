---
title: CorParamAttr, énumération
ms.date: 03/30/2017
api_name:
- CorParamAttr
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorParamAttr
helpviewer_keywords:
- CorParamAttr enumeration [.NET Framework metadata]
ms.assetid: a7ff90ad-dad8-48e8-917d-4aa9a118cbc8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 97f62b082db11a5f0bb930e33cb47acef76e7a04
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61906297"
---
# <a name="corparamattr-enumeration"></a>CorParamAttr, énumération
Contient des valeurs qui décrivent les métadonnées d'un paramètre de méthode.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorParamAttr {  
  
    pdIn                        =   0x0001,  
    pdOut                       =   0x0002,  
    pdOptional                  =   0x0010,  
  
    pdReservedMask              =   0xf000,  
    pdHasDefault                =   0x1000,  
    pdHasFieldMarshal           =   0x2000,  
  
    pdUnused                    =   0xcfe0  
  
} CorParamAttr;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`pdIn`|Spécifie que le paramètre est passé dans l’appel de méthode.|  
|`pdOut`|Spécifie que le paramètre est passé à partir de la méthode de retour.|  
|`pdOptional`|Spécifie que le paramètre est facultatif.|  
|`pdReservedMask`|Réservé à un usage interne par le common language runtime.|  
|`pdHasDefault`|Spécifie que le paramètre a une valeur par défaut.|  
|`pdHasFieldMarshal`|Spécifie que le paramètre a des informations de marshaling.|  
|`pdUnused`|Non utilisé.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorHdr.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
