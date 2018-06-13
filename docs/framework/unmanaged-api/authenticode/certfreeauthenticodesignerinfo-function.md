---
title: CertFreeAuthenticodeSignerInfo, fonction
ms.date: 03/30/2017
api_name:
- CertFreeAuthenticodeSignerInfo
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: 8029633c-b6e4-4665-a7c2-89607c3247ef
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 84f15dc49d14e781f69d0f9da8f314eb71d8c034
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33401614"
---
# <a name="certfreeauthenticodesignerinfo-function"></a><span data-ttu-id="4fc84-102">CertFreeAuthenticodeSignerInfo, fonction</span><span class="sxs-lookup"><span data-stu-id="4fc84-102">CertFreeAuthenticodeSignerInfo Function</span></span>
<span data-ttu-id="4fc84-103">Libère les ressources allouées pour le [AXL_AUTHENTICODE_SIGNER_INFO](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md) structure.</span><span class="sxs-lookup"><span data-stu-id="4fc84-103">Frees resources allocated for the [AXL_AUTHENTICODE_SIGNER_INFO](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md) structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4fc84-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fc84-104">Syntax</span></span>  
  
```  
HRESULT CertFreeAuthenticodeSignerInfo (  
    [in, out]  PAXL_AUTHENTICODE_SIGNER_INFO   pSignerInfo);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4fc84-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4fc84-105">Parameters</span></span>  
 `pSignerInfo`  
 <span data-ttu-id="4fc84-106">[en entrée, en sortie] Les informations du signataire à libérer.</span><span class="sxs-lookup"><span data-stu-id="4fc84-106">[in, out] Signer information to be released.</span></span> <span data-ttu-id="4fc84-107">Consultez le [AXL_AUTHENTICODE_SIGNER_INFO](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md) structure.</span><span class="sxs-lookup"><span data-stu-id="4fc84-107">See the [AXL_AUTHENTICODE_SIGNER_INFO](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md) structure.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4fc84-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4fc84-108">Return Value</span></span>  
 <span data-ttu-id="4fc84-109">`S_OK` si la fonction réussit.</span><span class="sxs-lookup"><span data-stu-id="4fc84-109">`S_OK` if the function succeeds.</span></span> <span data-ttu-id="4fc84-110">Sinon, retourne un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="4fc84-110">Otherwise, returns an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4fc84-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fc84-111">See Also</span></span>  
 [<span data-ttu-id="4fc84-112">Authenticode</span><span class="sxs-lookup"><span data-stu-id="4fc84-112">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
