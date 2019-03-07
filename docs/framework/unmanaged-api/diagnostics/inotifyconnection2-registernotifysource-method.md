---
title: INotifyConnection2::RegisterNotifySource, méthode
ms.date: 03/30/2017
api_name:
- INotifyConnection2.RegisterNotifySource
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifyConnection2::RegisterNotifySource
helpviewer_keywords:
- INotifyConnection2::RegisterNotifySource method [.NET Framework debugging]
- RegisterNotifySource method [.NET Framework debugging]
ms.assetid: 2632da80-6e4b-4429-8dee-b382745a5f81
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0c08cac6fd6b467fe365989cb4d6780325bdaa90
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57501615"
---
# <a name="inotifyconnection2registernotifysource-method"></a>INotifyConnection2::RegisterNotifySource, méthode
Installe une source de notification spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT RegisterNotifySource  
(  
    [in]  INotifySource2*  in_pNotifySource,  
    [out] INotifySink2**   out_ppNotifySink  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `in_pNotifySource`  
 [in] Spécifie l’objet à utiliser comme source de notification.  
  
 `out_ppNotifySink`  
 [out] Reçoit l’objet à utiliser en tant que le récepteur de notification.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** ProtocolNotify2.idl  
  
## <a name="see-also"></a>Voir aussi
- [INotifyConnection2, interface](../../../../docs/framework/unmanaged-api/diagnostics/inotifyconnection2-interface.md)
- [INotifySource2, interface](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-interface.md)
- [INotifySink2, interface](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)
- [UnregisterNotifySource, méthode](../../../../docs/framework/unmanaged-api/diagnostics/inotifyconnection2-unregisternotifysource-method.md)
