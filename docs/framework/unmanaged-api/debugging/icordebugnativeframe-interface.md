---
title: ICorDebugNativeFrame Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame
helpviewer_keywords:
- ICorDebugNativeFrame interface [.NET Framework debugging]
ms.assetid: 04819c58-7246-4b32-befb-680cf1dbc436
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7996d5800e99d8e6161e24f34604aff3e4e906bd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33422001"
---
# <a name="icordebugnativeframe-interface1"></a>ICorDebugNativeFrame Interface1
Implémentation spécialisée de ICorDebugFrame utilisée pour les frames natifs.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[CanSetIP, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-cansetip-method.md)|Obtient une valeur qui indique s’il est possible de définir le pointeur d’instruction à l’emplacement de décalage spécifié dans le code natif.|  
|[GetIP, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-getip-method.md)|Obtient l’offset du frame de pile en code natif.|  
|[GetLocalDoubleRegisterValue, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-getlocaldoubleregistervalue-method.md)|Obtient un pointeur vers un ICorDebugValue qui représente la valeur d’un argument ou une variable locale stockée dans deux registres de mémoire d’un frame natif.|  
|[GetLocalMemoryRegisterValue, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-getlocalmemoryregistervalue-method.md)|Obtient un pointeur vers un `ICorDebugValue` qui représente la valeur d’une variable locale, dont les bits de poids faibles sont stockés dans le Registre spécifié et les bits de poids fort sont stockés à l’adresse mémoire spécifiée.|  
|[GetLocalMemoryValue, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-getlocalmemoryvalue-method.md)|Obtient un pointeur vers un `ICorDebugValue` qui représente la valeur d’une variable locale stockée à l’adresse mémoire spécifiée.|  
|[GetLocalRegisterMemoryValue, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-getlocalregistermemoryvalue-method.md)|Obtient un pointeur vers un `ICorDebugValue` qui représente la valeur d’une variable locale, dont les bits de poids fort sont stockés dans le Registre spécifié et les bits de poids faibles sont stockés à l’adresse mémoire spécifiée|  
|[GetLocalRegisterValue, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-getlocalregistervalue-method.md)|Obtient un pointeur vers un `ICorDebugValue` qui représente la valeur d’un argument ou une variable locale stockée dans le Registre natif spécifié.|  
|[GetRegisterSet, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-getregisterset-method.md)|Obtient un pointeur vers un [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) qui représente le Registre défini pour ce `ICorDebugNativeFrame`.|  
|[SetIP, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-setip-method.md)|Définit le pointeur d’instruction à l’emplacement de décalage spécifié dans le code natif.|  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
