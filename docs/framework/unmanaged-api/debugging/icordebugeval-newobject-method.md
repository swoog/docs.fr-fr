---
title: ICorDebugEval::NewObject, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEval.NewObject
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::NewObject
helpviewer_keywords:
- NewObject method [.NET Framework debugging]
- ICorDebugEval::NewObject method [.NET Framework debugging]
ms.assetid: ce3025e8-defa-4c5e-8298-f49d71fa5736
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 97217421d30ee4065aa1b2500e9486405e438902
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57471366"
---
# <a name="icordebugevalnewobject-method"></a>ICorDebugEval::NewObject, méthode
Alloue une nouvelle instance d’objet et appelle la méthode de constructeur spécifié.  
  
 Cette méthode est obsolète dans le .NET Framework version 2.0. Utilisez [ICorDebugEval2::NewParameterizedObject](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedobject-method.md) à la place.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT NewObject (  
    [in] ICorDebugFunction  *pConstructor,  
    [in] ULONG32            nArgs,  
    [in, size_is(nArgs)] ICorDebugValue *ppArgs[]  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pConstructor`  
 [in] Le constructeur à appeler.  
  
 `nArgs`  
 [in] Taille du tableau `ppArgs`.  
  
 `ppArgs`  
 [in] Tableau d’objets ICorDebugValue, chacun d’eux représente un argument à passer au constructeur.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** 1.1, 1.0  
  
## <a name="see-also"></a>Voir aussi
- [NewParameterizedObject, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedobject-method.md)
