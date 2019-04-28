---
title: ASM_NAME, énumération
ms.date: 03/30/2017
api_name:
- ASM_NAME
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- ASM_NAME
helpviewer_keywords:
- ASM_NAME enumeration [.NET Framework fusion]
ms.assetid: c8b65b19-d777-428f-bc0c-0d84c78a37bc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b37e9c2874448b5fff82f6a37f6ca850875f2b04
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61914585"
---
# <a name="asmname-enumeration"></a>ASM_NAME, énumération
Indique la version, la build, la culture, la signature et ainsi de suite, de l’assembly dont les propriétés seront récupérées ou définies [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) méthodes.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum {  
  
    ASM_NAME_PUBLIC_KEY = 0,  
    ASM_NAME_PUBLIC_KEY_TOKEN,  
    ASM_NAME_HASH_VALUE,  
    ASM_NAME_NAME,  
    ASM_NAME_MAJOR_VERSION,  
    ASM_NAME_MINOR_VERSION,  
    ASM_NAME_BUILD_NUMBER,  
    ASM_NAME_REVISION_NUMBER,  
    ASM_NAME_CULTURE,  
    ASM_NAME_PROCESSOR_ID_ARRAY,  
    ASM_NAME_OSINFO_ARRAY,  
    ASM_NAME_HASH_ALGID,  
    ASM_NAME_ALIAS,  
    ASM_NAME_CODEBASE_URL,  
    ASM_NAME_CODEBASE_LASTMOD,  
    ASM_NAME_NULL_PUBLIC_KEY,  
    ASM_NAME_NULL_PUBLIC_KEY_TOKEN,  
    ASM_NAME_CUSTOM,  
    ASM_NAME_NULL_CUSTOM,   
    ASM_NAME_MVID,  
    ASM_NAME_FILE_MAJOR_VERSION,  
    ASM_NAME_FILE_MINOR_VERSION,  
    ASM_NAME_FILE_BUILD_NUMBER,  
    ASM_NAME_FILE_REVISION_NUMBER,  
    ASM_NAME_RETARGET,  
    ASM_NAME_SIGNATURE_BLOB,  
    ASM_NAME_CONFIG_MASK,  
    ASM_NAME_ARCHITECTURE,  
    ASM_NAME_MAX_PARAMS  
  
} ASM_NAME;  
```  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Fusion.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IAssemblyName, interface](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
- [Énumérations de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-enumerations.md)
