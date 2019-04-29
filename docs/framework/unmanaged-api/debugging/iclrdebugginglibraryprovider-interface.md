---
title: ICLRDebuggingLibraryProvider, interface
ms.date: 03/30/2017
api_name:
- ICLRDebuggingLibraryProvider
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDebuggingLibraryProvider
helpviewer_keywords:
- ICLRDebuggingLibraryProvider interface [.NET Framework debugging]
ms.assetid: 67739617-6add-41a9-9de5-a3200c3109ce
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c62079a87c09bcbe09167a137fd39530652ae3e5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61697860"
---
# <a name="iclrdebugginglibraryprovider-interface"></a>ICLRDebuggingLibraryProvider, interface
Inclut le [ProvideLibrary, méthode](../../../../docs/framework/unmanaged-api/debugging/iclrdebugginglibraryprovider-providelibrary-method.md) (méthode), qui obtient un fournisseur de bibliothèque interface de rappel qui permet de common language runtime des bibliothèques de débogage spécifiques à la version être à la demande et le chargement.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[ProvideLibrary, méthode](../../../../docs/framework/unmanaged-api/debugging/iclrdebugginglibraryprovider-providelibrary-method.md)|Permet au débogueur de fournir un handle à un module qui peut être utilisé pour charger une bibliothèque de débogage.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
