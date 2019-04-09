---
title: ICorDebugReferenceValue, interface
ms.date: 03/30/2017
api_name:
- ICorDebugReferenceValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugReferenceValue
helpviewer_keywords:
- ICorDebugReferenceValue interface [.NET Framework debugging]
ms.assetid: 2040e2be-119a-4cfb-ae52-b0b6f052665c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d6575acfb1f75cbc8e3d59ddca5fea0953274cf2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59206458"
---
# <a name="icordebugreferencevalue-interface"></a>ICorDebugReferenceValue, interface
Fournit des méthodes qui gèrent une valeur qui est une référence à un objet. (Autrement dit, cette interface fournit des méthodes qui gèrent un pointeur.) Cette interface implémente « ICorDebugValue ».  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Dereference, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugreferencevalue-dereference-method.md)|Obtient l’objet qui est référencé.|  
|[DereferenceStrong, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugreferencevalue-dereferencestrong-method.md)|Non implémenté. N'appelez pas cette méthode.|  
|[GetValue, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugreferencevalue-getvalue-method.md)|Obtient l’adresse mémoire actuelle de l’objet référencé.|  
|[IsNull, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugreferencevalue-isnull-method.md)|Obtient une valeur qui indique si ce `ICorDebugReferenceValue` est une valeur null, auquel cas le `ICorDebugReferenceValue` ne pointe pas vers un objet.|  
|[SetValue, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugreferencevalue-setvalue-method.md)|Définit l’adresse de mémoire actuelle. Autrement dit, cette méthode définit ce `ICorDebugReferenceValue` pour pointer vers un objet.|  
  
## <a name="remarks"></a>Notes  
 Le common language runtime (CLR) peut effectuer un garbage collection sur des objets lors de la poursuite du processus débogué. Le garbage collection peut déplacer les objets en mémoire. Un `ICorDebugReferenceValue` soit coopéreront avec le garbage collection afin que ses informations sont mis à jour après le garbage collection, ou sera invalidé implicitement avant le garbage collection.  
  
 Le `ICorDebugReferenceValue` objet peut être invalidé implicitement après poursuite du processus débogué. Le ICorDebugHandleValue « dérivé » n’est pas invalidé jusqu'à ce qu’elle est explicitement libéré ou exposé.  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
