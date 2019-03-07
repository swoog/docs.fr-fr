---
title: ICorDebugModule::GetFunctionFromToken, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetFunctionFromToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetFunctionFromToken
helpviewer_keywords:
- GetFunctionFromToken method, ICorDebugModule interface [.NET Framework debugging]
- ICorDebugModule::GetFunctionFromToken method [.NET Framework debugging]
ms.assetid: 6fe12194-4ef7-43c1-9570-ade35ccf127a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c1af0f8f792c856c0b27b4d3d9ff557bcc5fce82
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57500068"
---
# <a name="icordebugmodulegetfunctionfromtoken-method"></a>ICorDebugModule::GetFunctionFromToken, méthode
Obtient la fonction qui est spécifiée par le jeton de métadonnées.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetFunctionFromToken(  
    [in] mdMethodDef methodDef,  
    [out] ICorDebugFunction **ppFunction  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `methodDef`  
 [in] Un `mdMethodDef` jeton de métadonnées qui référence les métadonnées de la fonction.  
  
 `ppFunction`  
 [out] Pointeur vers l’adresse d’un objet d’interface ICorDebugFunction qui représente la fonction.  
  
## <a name="remarks"></a>Notes  
 Le `GetFunctionFromToken` méthode retourne une valeur HRESULT CORDBG_E_FUNCTION_NOT_IL si la valeur passée dans `methodDef` ne fait pas référence à une méthode MSIL (intermediate language).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
