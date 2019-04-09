---
title: CVStruct, structure
ms.date: 03/30/2017
api_name:
- CVStruct
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CVStruct
helpviewer_keywords:
- CVStruct structure [.NET Framework metadata]
ms.assetid: e9e4e497-d5fb-464b-991c-3bdd824664fd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4a5f06b3f79fed5dac5a6f07650e4fabd0aa5867
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59142166"
---
# <a name="cvstruct-structure"></a>CVStruct, structure
Contient des informations utilisées lors de l'installation d'un module ou d'une image composite.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef struct {  
    short Major;  
    short Minor;  
    short Sub;  
    short Build;  
} CVStruct;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|Majeur|Numéro de build de version principale.|  
|Mineur|Numéro de build de version mineure.|  
|Sub|Numéro de version secondaire.|  
|Build|numéro de build.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Structures de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-structures.md)
