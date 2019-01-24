---
title: ICorDebugBreakpoint, Interface1
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
ms.openlocfilehash: a222f578daed0ab81e2136e00d6f9b032acd95fc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54744932"
---
# <a name="icordebugbreakpoint-interface1"></a>ICorDebugBreakpoint, Interface1
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
