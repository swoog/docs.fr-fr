---
title: StackOverflowInfo, structure
ms.date: 03/30/2017
api_name:
- StackOverflowInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StackOverflowInfo
helpviewer_keywords:
- StackOverflowInfo structure [.NET Framework hosting]
ms.assetid: 519389f2-0217-436c-99d4-93a76ebce5b5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ac0f5d522a24394369583692f8c564254529bf13
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59137344"
---
# <a name="stackoverflowinfo-structure"></a>StackOverflowInfo, structure
Stocke le type de dépassement de capacité s’est produite et des informations sur l’exception qui a été levée en raison du dépassement de capacité.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef struct _StackOverflowInfo {  
    StackOverflowType   soType;  
    EXCEPTION_POINTERS  *pExceptionInfo;  
} StackOverflowInfo;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`soType`|Une valeur de la [StackOverflowType](../../../../docs/framework/unmanaged-api/hosting/stackoverflowtype-enumeration.md) énumération qui spécifie le type de dépassement de capacité.|  
|`pExceptionInfo`|Un pointeur vers un Win32 `EXCEPTION_POINTERS` objet qui contient un enregistrement d’exception avec une description indépendante de l’ordinateur d’une exception et un enregistrement de contexte avec une description dépendantes de l’ordinateur du contexte du processeur au moment de l’exception.|  
  
## <a name="remarks"></a>Notes  
 Un `StackOverflowInfo` objet est passé à la [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) méthode pour `Event_StackOverflow` événements.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.idl  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Structures d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)
