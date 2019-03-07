---
title: StrongNameCompareAssemblies, fonction
ms.date: 03/30/2017
api_name:
- StrongNameCompareAssemblies
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameCompareAssemblies
helpviewer_keywords:
- StrongNameCompareAssemblies function [.NET Framework strong naming]
ms.assetid: 763f2375-efc6-4219-8806-a3b0567ef72b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: dd3813d977f94db4168da8c888485b323f4072ad
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57471275"
---
# <a name="strongnamecompareassemblies-function"></a>StrongNameCompareAssemblies, fonction
Détermine si deux assemblys diffèrent uniquement par leurs signatures avec nom fort.  
  
 Cette fonction a été déconseillée. Utilisez le [ICLRStrongName::StrongNameCompareAssemblies](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamecompareassemblies-method.md) méthode à la place.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
BOOLEAN StrongNameCompareAssemblies (  
    [in]  LPCWSTR   wszAssembly1,  
    [in]  LPCWSTR   wszAssembly2,  
    [out] DWORD     *pdwResult  
);  
```  
  
## <a name="parameters"></a>Paramètres  
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
 `true` de réussite ; Sinon, `false`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** StrongName.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="remarks"></a>Notes  
 La signature de nom fort d’un assembly se compose du nom de texte, version, culture et jeton de clé publique de l’assembly.  
  
 Si le `StrongNameCompareAssemblies` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.  
  
## <a name="see-also"></a>Voir aussi
- [StrongNameCompareAssemblies, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamecompareassemblies-method.md)
- [ICLRStrongName, interface](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
