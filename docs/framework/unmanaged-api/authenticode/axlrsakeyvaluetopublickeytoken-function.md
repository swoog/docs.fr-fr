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
ms.openlocfilehash: 7ef73f0f7599fdff887437756a5995591fd8ec89
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402407"
---
# <a name="axlrsakeyvaluetopublickeytoken-function"></a><span data-ttu-id="5f148-102">_AxlRSAKeyValueToPublicKeyToken, fonction</span><span class="sxs-lookup"><span data-stu-id="5f148-102">_AxlRSAKeyValueToPublicKeyToken Function</span></span>
<span data-ttu-id="5f148-103">Convertit un modulo et un exposant en un jeton de clé publique de nom fort.</span><span class="sxs-lookup"><span data-stu-id="5f148-103">Converts a Modulus and Exponent to a strong name public key token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f148-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f148-104">Syntax</span></span>  
  
```  
HRESULT _AxlRSAKeyValueToPublicKeyToken (  
    [in]  PCRYPT_DATA_BLOB pModulusBlob,  
    [in]  PCRYPT_DATA_BLOB pExponentBlob,  
    [out] LPWSTR           *ppwszPublicKeyToken  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5f148-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f148-105">Parameters</span></span>  
 `pModulusBlob`  
 <span data-ttu-id="5f148-106">[in] L’objet blob Modulus codé en base64 (à partir de la \<modulo > élément).</span><span class="sxs-lookup"><span data-stu-id="5f148-106">[in] The base64-encoded Modulus blob (from the \<Modulus> element).</span></span>  <span data-ttu-id="5f148-107">Consultez le [CRYPTOAPI_BLOB](http://msdn.microsoft.com/library/windows/desktop/aa380238.aspx) structure.</span><span class="sxs-lookup"><span data-stu-id="5f148-107">See the [CRYPTOAPI_BLOB](http://msdn.microsoft.com/library/windows/desktop/aa380238.aspx) structure.</span></span>  
  
 `pExponentBlob`  
 <span data-ttu-id="5f148-108">[in] L’objet blob Exponent codé en base64 (à partir de la \<exposant > élément).</span><span class="sxs-lookup"><span data-stu-id="5f148-108">[in] The base64-encoded Exponent blob (from the \<Exponent> element).</span></span> <span data-ttu-id="5f148-109">Consultez le [CRYPTOAPI_BLOB](http://msdn.microsoft.com/library/windows/desktop/aa380238.aspx) structure.</span><span class="sxs-lookup"><span data-stu-id="5f148-109">See the [CRYPTOAPI_BLOB](http://msdn.microsoft.com/library/windows/desktop/aa380238.aspx) structure.</span></span>  
  
 `ppwszPublicKeyToken`  
 <span data-ttu-id="5f148-110">[en sortie] Un pointeur vers WCHAR \* pour recevoir le jeton de clé publique codé en hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="5f148-110">[out] A pointer to WCHAR \* to receive the hex-encoded public key token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5f148-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5f148-111">Return Value</span></span>  
 <span data-ttu-id="5f148-112">`S_OK` si la fonction réussit.</span><span class="sxs-lookup"><span data-stu-id="5f148-112">`S_OK` if the function succeeds.</span></span> <span data-ttu-id="5f148-113">Sinon, retourne un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="5f148-113">Otherwise, returns an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f148-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f148-114">See Also</span></span>  
 [<span data-ttu-id="5f148-115">Authenticode</span><span class="sxs-lookup"><span data-stu-id="5f148-115">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
