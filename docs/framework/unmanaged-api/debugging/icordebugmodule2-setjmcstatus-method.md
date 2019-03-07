---
title: ICorDebugModule2::SetJMCStatus, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule2.SetJMCStatus
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule2::SetJMCStatus
helpviewer_keywords:
- SetJMCStatus method, ICorDebugModule2 interface [.NET Framework debugging]
- ICorDebugModule2::SetJMCStatus method [.NET Framework debugging]
ms.assetid: 8c6d2089-4dbb-4715-b9e9-2a4491c8c9ce
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d20c640d6a6a43b7bde4c7d46df470c7bc8c5aa2
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57499522"
---
# <a name="icordebugmodule2setjmcstatus-method"></a>ICorDebugModule2::SetJMCStatus, méthode
Définit l’état d’uniquement mon Code (JMC) de toutes les méthodes de toutes les classes dans ce ICorDebugModule2 à la valeur spécifiée, à l’exception de celles figurant dans le `pTokens` tableau, il définit la valeur opposée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetJMCStatus (  
    [in] BOOL                        bIsJustMyCode,  
    [in] ULONG32                     cTokens,  
    [in, size_is(cTokens)] mdToken   pTokens[]  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `bIsJustMycode`  
 [in] La valeur `true` si le code doit être débogué ; sinon, la valeur est `false`.  
  
 `cTokens`  
 [in] Taille du tableau `pTokens`.  
  
 `pTokens`  
 [in] Un tableau de `mdToken` valeurs, chacune d’elles fait référence à une méthode qui auront leur état JMC défini sur !`bIsJustMycode`.  
  
## <a name="remarks"></a>Notes  
 L’état JMC de chaque méthode qui est spécifiée dans le `pTokens` tableau est défini à l’opposé de la `bIsJustMycode` valeur. L’état de toutes les autres méthodes dans ce module est défini sur le `bIsJustMycode` valeur.  
  
 Le `SetJMCStatus` méthode efface tous les paramètres JMC précédents dans ce module.  
  
 Le `SetJMCStatus` méthode retourne une valeur S_OK HRESULT si toutes les fonctions ont été définies correctement. Elle retourne un HRESULT CORDBG_E_FUNCTION_NOT_DEBUGGABLE si certaines fonctions sont marquées `true` ne sont pas pouvant être débogué.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
