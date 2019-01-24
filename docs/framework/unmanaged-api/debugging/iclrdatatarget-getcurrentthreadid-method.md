---
title: ICLRDataTarget::GetCurrentThreadID, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.GetCurrentThreadID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::GetCurrentThreadID
helpviewer_keywords:
- GetCurrentThreadID method, ICLRDataTarget interface [.NET Framework debugging]
- ICLRDataTarget::GetCurrentThreadID method [.NET Framework debugging]
ms.assetid: dc9a0a6c-d592-4fb7-86ed-62684da3b0e1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fb1e0aec9ce746c3082ad9cc57b572cbca0fd7e0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54552259"
---
# <a name="iclrdatatargetgetcurrentthreadid-method"></a>ICLRDataTarget::GetCurrentThreadID, méthode
Obtient l’identificateur de système d’exploitation pour le thread actuel.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetCurrentThreadID (  
    [out] ULONG32    *threadID  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `threadID`  
 [out] Un pointeur vers l’identificateur de système d’exploitation du thread actuel pour le processus cible.  
  
## <a name="remarks"></a>Notes  
 S’il n’existe aucun thread actuel pour le processus cible, le `GetCurrentThreadID` méthode peut échouer.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** ClrData.idl, ClrData.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICLRDataTarget, interface](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
