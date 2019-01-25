---
title: CorEventAttr, énumération
ms.date: 03/30/2017
api_name:
- CorEventAttr
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorEventAttr
helpviewer_keywords:
- CorEventAttr enumeration [.NET Framework metadata]
ms.assetid: dc2b3281-3820-487e-930d-350b66dc6417
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d34aa954126cc26519aaea963f99299e5557d2c8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54743049"
---
# <a name="coreventattr-enumeration"></a>CorEventAttr, énumération
Contient des valeurs qui décrivent les métadonnées d'un événement.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorEventAttr {  
  
    evSpecialName           =   0x0200,  
  
    evReservedMask          =   0x0400,  
    evRTSpecialName         =   0x0400,  
  
} CorEventAttr;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`evSpecialName`|Spécifie que l’événement est spécial, et que son nom décrit comment.|  
|`evReservedMask`|Réservé à un usage interne par le common language runtime.|  
|`evRTSpecialName`|Spécifie que le common language runtime doit vérifier l’encodage du nom de l’événement.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorHdr.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Énumérations de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
