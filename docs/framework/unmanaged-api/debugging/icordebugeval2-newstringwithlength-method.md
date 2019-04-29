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
ms.openlocfilehash: b84a2fad53feda2996515781035c0eaad5828d54
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61666986"
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
  
## <a name="parameters"></a>Paramètres  
 `string`  
 [in] Pointeur vers la valeur de chaîne.  
  
 `uiLength`  
 [in] Longueur de la chaîne.  
  
## <a name="remarks"></a>Notes  
 Si à la fin de la chaîne de caractère null est censé être dans la chaîne managée, l’appelant de la `NewStringWithLength` méthode doit vérifier que la longueur de chaîne inclut le caractère null de fin.  
  
 La chaîne est toujours créée dans le domaine d’application dans lequel le thread est en cours d’exécution.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
