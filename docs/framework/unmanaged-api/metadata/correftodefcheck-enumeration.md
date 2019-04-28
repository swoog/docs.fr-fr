---
title: CorRefToDefCheck, énumération
ms.date: 03/30/2017
api_name:
- CorRefToDefCheck
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorRefToDefCheck
helpviewer_keywords:
- CorRefToDefCheck enumeration [.NET Framework metadata]
ms.assetid: f9a80f1a-55af-4459-b095-8441aae16119
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 82abeb0ce3db075d794787bb1fcd5bc18321bef2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61906176"
---
# <a name="correftodefcheck-enumeration"></a>CorRefToDefCheck, énumération
Spécifie des indicateurs pour contrôler les éléments référencés qui sont convertis en définitions afin d'optimiser le code.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorRefToDefCheck {  
    MDRefToDefDefault           = 0x00000003,  
    MDRefToDefAll               = 0xffffffff,  
    MDRefToDefNone              = 0x00000000,  
    MDTypeRefToDef              = 0x00000001,  
    MDMemberRefToDef            = 0x00000002  
} CorRefToDefCheck;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`MDRefToDefDefault`|Spécifie que les références de type et membre doivent être convertis en définitions. C’est la valeur par défaut (`MDTypeRefToDef` &#124; `MDMemberRefToDef`).|  
|`MDRefToDefAll`|Spécifie que tous les éléments référencés doivent être convertis en définitions.|  
|`MDRefToDefNone`|Spécifie qu’aucun élément référencé ne doit être convertie en définitions.|  
|`MDTypeRefToDef`|Spécifie que seules les références de type doivent être convertis en définitions de type.|  
|`MDMemberRefToDef`|Spécifie que seules les références de membre doivent être convertis en définitions. Autrement dit, les références de membre doivent être converties vers les définitions de méthode ou de définitions de champ.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorHdr.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
