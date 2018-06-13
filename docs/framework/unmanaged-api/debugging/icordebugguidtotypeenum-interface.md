---
title: ICorDebugGuidToTypeEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugGuidToTypeEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGuidToTypeEnum
helpviewer_keywords:
- ICorDebugGuidToTypeEnum interface [.NET Framework debugging]
ms.assetid: aa32b12b-05fc-4ea8-a904-adae25034269
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 91d653587d5b7c35a2a43c7eed7c4bf33e5401f6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33416749"
---
# <a name="icordebugguidtotypeenum-interface"></a>ICorDebugGuidToTypeEnum, interface
Fournit un énumérateur qui définit le mappage entre un ensemble de GUID et leurs types correspondants, qui sont représentés par des instances ICorDebugType. Cette interface hérite des méthodes de l’interface de ICorDebugEnum.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[ICorDebugGuidToTypeEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugguidtotypeenum-next-method.md)|Obtient le nombre spécifié de [CorDebugGuidToTypeMapping](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md) instances qui correspondent à des informations de type GUID.|  
  
## <a name="remarks"></a>Notes  
 Un `ICorDebugGuidToTypeEnum` objet d’interface peut être récupéré en appelant le [ICorDebugAppDomain3::GetCachedWinRTTypes](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain3-getcachedwinrttypes-method.md) (méthode). Un débogueur peut appeler de cette interface [suivant](../../../../docs/framework/unmanaged-api/debugging/icordebugguidtotypeenum-next-method.md) pour récupérer [CorDebugGuidToTypeMapping](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md) les objets qui représentent les mappages de gérés représentations sous forme de [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types chargés dans le domaine d’application utilisé pour l’appel à la [ICorDebugAppDomain3::GetCachedWinRTTypes](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain3-getcachedwinrttypes-method.md) (méthode).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
