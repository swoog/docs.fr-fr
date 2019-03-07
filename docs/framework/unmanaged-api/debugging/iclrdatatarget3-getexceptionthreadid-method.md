---
title: ICLRDataTarget3::GetExceptionThreadID, méthode
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICLRDataTarget3.GetExceptionThreadID
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 307d6ac7-4a86-45f3-999d-6b47004a68f2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: de3606e4763596038a2c573002d774c6348071e8
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57473511"
---
# <a name="iclrdatatarget3getexceptionthreadid-method"></a>ICLRDataTarget3::GetExceptionThreadID, méthode
Appelée par les services d'accès aux données de CLR (Common Language Runtime) pour obtenir l'ID du thread qui a levé l'exception.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp  
HRESULT GetExceptionThreadID(  
    [out] ULONG32* threadID  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `threadID`  
 [en sortie] L'ID du thread qui a levé l'exception.  
  
## <a name="return-value"></a>Valeur de retour  
 La valeur de retour est `S_OK` en cas de réussite ou un code d'échec `HRESULT` en cas d'échec. Les codes `HRESULT` peuvent comprendre, sans y être limités, ce qui suit :  
  
|Code de retour|Description|  
|-----------------|-----------------|  
|`S_OK`|La méthode a réussi.|  
|`HRESULT_FROM_WIN32(ERROR_NOT_FOUND)`|Impossible de trouver un ID de thread valide pour l'exception.|  
  
## <a name="remarks"></a>Notes  
 Cette méthode est implémentée par le writer de l'application de débogage.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** ClrData.idl, ClrData.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[v451_update](../../../../includes/net-current-v451-nov-plus.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICLRDataTarget3, interface](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-interface.md)
- [GetExceptionContextRecord, méthode](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptioncontextrecord-method.md)
- [GetExceptionRecord, méthode](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptionrecord-method.md)
