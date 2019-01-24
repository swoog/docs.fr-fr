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
ms.openlocfilehash: 170961e366e9788e92fc484514bb349332419aea
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54678618"
---
# <a name="axlgetissuerpublickeyhash-function"></a><span data-ttu-id="6aeda-102">_AxlGetIssuerPublicKeyHash, fonction</span><span class="sxs-lookup"><span data-stu-id="6aeda-102">_AxlGetIssuerPublicKeyHash Function</span></span>
<span data-ttu-id="6aeda-103">Récupère le hachage SHA-1 de la clé publique associée à la clé privée utilisée pour signer le certificat spécifié.</span><span class="sxs-lookup"><span data-stu-id="6aeda-103">Retrieves the SHA-1 hash of the public key associated with the private key that is used to sign the specified certificate.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6aeda-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6aeda-104">Syntax</span></span>  
  
```  
HRESULT _AxlGetIssuerPublicKeyHash (  
    [in]  IN PCRYPT_DATA_BLOB   pChainContext,  
    [out] LPWSTR                *ppwszPublicKeyHash  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6aeda-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6aeda-105">Parameters</span></span>  
 `pChainContext`  
 <span data-ttu-id="6aeda-106">[en entrée] L'objet blob de clé publique CSP.</span><span class="sxs-lookup"><span data-stu-id="6aeda-106">[in] The CSP public key blob.</span></span> <span data-ttu-id="6aeda-107">Consultez le [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) structure.</span><span class="sxs-lookup"><span data-stu-id="6aeda-107">See the [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) structure.</span></span>  
  
 `ppwszPublicKeyHash`  
 <span data-ttu-id="6aeda-108">[en sortie] Un pointeur vers WCHAR \* pour recevoir le jeton de clé publique codé en hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="6aeda-108">[out] A pointer to WCHAR \* to receive the hex-encoded public key token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6aeda-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6aeda-109">Return Value</span></span>  
 <span data-ttu-id="6aeda-110">`S_OK` si la fonction réussit, sinon `S_FALSE`.</span><span class="sxs-lookup"><span data-stu-id="6aeda-110">`S_OK` if the function succeeds; otherwise `S_FALSE`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6aeda-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6aeda-111">See also</span></span>
- [<span data-ttu-id="6aeda-112">Authenticode</span><span class="sxs-lookup"><span data-stu-id="6aeda-112">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
