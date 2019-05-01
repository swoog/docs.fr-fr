---
title: ICorDebugStepper::StepRange, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugStepper.StepRange
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper::StepRange
helpviewer_keywords:
- StepRange method [.NET Framework debugging]
- ICorDebugStepper::StepRange method [.NET Framework debugging]
ms.assetid: b9776112-6e6d-4708-892a-8873db02e16f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7b18474aeaa79224de5371df3ff0cac5ed9bf4ff
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61994279"
---
# <a name="icordebugsteppersteprange-method"></a>ICorDebugStepper::StepRange, méthode
Provoque ICorDebugStepper pas à pas son thread conteneur et à retourner lorsqu’il atteint le code au-delà de la dernière des plages spécifiées.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT StepRange (  
    [in] BOOL     bStepIn,  
    [in, size_is(cRangeCount)] COR_DEBUG_STEP_RANGE ranges[],  
    [in] ULONG32  cRangeCount  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `bStepIn`  
 [in] La valeur `true` à l’étape dans une fonction qui est appelée dans le thread. La valeur `false` pour ignorer la fonction.  
  
 `ranges`  
 [in] Tableau de structures COR_DEBUG_STEP_RANGE, dont chacun spécifie une plage.  
  
 `cRangeCount`  
 [in] Taille du tableau `ranges`.  
  
## <a name="remarks"></a>Notes  
 Le `StepRange` méthode fonctionne comme le [ICorDebugStepper::Step](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-step-method.md) (méthode), sauf qu’elle ne se termine pas tant que le code en dehors de la plage donnée est atteinte.  
  
 Cela peut être plus efficace que l’exécution pas à pas d’une instruction à la fois. Les plages sont spécifiées comme une liste de paires d’offsets à partir du début du frame de d’exécution pas à pas.  
  
 Les plages sont relatives au code Microsoft intermediate language (MSIL) d’une méthode. Appelez [ICorDebugStepper::SetRangeIL](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setrangeil-method.md) avec `false` pour que les plages par rapport au code natif d’une méthode.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
