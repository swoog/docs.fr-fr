---
title: CorFileMapping, énumération
ms.date: 03/30/2017
api_name:
- CorFileMapping
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorFileMapping
helpviewer_keywords:
- CorFileMapping enumeration [.NET Framework metadata]
ms.assetid: 3ca41592-b8da-475a-8032-a15627730003
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3c8864aa604b0483130eac5aa0d7c0640abbac99
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443721"
---
# <a name="corfilemapping-enumeration"></a>CorFileMapping, énumération
Contient des valeurs qui décrivent le type de mappage de fichier retourné par un appel à la [IMetaDataInfo::GetFileMapping](../../../../docs/framework/unmanaged-api/metadata/imetadatainfo-getfilemapping-method.md) (méthode).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorFileMapping {  
  
    fmFlat                  =   0x0000,  
    fmExecutableImage       =   0x0001  
  
} CorFileMapping;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`fmFlat`|Le fichier est mappé comme un fichier de données. Autrement dit, le `SEC_IMAGE` indicateur n’a pas été transmis à Microsoft Win32 `CreateFileMapping` (fonction).|  
|`fmExecutableImage`|Le fichier est mappé pour l’exécution, en utilisant le `LoadLibrary` (fonction) ou le `CreateFileMapping` fonctionne avec le `SEC_IMAGE` indicateur.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorHdr.h  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Énumérations de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)  
 [GetFileMapping, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatainfo-getfilemapping-method.md)
