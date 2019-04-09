---
title: StrongNameSignatureVerification, fonction
ms.date: 03/30/2017
api_name:
- StrongNameSignatureVerification
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameSignatureVerification
helpviewer_keywords:
- StrongNameSignatureVerification function [.NET Framework strong naming]
ms.assetid: 933758dd-231e-4382-8819-242c0a13a4b7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c398663b84637d2551b0d94bd59b9e0994721ba5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59124759"
---
# <a name="strongnamesignatureverification-function"></a><span data-ttu-id="7681f-102">StrongNameSignatureVerification, fonction</span><span class="sxs-lookup"><span data-stu-id="7681f-102">StrongNameSignatureVerification Function</span></span>
<span data-ttu-id="7681f-103">Obtient une valeur indiquant si le manifeste d’assembly au chemin fourni contient une signature de nom fort, qui est vérifiée en fonction des indicateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7681f-103">Gets a value indicating whether the assembly manifest at the supplied path contains a strong name signature, which is verified according to the specified flags.</span></span>  
  
 <span data-ttu-id="7681f-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7681f-104">This function has been deprecated.</span></span> <span data-ttu-id="7681f-105">Utilisez le [ICLRStrongName::StrongNameSignatureVerification](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverification-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="7681f-105">Use the [ICLRStrongName::StrongNameSignatureVerification](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverification-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7681f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7681f-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameSignatureVerification (  
    [in]  LPCWSTR   wszFilePath,  
    [in]  DWORD     dwInFlags,  
    [out] DWORD     *pdwOutFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7681f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7681f-107">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="7681f-108">[in] Le chemin d’accès pour le fichier exécutable portable (.dll ou .exe) pour l’assembly à vérifier.</span><span class="sxs-lookup"><span data-stu-id="7681f-108">[in] The path to the portable executable (.dll or .exe) file for the assembly to verify.</span></span>  
  
 `dwInFlags`  
 <span data-ttu-id="7681f-109">[in] Indicateurs pour modifier le comportement de vérification.</span><span class="sxs-lookup"><span data-stu-id="7681f-109">[in] Flags to modify the verification behavior.</span></span> <span data-ttu-id="7681f-110">Les valeurs suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="7681f-110">The following values are supported:</span></span>  
  
-   `SN_INFLAG_FORCE_VER` <span data-ttu-id="7681f-111">(0 x 00000001) - force la vérification même s’il est nécessaire de remplacer les paramètres de Registre.</span><span class="sxs-lookup"><span data-stu-id="7681f-111">(0x00000001) - Forces verification even if it is necessary to override registry settings.</span></span>  
  
-   `SN_INFLAG_INSTALL` <span data-ttu-id="7681f-112">(0 x 00000002) - Spécifie qu’il s’agit de la première fois que le manifeste est vérifié.</span><span class="sxs-lookup"><span data-stu-id="7681f-112">(0x00000002) - Specifies that this is the first time the manifest is verified.</span></span>  
  
-   `SN_INFLAG_ADMIN_ACCESS` <span data-ttu-id="7681f-113">(0 x 00000004) - Spécifie que le cache autorise l’accès uniquement aux utilisateurs qui disposent des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="7681f-113">(0x00000004) - Specifies that the cache will allow access only to users who have administrative privileges.</span></span>  
  
-   `SN_INFLAG_USER_ACCESS` <span data-ttu-id="7681f-114">(0 x 00000008) - Spécifie que l’assembly sera accessible uniquement à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="7681f-114">(0x00000008) - Specifies that the assembly will be accessible only to the current user.</span></span>  
  
-   `SN_INFLAG_ALL_ACCESS` <span data-ttu-id="7681f-115">(0 x 00000010) - Spécifie que le cache ne fournirez aucune garantie de restriction d’accès.</span><span class="sxs-lookup"><span data-stu-id="7681f-115">(0x00000010) - Specifies that the cache will provide no guarantees of access restriction.</span></span>  
  
-   `SN_INFLAG_RUNTIME` <span data-ttu-id="7681f-116">(0 x 80000000) - réservé au débogage interne.</span><span class="sxs-lookup"><span data-stu-id="7681f-116">(0x80000000) - Reserved for internal debugging.</span></span>  
  
 `pdwOutFlags`  
 <span data-ttu-id="7681f-117">[out] Indicateurs spécifiant si la signature de nom fort a été vérifiée.</span><span class="sxs-lookup"><span data-stu-id="7681f-117">[out] Flags indicating whether the strong name signature was verified.</span></span> <span data-ttu-id="7681f-118">La valeur suivante est prise en charge :</span><span class="sxs-lookup"><span data-stu-id="7681f-118">The following value is supported:</span></span>  
  
-   `SN_OUTFLAG_WAS_VERIFIED` <span data-ttu-id="7681f-119">(0 x 00000001) - cette valeur est définie sur `false` pour spécifier que la vérification a réussi en raison des paramètres de Registre.</span><span class="sxs-lookup"><span data-stu-id="7681f-119">(0x00000001) - This value is set to `false` to specify that the verification succeeded due to registry settings.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7681f-120">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7681f-120">Return Value</span></span>  
 `true` <span data-ttu-id="7681f-121">Si la vérification a réussi ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="7681f-121">if the verification was successful; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7681f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7681f-122">Requirements</span></span>  
 <span data-ttu-id="7681f-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7681f-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7681f-124">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="7681f-124">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="7681f-125">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7681f-125">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="7681f-126">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="7681f-126">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="7681f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7681f-127">See also</span></span>

- [<span data-ttu-id="7681f-128">StrongNameSignatureVerification, méthode</span><span class="sxs-lookup"><span data-stu-id="7681f-128">StrongNameSignatureVerification Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverification-method.md)
- [<span data-ttu-id="7681f-129">StrongNameSignatureVerificationEx, méthode</span><span class="sxs-lookup"><span data-stu-id="7681f-129">StrongNameSignatureVerificationEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverificationex-method.md)
- [<span data-ttu-id="7681f-130">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="7681f-130">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
