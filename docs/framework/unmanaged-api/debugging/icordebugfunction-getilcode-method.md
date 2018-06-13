---
title: ICorDebugFunction::GetILCode, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.GetILCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::GetILCode
helpviewer_keywords:
- ICorDebugFunction::GetILCode method [.NET Framework debugging]
- GetILCode method [.NET Framework debugging]
ms.assetid: f794dd47-a7cd-47f6-96e9-a41a4dae8e72
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ac34fbca56c8a0f00ee3a7e0f898b8ee03287b11
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33412283"
---
# <a name="icordebugfunctiongetilcode-method"></a>ICorDebugFunction::GetILCode, méthode
Obtient l’instance ICorDebugCode qui représente le code de langage intermédiaire MSIL Microsoft associé à cet objet ICorDebugFunction.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetILCode (  
    [out] ICorDebugCode **ppCode  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `ppCode`  
 [out] Un pointeur vers le `ICorDebugCode` de l’instance, ou null si la fonction n’a pas été compilée dans du code MSIL.  
  
## <a name="remarks"></a>Notes  
 Si Modifier & Continuer a été autorisée pour cette fonction, le `GetILCode` méthode obtiendra le code MSIL correspondant à la version modifiée de cette fonction du code dans le common language runtime (CLR).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
