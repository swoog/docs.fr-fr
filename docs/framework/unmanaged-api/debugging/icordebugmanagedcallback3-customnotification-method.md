---
title: ICorDebugManagedCallback3::CustomNotification, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback3.CustomNotification Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback3::CustomNotification
helpviewer_keywords:
- ICorDebugManagedCallback3::CustomNotification method [.NET Framework debugging]
- CustomNotification method [.NET Framework debugging]
ms.assetid: 5e5422ac-afa1-403d-a894-2d7348673e38
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b086c27d73324b4d834c9afa9e7aea20bf6d9148
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59193575"
---
# <a name="icordebugmanagedcallback3customnotification-method"></a>ICorDebugManagedCallback3::CustomNotification, méthode
Indique qu’une notification de débogueur personnalisée a été déclenchée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT CustomNotification(ICorDebugThread *    pThread,  
                           ICorDebugAppDomain * pAppDomain);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pThread`  
 [in] Pointeur vers le thread qui a déclenché la notification.  
  
 `pAppDomain`  
 [in] Pointeur vers le domaine d’application qui contient le thread qui a déclenché la notification.  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|La commande s'est correctement terminée.|  
  
## <a name="exceptions"></a>Exceptions  
  
## <a name="remarks"></a>Notes  
 Un appel ultérieur à la [ICorDebugThread4::GetCurrentCustomDebuggerNotification](../../../../docs/framework/unmanaged-api/debugging/icordebugthread4-getcurrentcustomdebuggernotification-method.md) méthode récupère l’objet thread qui a été passé à la <xref:System.Diagnostics.Debugger.NotifyOfCrossThreadDependency%2A?displayProperty=nameWithType> (méthode). Type de l’objet thread doit avoir été précédemment activé en appelant le [ICorDebugProcess3::SetEnableCustomNotification](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess3-setenablecustomnotification-method.md) (méthode). Le débogueur peut lire des paramètres spécifiques au type à partir des champs de l’objet thread et peut stocker les réponses dans des champs.  
  
 Le [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) interface n’impose aucune stratégie sur les types de notifications ou leur contenu, et la sémantique des notifications est strictement un contrat entre les débogueurs, applications et le .NET Framework.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugManagedCallback3, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback3-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
