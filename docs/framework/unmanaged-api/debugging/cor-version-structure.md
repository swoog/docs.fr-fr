---
title: COR_VERSION, structure
ms.date: 03/30/2017
api_name:
- COR_VERSION
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_VERSION
helpviewer_keywords:
- COR_VERSION structure [.NET Framework debugging]
ms.assetid: 5efaee1c-a001-4c73-9525-4160f4c71567
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 00e58d83c19c3cb6a2e1eb38942500d7f5dc5cf9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61609293"
---
# <a name="corversion-structure"></a>COR_VERSION, structure
Stocke le numéro de version en quatre parties du CLR (Common Language Runtime).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef struct _COR_VERSION {  
    DWORD dwMajor;  
    DWORD dwMinor;  
    DWORD dwBuild;  
    DWORD dwSubBuild;  
} COR_VERSION;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`dwMajor`|Numéro de version principale.|  
|`dwMinor`|Numéro de version secondaire.|  
|`dwBuild`|Le numéro de build.|  
|`dwSubBuild`|Le numéro de version secondaire.|  
  
## <a name="remarks"></a>Notes  
 Si le numéro de version est 1.0.3705.288, 1 est le numéro de version majeure, 0 est le numéro de version secondaire, 3705 est le numéro de build et 288 est le numéro de version secondaire.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Structures de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
