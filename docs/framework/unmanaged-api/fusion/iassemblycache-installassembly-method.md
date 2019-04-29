---
title: IAssemblyCache::InstallAssembly, méthode
ms.date: 03/30/2017
api_name:
- IAssemblyCache.InstallAssembly
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCache::InstallAssembly
helpviewer_keywords:
- InstallAssembly method [.NET Framework fusion]
- IAssemblyCache::InstallAssembly method [.NET Framework fusion]
ms.assetid: 33c1d269-c85e-4cb1-b0e6-1c510c8fb5fa
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7199fbc0c8760354269a50b647952729860c805b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61697548"
---
# <a name="iassemblycacheinstallassembly-method"></a>IAssemblyCache::InstallAssembly, méthode
Installe l’assembly spécifié dans le global assembly cache.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT InstallAssembly (  
    [in] DWORD dwFlags,  
    [in] LPCWSTR pszManifestFilePath,  
    [in] LPCFUSION_INSTALL_REFERENCE pRefData  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `dwFlags`  
 [in] Indicateurs définis dans Fusion.idl. Les valeurs suivantes sont prises en charge :  
  
- IASSEMBLYCACHE_INSTALL_FLAG_REFRESH (0x00000001)  
  
- IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH (0x00000002)  
  
 `pszManifestFilePath`  
 [in] Le chemin d’accès au manifeste de l’assembly à installer.  
  
 `pRefData`  
 [in] Un [FUSION_INSTALL_REFERENCE](../../../../docs/framework/unmanaged-api/fusion/fusion-install-reference-structure.md) structure qui contient les données pour l’installation.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Fusion.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IAssemblyCache, interface](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-interface.md)
