---
title: INotifySink2::OnSyncCallReturn, méthode
ms.date: 03/30/2017
api_name:
- INotifySink2.OnSyncCallReturn
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifySink2::OnSyncCallReturn
helpviewer_keywords:
- OnSyncCallReturn method [.NET Framework debugging]
- INotifySink2::OnSyncCallReturn method [.NET Framework debugging]
ms.assetid: c1bda761-6292-4750-a14b-7d5db8f33456
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0adc6ec1db3f12d1850bb6ff9a01d5b6cc5f90c7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59157922"
---
# <a name="inotifysink2onsynccallreturn-method"></a>INotifySink2::OnSyncCallReturn, méthode
Appelée lorsqu’un appel est retourné.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT OnSyncCallReturn  
(  
    [in]  CALL_ID   in_CallID,  
    [in, size_is(in_BufferSize)] BYTE*  in_pBuffer,  
    [in]  DWORD     in_BufferSize  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `in_CallID`  
 [in] ID de l’appel retourné. Consultez [call_id, Structure](../../../../docs/framework/unmanaged-api/diagnostics/call-id-structure.md).  
  
 `in_pBuffer`  
 [in] Mémoire tampon d’appel.  
  
 `in_BufferSize`  
 [in] Taille de la mémoire tampon de l’appel, en octets.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit.  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** ProtocolNotify2.idl  
  
## <a name="see-also"></a>Voir aussi

- [INotifySink2, interface](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)
- [INotifySource2, interface](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-interface.md)
- [INotifyConnection2, interface](../../../../docs/framework/unmanaged-api/diagnostics/inotifyconnection2-interface.md)
