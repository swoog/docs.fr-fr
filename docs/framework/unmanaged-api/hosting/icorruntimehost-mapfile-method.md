---
title: ICorRuntimeHost::MapFile, méthode
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.MapFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::MapFile
helpviewer_keywords:
- ICorRuntimeHost::MapFile method [.NET Framework hosting]
- MapFile method [.NET Framework hosting]
ms.assetid: 45ae0502-0a31-4342-b7e3-f36e1cf738f3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 814073b766d5d562b414a566ae3f92abd664ce35
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54707841"
---
# <a name="icorruntimehostmapfile-method"></a>ICorRuntimeHost::MapFile, méthode
Mappe le fichier spécifié dans la mémoire. Cette méthode est obsolète.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT MapFile(  
    [in]  HANDLE    hFile,  
    [out] HMODULE*  hMapAddress  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `hFile`  
 [in] Le handle du fichier à mapper.  
  
 `hMapAddress`  
 [out] L’adresse mémoire de départ à partir duquel commencer le fichier de mappage.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Version du .NET framework :** 1.0, 1.1  
  
## <a name="see-also"></a>Voir aussi
- [ICorRuntimeHost, interface](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
