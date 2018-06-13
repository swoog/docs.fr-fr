---
title: CertTimestampAuthenticodeLicense, fonction
ms.date: 03/30/2017
api_name:
- CertTimestampAuthenticodeLicense
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: d468325a-21c5-43ce-8567-84e342b22308
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b110adac8c1ae68a3918a9e0fdf3f3eb4d017f0f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33406206"
---
# <a name="certtimestampauthenticodelicense-function"></a><span data-ttu-id="f29f3-102">CertTimestampAuthenticodeLicense, fonction</span><span class="sxs-lookup"><span data-stu-id="f29f3-102">CertTimestampAuthenticodeLicense Function</span></span>
<span data-ttu-id="f29f3-103">Horodate une licence XrML Authenticode.</span><span class="sxs-lookup"><span data-stu-id="f29f3-103">Time-stamps an Authenticode XrML license.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f29f3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f29f3-104">Syntax</span></span>  
  
```  
HRESULT CertTimestampAuthenticodeLicense (  
    [in]  PCRYPT_DATA_BLOB   pSignedLicenseBlob,  
    [in]  LPCWSTR            pwszTimestampURI,  
    [out] PCRYPT_DATA_BLOB   pTimestampSignatureBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f29f3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f29f3-105">Parameters</span></span>  
 `pSignedLicenseBlob`  
 <span data-ttu-id="f29f3-106">[en entrée] La licence XrML Authenticode signée à horodater.</span><span class="sxs-lookup"><span data-stu-id="f29f3-106">[in] The signed Authenticode XrML license to be time-stamped.</span></span> <span data-ttu-id="f29f3-107">Consultez le [CRYPTOAPI_BLOB](http://msdn.microsoft.com/library/windows/desktop/aa380238.aspx) structure.</span><span class="sxs-lookup"><span data-stu-id="f29f3-107">See the [CRYPTOAPI_BLOB](http://msdn.microsoft.com/library/windows/desktop/aa380238.aspx) structure.</span></span>  
  
 `pwszTimestampURI`  
 <span data-ttu-id="f29f3-108">[en entrée] L'URI du server d'horodatage.</span><span class="sxs-lookup"><span data-stu-id="f29f3-108">[in] The time-stamp server's URI.</span></span>  
  
 `pTimestampSignatureBlob`  
 <span data-ttu-id="f29f3-109">[en sortie] Un pointeur vers CRYPT_DATA_BLOB pour recevoir la signature de l'horodatage codé en base64.</span><span class="sxs-lookup"><span data-stu-id="f29f3-109">[out] A pointer to CRYPT_DATA_BLOB to receive the base64-encoded time-stamp signature.</span></span> <span data-ttu-id="f29f3-110">Il incombe l’appelant de libérer `pTimestampSignatureBlob` -> `pbData` avec `HepFree()` après utilisation.</span><span class="sxs-lookup"><span data-stu-id="f29f3-110">It is the caller's responsibility to free `pTimestampSignatureBlob`->`pbData` with `HepFree()` after use.</span></span> <span data-ttu-id="f29f3-111">Consultez le [CRYPTOAPI_BLOB](http://msdn.microsoft.com/library/windows/desktop/aa380238.aspx) structure.</span><span class="sxs-lookup"><span data-stu-id="f29f3-111">See the [CRYPTOAPI_BLOB](http://msdn.microsoft.com/library/windows/desktop/aa380238.aspx) structure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f29f3-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f29f3-112">Remarks</span></span>  
 <span data-ttu-id="f29f3-113">La signature de l'horodatage est en réalité un message PKCS #7 SignedData dont le contenu est la forme binaire de la valeur de SignatureValue de la signature de la licence.</span><span class="sxs-lookup"><span data-stu-id="f29f3-113">The time-stamp signature is actually a PKCS #7 SignedData message whose content is the binary form of the SignatureValue from the license's signature.</span></span> <span data-ttu-id="f29f3-114">Ceci agit comme une contre-signature de la licence.</span><span class="sxs-lookup"><span data-stu-id="f29f3-114">Basically, this acts as a counter-signature of the license.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f29f3-115">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f29f3-115">Return Value</span></span>  
 <span data-ttu-id="f29f3-116">`S_OK` si la fonction réussit.</span><span class="sxs-lookup"><span data-stu-id="f29f3-116">`S_OK` if the function succeeds.</span></span> <span data-ttu-id="f29f3-117">Sinon, retourne un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="f29f3-117">Otherwise, returns an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f29f3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f29f3-118">See Also</span></span>  
 [<span data-ttu-id="f29f3-119">Authenticode</span><span class="sxs-lookup"><span data-stu-id="f29f3-119">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
