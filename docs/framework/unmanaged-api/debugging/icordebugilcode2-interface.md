---
title: ICorDebugILCode2, interface
ms.date: 03/30/2017
api_name:
- ICorDebugILCode2
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: f9dc2afd-df8a-464d-bdbf-5af0a1d4bf85
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1982226e90792d4bbda1cb023d80dec96fcb2060
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33418104"
---
# <a name="icordebugilcode2-interface"></a>ICorDebugILCode2, interface
[Pris en charge dans .NET Framework 4.5.2 et ultérieur]  
  
 Étend logiquement le [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md) interface pour fournir des méthodes qui retournent le jeton de signature de variable locale d’une fonction et qui mappent le langage intermédiaire instrumenté d’un profileur (il Intermediate Language) aux offsets IL de méthode d’origine décalages.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetInstrumentedILMap, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode2-getinstrumentedilmap-method.md)|Retourne un mappage des décalages du langage intermédiaire instrumenté par le profileur avec les décalages du langage intermédiaire de la méthode d'origine pour cette instance.|  
|[GetLocalVarSigToken, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode2-getlocalvarsigtoken-method.md)|Obtient le jeton de métadonnées de la signature de variable locale pour la fonction représentée par cette instance.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICorDebugILCode, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md)  
 [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
