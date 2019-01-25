---
title: Méthode ICLRStrongName::StrongNameCompareAssemblies
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameCompareAssemblies
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameCompareAssemblies
helpviewer_keywords:
- ICLRStrongName::StrongNameCompareAssemblies method [.NET Framework hosting]
- StrongNameCompareAssemblies method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: b1fb356c-72cf-4aa4-8376-f291a6d97c01
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 23d5e2f586f63cbd21dcb6e5da3445153f4a9db3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54683388"
---
# <a name="iclrstrongnamestrongnamecompareassemblies-method"></a>Méthode ICLRStrongName::StrongNameCompareAssemblies
Détermine si deux assemblys diffèrent uniquement par leurs signatures avec nom fort.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT StrongNameCompareAssemblies (  
    [in]  LPCWSTR   wszAssembly1,  
    [in]  LPCWSTR   wszAssembly2,  
    [out] DWORD     *pdwResult  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `wszAssembly1`  
 [in] Le chemin d’accès à l’assembly en premier.  
  
 `wszAssembly2`  
 [in] Le chemin d’accès au deuxième assembly.  
  
 `pdwResult`  
 [out] Une des valeurs suivantes :  
  
-   `SN_CMP_DIFFERENT` (0) : Spécifie que les assemblys contiennent des données différentes.  
  
-   `SN_CMP_IDENTICAL` (1) - Spécifie que les assemblys sont exactement identiques, y compris leurs signatures et la somme de contrôle.  
  
-   `SN_CMP_SIGONLY` (2) : Spécifie que les assemblys diffèrent uniquement par la signature et la somme de contrôle.  
  
## <a name="return-value"></a>Valeur de retour  
 `S_OK` Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (consultez [valeurs HRESULT courantes](https://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MetaHost.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="remarks"></a>Notes  
 La signature de nom fort d’un assembly se compose du nom de texte, version, culture et jeton de clé publique de l’assembly.  
  
## <a name="see-also"></a>Voir aussi
- [ICLRStrongName, interface](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
