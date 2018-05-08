---
title: ICorDebugEval2::NewStringWithLength, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEval2.NewStringWithLength
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval2::NewStringWithLength
helpviewer_keywords:
- NewStringWithLength method [.NET Framework debugging]
- ICorDebugEval2::NewStringWithLength method [.NET Framework debugging]
ms.assetid: d5f54a34-6335-4708-b407-a756ec70fab4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6b3b77a0ffc7af3b3640d1b255bd3be522f45a7a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="icordebugeval2newstringwithlength-method"></a>ICorDebugEval2::NewStringWithLength, méthode
Crée une chaîne de la longueur spécifiée, avec le contenu spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT NewStringWithLength (  
    [in] LPCWSTR               string,  
    [in] UINT                  uiLength  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `string`  
 [in] Pointeur vers la valeur de chaîne.  
  
 `uiLength`  
 [in] Longueur de la chaîne.  
  
## <a name="remarks"></a>Notes  
 Si à la fin de la chaîne de caractère null est censé être dans la chaîne managée, l’appelant de la `NewStringWithLength` méthode doit garantir que la longueur de chaîne inclut le caractère null de fin.  
  
 La chaîne est toujours créée dans le domaine d’application dans lequel le thread est en cours d’exécution.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
