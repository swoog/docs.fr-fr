---
title: USER_THREAD, structure
ms.date: 03/30/2017
api_name:
- USER_THREAD
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- USER_THREAD
helpviewer_keywords:
- USER_THREAD structure [.NET Framework debugging]
ms.assetid: a57c7d71-c4b0-41f9-a964-0c5ee84a3124
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 93e96d6f8570e6aef7bfc18ef2859dc1e86ec8fb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429029"
---
# <a name="userthread-structure"></a>USER_THREAD, structure
Fournit des informations à un débogueur sur un thread. Pour plus d’informations, consultez la [INotifySource2::SetNotifyFilter](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-setnotifyfilter-method.md) (méthode).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef struct tagUSER_THREAD  
{  
    BYTE    *pSidBuffer;  
    DWORD   dwSidLen;  
    DWORD   dwTid;  
} USER_THREAD;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`pSidBuffer`|Adresse de la mémoire tampon de thread.|  
|`dwSidLen`|Longueur de la mémoire tampon de thread, en octets.|  
|`dwTid`|ID de thread.|  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** ProtocolNotify2.idl  
  
## <a name="see-also"></a>Voir aussi  
 [SetNotifyFilter, méthode](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-setnotifyfilter-method.md)  
 [Structures du magasin de symboles de diagnostics](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-structures.md)
