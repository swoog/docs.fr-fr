---
title: GetHashFromAssemblyFileW, fonction
ms.date: 03/30/2017
api_name:
- GetHashFromAssemblyFileW
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromAssemblyFileW
helpviewer_keywords:
- GetHashFromAssemblyFileW function [.NET Framework strong naming]
ms.assetid: d1b2b172-5353-42af-a877-cf653c68ece0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 832d66eee14680870e70f1e0e8d40987eff3257f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33457572"
---
# <a name="gethashfromassemblyfilew-function"></a>GetHashFromAssemblyFileW, fonction
Obtient un hachage du fichier d’assembly spécifié, à l’aide de l’algorithme de hachage spécifié. Le chemin d’accès au fichier d’assembly doit être spécifié sous forme de chaîne Unicode.  
  
 Cette fonction est déconseillée. Utilisez le [ICLRStrongName::GetHashFromAssemblyFileW](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfilew-method.md) méthode à la place.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetHashFromAssemblyFileW (  
    [in]  LPCWSTR   wszFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE      *pbHash,  
    [in]  DWORD     cchHash,  
    [out] DWORD     *pchHash  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `wszFilePath`  
 [in] Le chemin d’accès au fichier à hacher. Ce paramètre doit être une chaîne Unicode.  
  
 `piHashAlg`  
 [dans, out] Constante qui spécifie l’algorithme de hachage. Utilisez zéro pour l’algorithme de hachage par défaut.  
  
 `pbHash`  
 [out] La mémoire tampon de hachage retournée.  
  
 `cchHash`  
 [in] La taille maximum demandée `pbHash`.  
  
 `pchHash`  
 [out] Le retournée, la taille, en octets, `pbHash`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** StrongName.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [GetHashFromAssemblyFileW, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfilew-method.md)  
 [GetHashFromAssemblyFile, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfile-method.md)  
 [ICLRStrongName, interface](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
