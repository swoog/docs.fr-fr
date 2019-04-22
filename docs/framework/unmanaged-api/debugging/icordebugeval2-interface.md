---
title: ICorDebugEval2, interface
ms.date: 03/30/2017
api_name:
- ICorDebugEval2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval2
helpviewer_keywords:
- ICorDebugEval2 interface [.NET Framework debugging]
ms.assetid: fce34531-2687-406d-9131-d6ad94f2ce0e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3767368c9da8c97cd081787c0945a15552a1da46
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59092667"
---
# <a name="icordebugeval2-interface"></a>ICorDebugEval2, interface

Étend « ICorDebugEval » pour prendre en charge pour les types génériques.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[CallParameterizedFunction, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-callparameterizedfunction-method.md)|Définit un appel à « ICorDebugFunction spécifié », qui peut être imbriqué à l’intérieur d’un type dont le constructeur prend des paramètres de type, ou peut prendre lui-même des paramètres de type.|  
|[CreateValueForType, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-createvaluefortype-method.md)|Obtient un pointeur vers un nouvel « ICorDebugValue » du type spécifié, avec une valeur initiale de zéro ou null.|  
|[NewParameterizedArray, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedarray-method.md)|Alloue un nouveau tableau du type d’élément spécifié et des dimensions.|  
|[NewParameterizedObject, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedobject-method.md)|Instancie un nouvel objet de type paramétré et appelle la méthode de constructeur de l’objet.|  
|[NewParameterizedObjectNoConstructor, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedobjectnoconstructor-method.md)|Instancie un nouvel objet de type paramétrable de la classe spécifiée sans essayer d’appeler une méthode de constructeur|  
|[NewStringWithLength, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newstringwithlength-method.md)|Crée une nouvelle chaîne de la longueur spécifiée avec le contenu spécifié.|  
|[RudeAbort, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-rudeabort-method.md)|Abandonne le calcul que ce `ICorDebugEval2` en cours d’exécution.|  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
