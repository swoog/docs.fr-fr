---
title: FunctionEnter3WithInfo, fonction
ms.date: 03/30/2017
api_name:
- FunctionEnter3WithInfo
api_location:
- mscorwks.cll
api_type:
- COM
f1_keywords:
- FunctionEnter3WithInfo
helpviewer_keywords:
- FunctionEnter3WithInfo function [.NET Framework profiling]
ms.assetid: 277c3344-d0cb-431e-beae-eb1eeeba8eea
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 16e086f54865307e116a9e522b2fbadee8502249
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61598946"
---
# <a name="functionenter3withinfo-function"></a>FunctionEnter3WithInfo, fonction
Notifie le profileur que le contrôle est passé à une fonction et fournit un handle qui peut être passé à la [ICorProfilerInfo3::GetFunctionEnter3Info, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-getfunctionenter3info-method.md) pour récupérer les arguments de fonction et de frame de pile.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
void __stdcall FunctionEnter3WithInfo(  
               [in] FunctionIDOrClientID functionIDOrClientID,  
               [in] COR_PRF_ELT_INFO eltInfo);  
```  
  
## <a name="parameters"></a>Paramètres  
 `functionIDOrClientID`  
 [in] L’identificateur de la fonction à laquelle le contrôle est passé.  
  
 `eltInfo`  
 [in] Handle opaque qui représente des informations sur un frame de pile donné. Ce handle est valide uniquement pendant le rappel auquel il est passé.  
  
## <a name="remarks"></a>Notes  
 Le `FunctionEnter3WithInfo` méthode de rappel notifie le profileur que les fonctions sont appelées et permet au profileur d’utiliser le [ICorProfilerInfo3::GetFunctionEnter3Info, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-getfunctionenter3info-method.md) pour inspecter les valeurs d’argument. Pour accéder aux informations d’argument, la `COR_PRF_ENABLE_FUNCTION_ARGS` indicateur doit être défini. Le profileur peut utiliser le [ICorProfilerInfo::SetEventMask, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md) pour définir les indicateurs d’événement, puis utiliser le [ICorProfilerInfo3::SetEnterLeaveFunctionHooks3WithInfo, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3withinfo-method.md) pour inscrire votre implémentation de cette fonction.  
  
 Le `FunctionEnter3WithInfo` fonction est un rappel ; vous devez l’implémenter. L’implémentation doit utiliser le `__declspec(naked)` attribut de classe de stockage.  
  
 Le moteur d’exécution n’enregistre pas les registres avant d’appeler cette fonction.  
  
- À l’entrée, vous devez enregistrer tous les registres que vous utilisez, y compris celles dans l’unité de virgule flottante (FPU).  
  
- À la sortie, vous devez restaurer la pile en dépilant tous les paramètres qui ont été envoyés par son appelant.  
  
 L’implémentation de `FunctionEnter3WithInfo` ne doivent pas bloquer, car il sera retarder le garbage collection. L’implémentation ne doit pas tenter un garbage collection, car la pile est peut-être pas dans un état de la collection convivial garbage. Si un garbage collection est tenté, le runtime bloque jusqu'à ce que `FunctionEnter3WithInfo` retourne.  
  
 Le `FunctionEnter3WithInfo` (fonction) ne doit pas appeler dans du code managé ou provoquer une allocation de mémoire managée en aucune façon.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [GetFunctionEnter3Info](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-getfunctionenter3info-method.md)
- [FunctionEnter3](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md)
- [FunctionLeave3](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md)
- [Fonctions statiques globales de profilage](../../../../docs/framework/unmanaged-api/profiling/profiling-global-static-functions.md)
