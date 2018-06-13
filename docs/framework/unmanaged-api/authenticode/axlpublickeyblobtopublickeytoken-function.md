---
title: _AxlPublicKeyBlobToPublicKeyToken, fonction
ms.date: 03/30/2017
api_name:
- _AxlPublicKeyBlobToPublicKeyToken
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: 2d92a746-d68c-4f53-a16e-727f071a2d80
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 56333165d179abd79e82f1416342a2700029eb12
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33401672"
---
# <a name="axlpublickeyblobtopublickeytoken-function"></a><span data-ttu-id="58499-102">_AxlPublicKeyBlobToPublicKeyToken, fonction</span><span class="sxs-lookup"><span data-stu-id="58499-102">_AxlPublicKeyBlobToPublicKeyToken Function</span></span>
<span data-ttu-id="58499-103">Calcule le jeton de clé publique de nom fort à partir d'un format CSP PUBLICKEYBLOB.</span><span class="sxs-lookup"><span data-stu-id="58499-103">Computes the strong name public key token from a CSP PUBLICKEYBLOB format.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58499-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58499-104">Syntax</span></span>  
  
```  
HRESULT _AxlPublicKeyBlobToPublicKeyToken (  
    [in]  PCCERT_CHAIN_CONTEXT   pCspPublicKeyBlob,  
    [out] LPWSTR                 *ppwszPublicKeyToken  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="58499-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58499-105">Parameters</span></span>  
 `pCspPublicKeyBlob`  
 <span data-ttu-id="58499-106">[en entrée] L'objet blob de clé publique CSP.</span><span class="sxs-lookup"><span data-stu-id="58499-106">[in] The CSP public key blob.</span></span>  
  
 `ppwszPublicKeyHash`  
 <span data-ttu-id="58499-107">[en sortie] Un pointeur vers WCHAR \* pour recevoir le hachage de clé publique codé au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="58499-107">[out] A pointer to WCHAR \* to receive the hex-encoded public key hash.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="58499-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="58499-108">Return Value</span></span>  
 <span data-ttu-id="58499-109">`S_OK` si la fonction réussit, sinon `S_FALSE`.</span><span class="sxs-lookup"><span data-stu-id="58499-109">`S_OK` if the function succeeds; otherwise `S_FALSE`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58499-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58499-110">See Also</span></span>  
 [<span data-ttu-id="58499-111">Authenticode</span><span class="sxs-lookup"><span data-stu-id="58499-111">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
