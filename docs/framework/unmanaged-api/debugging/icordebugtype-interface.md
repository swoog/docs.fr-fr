---
title: ICorDebugType, Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType
helpviewer_keywords:
- ICorDebugType interface [.NET Framework debugging]
ms.assetid: 94e02e31-67ea-4b00-8148-a46740a4571d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d29ab3c67e0788b15850b7dfb8b55914c1d1e369
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54694527"
---
# <a name="icordebugtype-interface1"></a>ICorDebugType, Interface1
Représente un type, base ou complex (c'est-à-dire défini par l’utilisateur). Si le type est générique, `ICorDebugType` représente le type générique instancié.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[EnumerateTypeParameters, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-enumeratetypeparameters-method.md)|Obtient un pointeur d’interface ICorDebugTypeEnum qui référence le générique <xref:System.Type> paramètres de la classe référencée par ce `ICorDebugType`.|  
|[GetBase, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-getbase-method.md)|Obtient un pointeur d’interface vers un `ICorDebugType` qui fait référence à la classe de base de la classe référencée par ce `ICorDebugType`, s’il en existe.|  
|[GetClass, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-getclass-method.md)|Obtient un pointeur d’interface ICorDebugClass qui référence le constructeur typé de ce `ICorDebugType`.|  
|[GetFirstTypeParameter, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-getfirsttypeparameter-method.md)|Obtient un pointeur d’interface vers un `ICorDebugType` qui fait référence à la première générique <xref:System.Type> paramètre du constructeur de la classe référencée par ce `ICorDebugType`.|  
|[GetRank, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-getrank-method.md)|Obtient le nombre de dimensions dans un type tableau.|  
|[GetStaticFieldValue, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-getstaticfieldvalue-method.md)|Obtient un pointeur d’interface vers ICorDebugValue qui contient la valeur du champ statique référencé par le champ spécifié de jetons dans le frame de pile spécifié.|  
|[GetType, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-gettype-method.md)|Obtient une valeur CorElementType qui décrit le type natif du common language runtime <xref:System.Type> référencée par ce `ICorDebugType`.|  
  
## <a name="remarks"></a>Notes  
 Si le type est générique, `ICorDebugClass` représente le type non instancié. Le `ICorDebugType` interface représente un type générique instancié. Par exemple, table de hachage\<K, V > est représenté par `ICorDebugClass`, tandis que table de hachage\<Int32, String > est représenté par `ICorDebugType`.  
  
 Les types non génériques sont représentés par les deux `ICorDebugClass` et `ICorDebugType`. L’interface de ce dernier a été introduite dans le .NET Framework version 2.0 pour gérer l’instanciation de type.  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
