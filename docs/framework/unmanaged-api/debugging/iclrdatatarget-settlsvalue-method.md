---
title: ICLRDataTarget::SetTLSValue, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.SetTLSValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::SetTLSValue
helpviewer_keywords:
- ICLRDataTarget::SetTLSValue method [.NET Framework debugging]
- SetTLSValue method [.NET Framework debugging]
ms.assetid: 4a2d6a24-749a-47ad-9f01-4517203d3f35
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4c0be35772b10d89f90da5b33f47aa781034b13a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59152930"
---
# <a name="iclrdatatargetsettlsvalue-method"></a>ICLRDataTarget::SetTLSValue, méthode
Définit une valeur dans le stockage local des threads (TLS) du thread spécifié dans le processus cible. Cette méthode est appelée par les services d’accès de données common language runtime (CLR).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetTLSValue (  
    [in] ULONG32            threadID,  
    [in] ULONG32            index,  
    [in] CLRDATA_ADDRESS    value  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `threadID`  
 [in] L’identificateur de système d’exploitation d’un thread dans le processus cible.  
  
 `index`  
 [in] Index de l’emplacement. Cette valeur doit être un index valide dans le magasin local du thread spécifié.  
  
 `value`  
 [in] Un `CLRDATA_ADDRESS` valeur qui spécifie la valeur à placer dans l’emplacement TLS donné.  
  
## <a name="remarks"></a>Notes  
 Cette méthode est implémentée par le writer de l'application de débogage.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** ClrData.idl, ClrData.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICLRDataTarget, interface](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
