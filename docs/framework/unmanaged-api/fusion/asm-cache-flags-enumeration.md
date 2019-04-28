---
title: ASM_CACHE_FLAGS, énumération
ms.date: 03/30/2017
api_name:
- ASM_CACHE_FLAGS
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- ASM_CACHE_FLAGS
helpviewer_keywords:
- ASM_CACHE_FLAGS enumeration [.NET Framework fusion]
ms.assetid: 82e9a7da-321b-48b8-b239-52eaffda6be8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 619643eb50abc75fd10d59b38767013b2617c8cf
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61915289"
---
# <a name="asmcacheflags-enumeration"></a>ASM_CACHE_FLAGS, énumération
Indique la source d’un assembly qui est représenté par [IAssemblyCacheItem](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md) dans le global assembly cache.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum {  
    ASM_CACHE_ZAP       = 0x01,  
    ASM_CACHE_GAC       = 0x02,  
    ASM_CACHE_DOWNLOAD  = 0x04,  
    ASM_CACHE_ROOT      = 0x08,  
    ASM_CACHE_ROOT_EX   = 0x80  
} ASM_CACHE_FLAGS;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`ASM_CACHE_ZAP`|Énumère le cache d’assemblys précompilés à l’aide de Ngen.exe.|  
|`ASM_CACHE_GAC`|Énumère le global assembly cache.|  
|`ASM_CACHE_DOWNLOAD`|Énumère les assemblys qui ont été téléchargées à la demande ou qui ont été une copie fantôme.|  
|`ASM_CACHE_ROOT`|Indique que le [GetCachePath](../../../../docs/framework/unmanaged-api/fusion/getcachepath-function.md) fonction doit retourner le chemin d’accès dans le global assembly cache pour le common language runtime (CLR) version 2.0. Pertinent uniquement dans le contexte d’un appel à [GetCachePath](../../../../docs/framework/unmanaged-api/fusion/getcachepath-function.md).|  
|`ASM_CACHE_ROOT_EX`|Indique que le [GetCachePath](../../../../docs/framework/unmanaged-api/fusion/getcachepath-function.md) fonction doit retourner le chemin d’accès dans le global assembly cache pour le CLR version 4. Pertinent uniquement dans le contexte d’un appel à [GetCachePath](../../../../docs/framework/unmanaged-api/fusion/getcachepath-function.md).|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Fusion.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [GetCachePath, fonction](../../../../docs/framework/unmanaged-api/fusion/getcachepath-function.md)
- [IAssemblyCacheItem, interface](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md)
- [Énumérations de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-enumerations.md)
