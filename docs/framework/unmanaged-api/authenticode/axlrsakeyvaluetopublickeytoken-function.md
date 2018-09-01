---
title: _AxlRSAKeyValueToPublicKeyToken, fonction
ms.date: 03/30/2017
api_name:
- _AxlRSAKeyValueToPublicKeyToken
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: d60f19fe-7bec-47ba-b60e-ba9ce66abf8c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e09391af9b5d71cfa423b3bf1a2b307117d0dee1
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43385885"
---
# <a name="axlrsakeyvaluetopublickeytoken-function"></a><span data-ttu-id="34765-102">\_AxlRSAKeyValueToPublicKeyToken (fonction)</span><span class="sxs-lookup"><span data-stu-id="34765-102">\_AxlRSAKeyValueToPublicKeyToken function</span></span>

<span data-ttu-id="34765-103">Convertit un modulo et un exposant en un jeton de clé publique de nom fort.</span><span class="sxs-lookup"><span data-stu-id="34765-103">Converts a Modulus and Exponent to a strong name public key token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="34765-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34765-104">Syntax</span></span>  
  
```  
HRESULT _AxlRSAKeyValueToPublicKeyToken (  
    [in]  PCRYPT_DATA_BLOB pModulusBlob,  
    [in]  PCRYPT_DATA_BLOB pExponentBlob,  
    [out] LPWSTR           *ppwszPublicKeyToken  
);  
```  
  
### <a name="parameters"></a><span data-ttu-id="34765-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34765-105">Parameters</span></span>  
 `pModulusBlob`  
 <span data-ttu-id="34765-106">[in] L’objet blob Modulus codé en base64 (à partir de la \<modulo > élément).</span><span class="sxs-lookup"><span data-stu-id="34765-106">[in] The base64-encoded Modulus blob (from the \<Modulus> element).</span></span>  <span data-ttu-id="34765-107">Consultez le [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) structure.</span><span class="sxs-lookup"><span data-stu-id="34765-107">See the [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) structure.</span></span>  
  
 `pExponentBlob`  
 <span data-ttu-id="34765-108">[in] L’objet blob Exponent codé en base64 (à partir de la \<exposant > élément).</span><span class="sxs-lookup"><span data-stu-id="34765-108">[in] The base64-encoded Exponent blob (from the \<Exponent> element).</span></span> <span data-ttu-id="34765-109">Consultez le [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) structure.</span><span class="sxs-lookup"><span data-stu-id="34765-109">See the [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) structure.</span></span>  
  
 `ppwszPublicKeyToken`  
 <span data-ttu-id="34765-110">[en sortie] Un pointeur vers WCHAR \* pour recevoir le jeton de clé publique codé en hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="34765-110">[out] A pointer to WCHAR \* to receive the hex-encoded public key token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="34765-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="34765-111">Return Value</span></span>  
 <span data-ttu-id="34765-112">`S_OK` si la fonction réussit.</span><span class="sxs-lookup"><span data-stu-id="34765-112">`S_OK` if the function succeeds.</span></span> <span data-ttu-id="34765-113">Sinon, retourne un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="34765-113">Otherwise, returns an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="34765-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34765-114">See Also</span></span>  
 [<span data-ttu-id="34765-115">Authenticode</span><span class="sxs-lookup"><span data-stu-id="34765-115">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
