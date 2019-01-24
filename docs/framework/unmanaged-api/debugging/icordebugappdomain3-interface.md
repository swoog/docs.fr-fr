---
title: ICorDebugAppDomain3, interface
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain3
helpviewer_keywords:
- ICorDebugAppDomain3 interface [.NET Framework debugging]
ms.assetid: 875ef5be-c1e7-4d95-97e9-d3a667aeaba0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ade4c88f4431dd6db636ea2581bdb936ac8d8e5f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54538009"
---
# <a name="icordebugappdomain3-interface"></a>ICorDebugAppDomain3, interface
Fournit des méthodes pour récupérer des informations sur les représentations sous forme managées de [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types actuellement chargés dans un domaine d’application. Cette interface est une extension des interfaces ICorDebugAppDomain et ICorDebugAppDomain2.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[ICorDebugAppDomain3::GetCachedWinRTTypes](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain3-getcachedwinrttypes-method.md)|Obtient un énumérateur pour toutes les mises en cache [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types.|  
|[ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain3-getcachedwinrttypesforiids-method.md)|Obtient un énumérateur pour la mise en cache [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types dans un domaine d’application basés sur leurs identificateurs de l’interface.|  
  
## <a name="remarks"></a>Notes  
 Cette interface est destinée à être utilisée par un débogueur conjointement avec un appel à la fonction d’évaluation `M:System.Runtime.InteropServices.Marshal.GetInspectableIIDs(System.Object)`. Lorsque la méthode récupère les identificateurs d’interface pris en charge par un [!INCLUDE[wrt](../../../../includes/wrt-md.md)] l’objet de serveur, le débogueur peut utiliser les méthodes définies dans cette interface pour le mappage des types managés qui correspondent à ces interfaces.  
  
 Pour récupérer une instance de cette interface, exécutez `QueryInterface` sur une instance de l’interface ICorDebugAppDomain ou ICorDebugAppDomain2.  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
