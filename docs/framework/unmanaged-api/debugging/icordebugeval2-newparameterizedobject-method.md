---
title: ICorDebugEval2::NewParameterizedObject, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEval2.NewParameterizedObject
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval2::NewParameterizedObject
helpviewer_keywords:
- NewParameterizedObject method [.NET Framework debugging]
- ICorDebugEval2::NewParameterizedObject method [.NET Framework debugging]
ms.assetid: 3d705463-e640-4249-8036-4e8206d03cfe
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c35baaee13782566c64dd8447c6a034f699b5cd0
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57479608"
---
# <a name="icordebugeval2newparameterizedobject-method"></a>ICorDebugEval2::NewParameterizedObject, méthode
Instancie un nouvel objet de type paramétré et appelle la méthode de constructeur de l’objet.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT NewParameterizedObject (  
    [in] ICorDebugFunction     *pConstructor,  
    [in] ULONG32               nTypeArgs,  
    [in, size_is(nTypeArgs)] ICorDebugType *ppTypeArgs[],  
    [in] ULONG32               nArgs,  
    [in, size_is(nArgs)] ICorDebugValue *ppArgs[]  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pConstructor`  
 [in] Pointeur vers un objet ICorDebugFunction qui représente le constructeur de l’objet à instancier.  
  
 `nTypeArgs`  
 [in] Nombre d’arguments de type passés.  
  
 `ppTypeArgs`  
 [in] Tableau de pointeurs, chacun pointant vers un objet de ICorDebugType qui représente un argument de type pour l’objet qui est en cours d’instanciation.  
  
 `nArgs`  
 [in] Le nombre d’arguments passés au constructeur.  
  
 `ppArgs`  
 [in] Tableau de pointeurs, chacun d’eux pointe vers un objet ICorDebugValue qui représente une valeur d’argument est passée au constructeur.  
  
## <a name="remarks"></a>Notes  
 Constructeur de l’objet peut prendre <xref:System.Type> paramètres.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
