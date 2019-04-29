---
title: ICorDebugHandleValue, interface
ms.date: 03/30/2017
api_name:
- ICorDebugHandleValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHandleValue
helpviewer_keywords:
- ICorDebugHandleValue interface [.NET Framework debugging]
ms.assetid: 66fcd2b8-ac66-414b-83a8-75a925e17772
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9a9eb63e681b47f058901b0ff002015baffe6048
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775659"
---
# <a name="icordebughandlevalue-interface"></a>ICorDebugHandleValue, interface

Sous-classe de ICorDebugReferenceValue qui représente une valeur de référence auquel le débogueur a créé un handle pour le garbage collection.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Dispose, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebughandlevalue-dispose-method.md)|Libère le handle référencé par ce `ICorDebugHandleValue` objet sans libérer explicitement le pointeur d’interface.|  
|[GetHandleType, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebughandlevalue-gethandletype-method.md)|Obtient une valeur CorDebugHandleType qui décrit le type de handle référencé par cet `ICorDebugHandleValue`.|  
  
## <a name="remarks"></a>Notes  
 Un `ICorDebugReferenceValue` objet est invalidé par un arrêt dans l’exécution du code débogué. Un `ICorDebugHandleValue` conserve sa référence via les arrêts et reprises, jusqu'à ce qu’il est explicitement libéré.  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
