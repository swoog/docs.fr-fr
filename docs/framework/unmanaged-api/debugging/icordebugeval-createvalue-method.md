---
title: ICorDebugEval::CreateValue, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEval.CreateValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::CreateValue
helpviewer_keywords:
- ICorDebugEval::CreateValue method [.NET Framework debugging]
- CreateValue method [.NET Framework debugging]
ms.assetid: 9a1c0b47-6f10-4fcb-844a-4ab2d7990140
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2c16f6d1334888fc389a7c39cf0a3865afca2085
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57471042"
---
# <a name="icordebugevalcreatevalue-method"></a>ICorDebugEval::CreateValue, méthode
Crée une valeur du type spécifié, avec une valeur initiale de zéro ou null.  
  
 Cette méthode est obsolète dans le .NET Framework version 2.0. Utilisez [ICorDebugEval2::CreateValueForType](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-createvaluefortype-method.md) à la place.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT CreateValue (  
    [in] CorElementType     elementType,  
    [in] ICorDebugClass     *pElementClass,  
    [out] ICorDebugValue    **ppValue  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `elementType`  
 [in] Une valeur de la [CorElementType](../../../../docs/framework/unmanaged-api/metadata/corelementtype-enumeration.md) énumération qui spécifie le type de la valeur.  
  
 `pElementClass`  
 [in] Pointeur vers un [ICorDebugClass](../../../../docs/framework/unmanaged-api/debugging/icordebugclass-interface.md) objet qui spécifie la classe de la valeur, si le type n’est pas un type primitif.  
  
 `ppValue`  
 [out] Pointeur vers l’adresse d’un objet « ICorDebugValue » qui représente la valeur.  
  
## <a name="remarks"></a>Notes  
 `CreateValue` Crée un `ICorDebugValue` objet du type donné dans le seul but de l’utiliser dans une évaluation de fonction. Cet objet de valeur peut être utilisé pour passer des constantes de l’utilisateur en tant que paramètres.  
  
 Si le type de la valeur est un type primitif, sa valeur initiale est égal à zéro ou null. Utilisez [ICorDebugGenericValue::SetValue](../../../../docs/framework/unmanaged-api/debugging/icordebuggenericvalue-setvalue-method.md) pour définir la valeur d’un type primitif.  
  
 Si la valeur de `elementType` est ELEMENT_TYPE_CLASS, vous obtenez « ICorDebugReferenceValue » (retournées dans `ppValue`) représentant la référence d’objet null. Vous pouvez utiliser cet objet de passer null pour une évaluation de fonction qui a des paramètres de référence d’objet. Vous ne pouvez pas définir le `ICorDebugValue` à n’importe quoi : il reste toujours null.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** 1.1, 1.0  
  
## <a name="see-also"></a>Voir aussi

- [CreateValueForType, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-createvaluefortype-method.md)
- [ICorDebugEval (Interface)](icordebugeval-interface.md)
