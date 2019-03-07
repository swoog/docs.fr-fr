---
title: FunctionTailcall2 (fonction)
ms.date: 03/30/2017
api_name:
- FunctionTailcall2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionTailcall2
helpviewer_keywords:
- FunctionTailcall2 function [.NET Framework profiling]
ms.assetid: 249f9892-b5a9-41e1-b329-28a925904df6
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8491f80c1b4340756c00b5540520bd76f0f583a0
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57486993"
---
# <a name="functiontailcall2-function"></a>FunctionTailcall2 (fonction)
Notifie le profileur que la fonction en cours d’exécution est sur le point d’effectuer un appel tail à une autre fonction et fournit des informations sur le frame de pile.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
void __stdcall FunctionTailcall2 (  
    [in] FunctionID         funcId,   
    [in] UINT_PTR           clientData,   
    [in] COR_PRF_FRAME_INFO func  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `funcId`  
 [in] L’identificateur de la fonction en cours d’exécution qui doit faire un appel tail.  
  
 `clientData`  
 [in] Identificateur de fonction remappée, que le profileur spécifié précédemment via [FunctionIDMapper](../../../../docs/framework/unmanaged-api/profiling/functionidmapper-function.md), de la fonction en cours d’exécution qui doit faire un appel tail.  
  
 `func`  
 [in] Un `COR_PRF_FRAME_INFO` valeur qui pointe vers des informations sur le frame de pile.  
  
 Le profileur doit traiter ceci comme un handle opaque qui peut être passé au moteur d’exécution dans le [ICorProfilerInfo2::GetFunctionInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getfunctioninfo2-method.md) (méthode).  
  
## <a name="remarks"></a>Notes  
 La fonction de la cible de l’appel tail utilisera le frame de pile actuel et retournera directement à l’appelant de la fonction qui fait l’appel tail. Cela signifie qu’un [FunctionLeave2](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md) rappel ne sera pas émis pour une fonction qui est la cible d’un appel tail.  
  
 La valeur de la `func` paramètre n’est pas valide après la `FunctionTailcall2` fonction retourne, car la valeur peut changer ou être détruite.  
  
 Le `FunctionTailcall2` fonction est un rappel ; vous devez l’implémenter. L’implémentation doit utiliser le `__declspec`(`naked`) attribut de classe de stockage.  
  
 Le moteur d’exécution n’enregistre pas les registres avant d’appeler cette fonction.  
  
-   À l’entrée, vous devez enregistrer tous les registres que vous utilisez, y compris celles dans l’unité de virgule flottante (FPU).  
  
-   À la sortie, vous devez restaurer la pile en dépilant tous les paramètres qui ont été envoyés par son appelant.  
  
 L’implémentation de `FunctionTailcall2` ne doivent pas bloquer, car il sera retarder le garbage collection. L’implémentation ne doit pas tenter un garbage collection, car la pile est peut-être pas à l’état garbage collection convivial. Si un garbage collection est tenté, le runtime bloque jusqu'à ce que `FunctionTailcall2` retourne.  
  
 En outre, le `FunctionTailcall2` (fonction) ne doit pas appeler dans du code managé ou de quelque manière qu’une allocation de mémoire managée.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [FunctionEnter2, fonction](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md)
- [FunctionLeave2, fonction](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md)
- [SetEnterLeaveFunctionHooks2, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md)
- [Fonctions statiques globales de profilage](../../../../docs/framework/unmanaged-api/profiling/profiling-global-static-functions.md)
