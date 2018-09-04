---
title: _AxlGetIssuerPublicKeyHash, fonction
ms.date: 03/30/2017
api_name:
- _AxlGetIssuerPublicKeyHash
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: fb626b41-b888-4625-84c3-2c02b5e3866f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 408b71bf38427d12418e05f8b509fe841bc95ef1
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43563674"
---
# <a name="axlgetissuerpublickeyhash-function"></a>_AxlGetIssuerPublicKeyHash, fonction
Récupère le hachage SHA-1 de la clé publique associée à la clé privée utilisée pour signer le certificat spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT _AxlGetIssuerPublicKeyHash (  
    [in]  IN PCRYPT_DATA_BLOB   pChainContext,  
    [out] LPWSTR                *ppwszPublicKeyHash  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pChainContext`  
 [en entrée] L'objet blob de clé publique CSP. Consultez le [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) structure.  
  
 `ppwszPublicKeyHash`  
 [en sortie] Un pointeur vers WCHAR * pour recevoir le jeton de clé publique codé en hexadécimal.  
  
## <a name="return-value"></a>Valeur de retour  
 `S_OK` si la fonction réussit, sinon `S_FALSE`.  
  
## <a name="see-also"></a>Voir aussi  
 [Authenticode](../../../../docs/framework/unmanaged-api/authenticode/index.md)
