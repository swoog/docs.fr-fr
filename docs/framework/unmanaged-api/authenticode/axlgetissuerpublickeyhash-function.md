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
ms.openlocfilehash: 448712561f1531a055ac141db9825581525c779c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59106702"
---
# <a name="axlgetissuerpublickeyhash-function"></a><span data-ttu-id="979a0-102">_AxlGetIssuerPublicKeyHash, fonction</span><span class="sxs-lookup"><span data-stu-id="979a0-102">_AxlGetIssuerPublicKeyHash Function</span></span>
<span data-ttu-id="979a0-103">Récupère le hachage SHA-1 de la clé publique associée à la clé privée utilisée pour signer le certificat spécifié.</span><span class="sxs-lookup"><span data-stu-id="979a0-103">Retrieves the SHA-1 hash of the public key associated with the private key that is used to sign the specified certificate.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="979a0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="979a0-104">Syntax</span></span>  
  
```  
HRESULT _AxlGetIssuerPublicKeyHash (  
    [in]  IN PCRYPT_DATA_BLOB   pChainContext,  
    [out] LPWSTR                *ppwszPublicKeyHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="979a0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="979a0-105">Parameters</span></span>  
 `pChainContext`  
 <span data-ttu-id="979a0-106">[en entrée] L'objet blob de clé publique CSP.</span><span class="sxs-lookup"><span data-stu-id="979a0-106">[in] The CSP public key blob.</span></span> <span data-ttu-id="979a0-107">Consultez le [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) structure.</span><span class="sxs-lookup"><span data-stu-id="979a0-107">See the [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) structure.</span></span>  
  
 `ppwszPublicKeyHash`  
 <span data-ttu-id="979a0-108">[en sortie] Un pointeur vers WCHAR \* pour recevoir le jeton de clé publique codé en hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="979a0-108">[out] A pointer to WCHAR \* to receive the hex-encoded public key token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="979a0-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="979a0-109">Return Value</span></span>  
 <span data-ttu-id="979a0-110">`S_OK` si la fonction réussit ; sinon `S_FALSE`.</span><span class="sxs-lookup"><span data-stu-id="979a0-110">`S_OK` if the function succeeds; otherwise `S_FALSE`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="979a0-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="979a0-111">See also</span></span>

- [<span data-ttu-id="979a0-112">Authenticode</span><span class="sxs-lookup"><span data-stu-id="979a0-112">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
