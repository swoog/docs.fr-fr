---
title: ICorDebugStepper, interface
ms.date: 03/30/2017
api_name:
- ICorDebugStepper
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper
helpviewer_keywords:
- ICorDebugStepper interface [.NET Framework debugging]
ms.assetid: ed8364eb-f01b-46f6-b5e3-5dda9cae2dfe
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f83b9796bb692ce234a03c596387960bd879ebf3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61763735"
---
# <a name="icordebugstepper-interface"></a>ICorDebugStepper, interface
Représente dans l'exécution du code une étape qui est effectuée par un débogueur, et qui sert d'identificateur entre l'émission et l'achèvement d'une commande tout en offrant un moyen d'annuler une étape.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Deactivate, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-deactivate-method.md)|Cela entraîne `ICorDebugStepper` pour annuler la dernière commande reçue.|  
|[IsActive, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-isactive-method.md)|Obtient une valeur qui indique si ce `ICorDebugStepper` exécute actuellement une étape.|  
|[SetInterceptMask, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setinterceptmask-method.md)|Définit une valeur CorDebugIntercept qui spécifie les types de code sont détaillé.|  
|[SetRangeIL, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setrangeil-method.md)|Définit une valeur qui indique si les appels à [ICorDebugStepper::StepRange](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-steprange-method.md) valeurs d’argument par rapport à du code natif ou pour le code Microsoft intermediate language (MSIL) de la méthode qui est en cours a présenté.|  
|[SetUnmappedStopMask, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setunmappedstopmask-method.md)|Définit une valeur CorDebugUnmappedStop qui spécifie le type de code non mappé dans lequel l’exécution s’arrêtera.|  
|[Step, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-step-method.md)|Cela entraîne `ICorDebugStepper` à pas son thread conteneur et éventuellement, continuez le pas à pas via des fonctions appelées dans le thread.|  
|[StepOut, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-stepout-method.md)|Cela entraîne `ICorDebugStepper` à pas son thread conteneur et se termine lorsque le frame actuel retourne le contrôle au frame appelant.|  
|[StepRange, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-steprange-method.md)|Cela entraîne `ICorDebugStepper` à pas son thread conteneur et à retourner lorsqu’il atteint le code au-delà de la dernière des plages spécifiées.|  
  
## <a name="remarks"></a>Notes  
 Le `ICorDebugStepper` interface utilisé aux fins suivantes :  
  
- Il agit comme un identificateur entre une commande d’étape qui est émise et la fin de cette commande.  
  
- Il fournit une interface centrale pour encapsuler le pas à pas qui peut être effectuée.  
  
- Elle offre un moyen prématurément annuler une opération pas à pas.  
  
 Il peut y avoir plus d’une exécution pas à pas par thread. Par exemple, un point d’arrêt peut être atteint lors de l’exécution pas à pas sur une fonction, et l’utilisateur peut souhaiter démarrer une nouvelle opération pas à pas à l’intérieur de cette fonction. Il incombe au débogueur de déterminer comment gérer cette situation. Le débogueur peut être amené à annuler l’opération pas à pas d’origine ou imbriquer les deux opérations. Le `ICorDebugStepper` interface prend en charge les deux choix.  
  
 Une exécution pas à pas peut migrer entre des threads si le common language runtime (CLR) effectue un appel marshalé entre les threads.  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
