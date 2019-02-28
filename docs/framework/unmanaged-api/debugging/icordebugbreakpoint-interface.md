---
title: ICorDebugBreakpoint, interface
ms.date: 03/30/2017
api_name:
- ICorDebugBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBreakpoint
helpviewer_keywords:
- ICorDebugBreakpoint interface [.NET Framework debugging]
ms.assetid: aa5ad3d7-e1bb-42af-99bc-471224e3bcaa
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a7e454c15ddfa977a6d06921a5d80a6c05dca92f
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56973572"
---
# <a name="icordebugbreakpoint-interface"></a>ICorDebugBreakpoint, interface

Représente un point d’arrêt dans une fonction ou un point de contrôle sur une valeur.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Activate, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugbreakpoint-activate-method.md)|Définit l’état actif de ce `ICorDebugBreakpoint`.|  
|[IsActive, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugbreakpoint-isactive-method.md)|Obtient une valeur qui indique si ce `ICorDebugBreakpoint` est actif.|  
  
## <a name="remarks"></a>Notes  
 Points d’arrêt ne prennent pas directement en charge les expressions conditionnelles. Si cette fonctionnalité est souhaitée, un débogueur doit implémenter en haut de `ICorDebugBreakpoint`.  
  
 Étend l’interface ICorDebugFunctionBreakpoint `ICorDebugBreakpoint` pour prendre en charge des points d’arrêt dans les fonctions.  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
