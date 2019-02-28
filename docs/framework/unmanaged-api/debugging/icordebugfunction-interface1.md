---
title: ICorDebugFunction, interface
ms.date: 03/30/2017
api_name:
- ICorDebugFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction
helpviewer_keywords:
- ICorDebugFunction interface [.NET Framework debugging]
ms.assetid: 783faea9-8083-41c1-b04a-51a81ac4c8f3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0c2a4dc823768b722e9069c411be787a66989b2a
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56977108"
---
# <a name="icordebugfunction-interface"></a>ICorDebugFunction, interface

Représente une fonction ou une méthode managée.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[CreateBreakpoint, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-createbreakpoint-method.md)|Crée un point d’arrêt au début de cette fonction.|  
|[GetClass, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-getclass-method.md)|Obtient un objet ICorDebugClass qui représente la classe de que cette fonction est membre.|  
|[GetCurrentVersionNumber, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-getcurrentversionnumber-method.md)|Obtient le numéro de version de la dernière modification apportée à cette fonction.|  
|[GetILCode, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-getilcode-method.md)|Obtient le code de Microsoft intermediate language (MSIL) pour cette fonction.|  
|[GetLocalVarSigToken, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-getlocalvarsigtoken-method.md)|Obtient les métadonnées de jeton pour la signature de variable locale de la fonction qui est représentée par ce `ICorDebugFunction` instance.|  
|[GetModule, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-getmodule-method.md)|Obtient le module dans lequel cette fonction est définie.|  
|[GetNativeCode, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-getnativecode-method.md)|Obtient le code natif pour cette fonction.|  
|[GetToken, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-gettoken-method.md)|Obtient les métadonnées de jeton pour cette fonction.|  
  
## <a name="remarks"></a>Notes  
 Le `ICorDebugFunction` interface ne représente pas une fonction avec des paramètres de type générique. Par exemple, un `ICorDebugFunction` instance représenteraient `Func<T>` mais pas `Func<string>`. Appelez [ICorDebugILFrame2::EnumerateTypeParameters](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe2-enumeratetypeparameters-method.md) pour obtenir les paramètres de type générique.  
  
 La relation entre le jeton de métadonnées d’une méthode `mdMethodDef`et d’une méthode `ICorDebugFunction` objet dépend de si Modifier & Continuer est autorisé sur la fonction :  
  
-   Si Modifier & Continuer n’est pas autorisée sur la fonction, il existe une relation un à un entre le `ICorDebugFunction` objet et le `mdMethodDef` jeton. Autrement dit, la fonction a un `ICorDebugFunction` objet et l’autre `mdMethodDef` jeton.  
  
-   Si Modifier & Continuer est autorisé sur la fonction, il existe une relation plusieurs-à-un entre le `ICorDebugFunction` objet et le `mdMethodDef` jeton. Autrement dit, la fonction peut avoir plusieurs instances de `ICorDebugFunction`, un pour chaque version de la fonction, mais une seule `mdMethodDef` jeton.  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :**  CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
