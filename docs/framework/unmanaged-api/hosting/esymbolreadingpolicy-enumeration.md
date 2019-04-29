---
title: ESymbolReadingPolicy, énumération
ms.date: 03/30/2017
api_name:
- ESymbolReadingPolicy
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ESymbolReadingPolicy
helpviewer_keywords:
- ESymbolReadingPolicy enumeration [.NET Framework hosting]
ms.assetid: 4dc6c80d-b694-480b-a378-d5b18420ce17
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9ba29952fe4a6edfc6e9e80ec02f82de65ef0064
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61628598"
---
# <a name="esymbolreadingpolicy-enumeration"></a>ESymbolReadingPolicy, énumération
Contient des valeurs qui définissent la stratégie pour la lecture des fichiers de programme (PDB) de la base de données.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum {  
    eSymbolReadingNever,  
    eSymbolReadingAlways,  
    eSymbolReadingFullTrustOnly  
} ESymbolReadingPolicy;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`eSymbolReadingAlways`|Spécifie que le débogueur doit toujours lire des fichiers PDB.|  
|`eSymbolReadingFullTrustOnly`|Spécifie que le débogueur doit lire uniquement les fichiers PDB qui sont associés à des assemblys de confiance totale.|  
|`eSymbolReadingNever`|Spécifie que le débogueur doit lire jamais les fichiers PDB.|  
  
## <a name="remarks"></a>Notes  
 Le `ESymbolReadingPolicy` énumération est utilisée avec la [ICLRDebugManager::SetSymbolReadingPolicy](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setsymbolreadingpolicy-method.md) (méthode).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
