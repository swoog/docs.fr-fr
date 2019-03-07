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
ms.openlocfilehash: f34a2fe2bb1f92e75f77c086b03776ec59495600
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57482098"
---
# <a name="icordebugfunctiongetilcode-method"></a>ICorDebugFunction::GetILCode, méthode
Obtient l’instance ICorDebugCode qui représente le code de Microsoft intermediate language (MSIL) associé à cet objet ICorDebugFunction.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetILCode (  
    [out] ICorDebugCode **ppCode  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `ppCode`  
 [out] Un pointeur vers le `ICorDebugCode` de l’instance, ou null si la fonction n’a pas été compilée dans du code MSIL.  
  
## <a name="remarks"></a>Notes  
 Si Modifier & Continuer a été autorisée pour cette fonction, le `GetILCode` méthode obtiendra le code MSIL correspondant à cette version modifiée fonction du code dans le common language runtime (CLR).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
