---
title: ICorDebugStepper::SetUnmappedStopMask, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugStepper.SetUnmappedStopMask
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper::SetUnmappedStopMask
helpviewer_keywords:
- ICorDebugStepper::SetUnmappedStopMask method [.NET Framework debugging]
- SetUnmappedStopMask method [.NET Framework debugging]
ms.assetid: b1211981-e90c-4e05-8def-fa18d85ad9ab
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: da799b0d4f4e5e4b281445baa35d95f992ba0b63
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61987452"
---
# <a name="icordebugsteppersetunmappedstopmask-method"></a>ICorDebugStepper::SetUnmappedStopMask, méthode
Définit une valeur qui spécifie le type de code non mappé dans lequel l’exécution s’arrêtera.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetUnmappedStopMask (  
    [in] CorDebugUnmappedStop   mask  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `mask`  
 [in] Une valeur de l’énumération CorDebugUnmappedStop qui spécifie le type de code non mappé dans lequel le débogueur arrêtera l’exécution.  
  
 La valeur par défaut est STOP_OTHER_UNMAPPED. La valeur STOP_UNMANAGED est uniquement valide avec le débogage d’interopérabilité.  
  
## <a name="remarks"></a>Notes  
 Lorsque le débogueur trouve une compilation juste-à-temps (JIT) n’a aucun mappage correspondant à Microsoft intermediate language (MSIL), il arrête l’exécution si l’indicateur qui spécifie ce type de code non mappé a été défini ; le cas contraire, pas à pas détaillé en toute transparence continue.  
  
 Si le débogueur n’utilise pas une exécution pas à pas pour une méthode d’entrée, puis il ne sont pas nécessairement effectuer un survol code non mappé.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
