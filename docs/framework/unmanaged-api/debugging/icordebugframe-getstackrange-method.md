---
title: ICorDebugFrame::GetStackRange, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetStackRange
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetStackRange
helpviewer_keywords:
- GetStackRange method, ICorDebugFrame interface [.NET Framework debugging]
- ICorDebugFrame::GetStackRange method [.NET Framework debugging]
ms.assetid: fab037cb-fda6-40fb-9367-921e435dd5a0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5da87071bc23ac17a3077049cd77f0fb8611439f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="icordebugframegetstackrange-method"></a>ICorDebugFrame::GetStackRange, méthode
Obtient la plage d’adresses absolues de ce frame de pile.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetStackRange (  
    [out] CORDB_ADDRESS      *pStart,   
    [out] CORDB_ADDRESS      *pEnd  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pStart`  
 [out] Un pointeur vers un `CORDB_ADDRESS` qui spécifie l’adresse de départ du frame de pile représenté par ce `ICorDebugFrame` objet.  
  
 `pEnd`  
 [out] Un pointeur vers un `CORDB_ADDRESS` qui spécifie l’adresse de fin du frame de pile représenté par ce `ICorDebugFrame` objet.  
  
## <a name="remarks"></a>Notes  
 La plage d’adresses de la pile est utile pour regrouper des traces de pile entrelacées issues de plusieurs moteurs de débogage. La plage numérique ne fournit aucune information sur le contenu du frame de pile. Il n’est significative uniquement pour la comparaison des emplacements de frame de pile.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
