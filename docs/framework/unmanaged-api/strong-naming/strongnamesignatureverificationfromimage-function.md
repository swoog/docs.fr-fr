---
title: StrongNameSignatureVerificationFromImage, fonction
ms.date: 03/30/2017
api_name:
- StrongNameSignatureVerificationFromImage
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameSignatureVerificationFromImage
helpviewer_keywords:
- StrongnameSignatureVerificationFromImage function [.NET Framework strong naming]
ms.assetid: 9fb144d2-07e0-4a0e-8e05-907bbb6c9e03
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 54b1d35d1c40289bad465978750ba738acf28c90
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59212438"
---
# <a name="strongnamesignatureverificationfromimage-function"></a><span data-ttu-id="427b6-102">StrongNameSignatureVerificationFromImage, fonction</span><span class="sxs-lookup"><span data-stu-id="427b6-102">StrongNameSignatureVerificationFromImage Function</span></span>
<span data-ttu-id="427b6-103">Vérifie qu’un assembly qui a déjà été mappé en mémoire est valide pour la clé publique associée.</span><span class="sxs-lookup"><span data-stu-id="427b6-103">Verifies that an assembly that has already been mapped to memory is valid for the associated public key.</span></span>  
  
 <span data-ttu-id="427b6-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="427b6-104">This function has been deprecated.</span></span> <span data-ttu-id="427b6-105">Utilisez le [ICLRStrongName::StrongNameVerificationFromImage](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverificationfromimage-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="427b6-105">Use the [ICLRStrongName::StrongNameVerificationFromImage](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverificationfromimage-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="427b6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="427b6-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameSignatureVerificationFromImage (  
    [in]  BYTE    *pbBase,  
    [in]  DWORD   dwLength,  
    [in]  DWORD   dwInFlags,  
    [out] DWORD   *pdwOutFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="427b6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="427b6-107">Parameters</span></span>  
 `pbBase`  
 <span data-ttu-id="427b6-108">[in] L’adresse virtuelle relative du manifeste d’assembly mappé.</span><span class="sxs-lookup"><span data-stu-id="427b6-108">[in] The relative virtual address of the mapped assembly manifest.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="427b6-109">[in] La taille, en octets, de l’image mappée.</span><span class="sxs-lookup"><span data-stu-id="427b6-109">[in] The size, in bytes, of the mapped image.</span></span>  
  
 `dwInFlags`  
 <span data-ttu-id="427b6-110">[in] Indicateurs qui influencent le comportement de vérification.</span><span class="sxs-lookup"><span data-stu-id="427b6-110">[in] Flags that influence verification behavior.</span></span> <span data-ttu-id="427b6-111">Les valeurs suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="427b6-111">The following values are supported:</span></span>  
  
-   <span data-ttu-id="427b6-112">`SN_INFLAG_FORCE_VER` (0 x 00000001) - force la vérification même s’il est nécessaire de remplacer les paramètres de Registre.</span><span class="sxs-lookup"><span data-stu-id="427b6-112">`SN_INFLAG_FORCE_VER` (0x00000001) - Forces verification even if it is necessary to override registry settings.</span></span>  
  
-   <span data-ttu-id="427b6-113">`SN_INFLAG_INSTALL` (0 x 00000002) - Spécifie qu’il s’agit de la première vérification effectuée sur cette image.</span><span class="sxs-lookup"><span data-stu-id="427b6-113">`SN_INFLAG_INSTALL` (0x00000002) - Specifies that this is the first verification performed on this image.</span></span>  
  
-   <span data-ttu-id="427b6-114">`SN_INFLAG_ADMIN_ACCESS` (0 x 00000004) - Spécifie que le cache autorise l’accès uniquement aux utilisateurs qui disposent des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="427b6-114">`SN_INFLAG_ADMIN_ACCESS` (0x00000004) - Specifies that the cache will allow access only to users who have administrative privileges.</span></span>  
  
-   <span data-ttu-id="427b6-115">`SN_INFLAG_USER_ACCESS` (0 x 00000008) - Spécifie que l’assembly sera accessible uniquement à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="427b6-115">`SN_INFLAG_USER_ACCESS` (0x00000008) - Specifies that the assembly will be accessible only to the current user.</span></span>  
  
-   <span data-ttu-id="427b6-116">`SN_INFLAG_ALL_ACCESS` (0 x 00000010) - Spécifie que le cache ne fournirez aucune garantie de restriction d’accès.</span><span class="sxs-lookup"><span data-stu-id="427b6-116">`SN_INFLAG_ALL_ACCESS` (0x00000010) - Specifies that the cache will provide no guarantees of access restriction.</span></span>  
  
-   <span data-ttu-id="427b6-117">`SN_INFLAG_RUNTIME` (0 x 80000000) - réservé au débogage interne.</span><span class="sxs-lookup"><span data-stu-id="427b6-117">`SN_INFLAG_RUNTIME` (0x80000000) - Reserved for internal debugging.</span></span>  
  
 `pdwOutFlags`  
 <span data-ttu-id="427b6-118">[out] Un indicateur pour les données de sortie supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="427b6-118">[out] A flag for additional output information.</span></span> <span data-ttu-id="427b6-119">La valeur suivante est prise en charge :</span><span class="sxs-lookup"><span data-stu-id="427b6-119">The following value is supported:</span></span>  
  
-   <span data-ttu-id="427b6-120">`SN_OUTFLAG_WAS_VERIFIED` (0 x 00000001) - cette valeur est définie sur `false` pour spécifier que la vérification a réussi en raison des paramètres de Registre.</span><span class="sxs-lookup"><span data-stu-id="427b6-120">`SN_OUTFLAG_WAS_VERIFIED` (0x00000001) - This value is set to `false` to specify that the verification succeeded due to registry settings.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="427b6-121">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="427b6-121">Return Value</span></span>  
 <span data-ttu-id="427b6-122">`true` de réussite ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="427b6-122">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="427b6-123">Notes</span><span class="sxs-lookup"><span data-stu-id="427b6-123">Remarks</span></span>  
 <span data-ttu-id="427b6-124">Si le `StrongNameSignatureVerificationFromImage` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.</span><span class="sxs-lookup"><span data-stu-id="427b6-124">If the `StrongNameSignatureVerificationFromImage` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="427b6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="427b6-125">Requirements</span></span>  
 <span data-ttu-id="427b6-126">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="427b6-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="427b6-127">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="427b6-127">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="427b6-128">**Bibliothèque :** Inclus en tant que ressource dans mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="427b6-128">**Library:** Included as a resource in mscoree.dll</span></span>  
  
 <span data-ttu-id="427b6-129">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="427b6-129">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="427b6-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="427b6-130">See also</span></span>

- [<span data-ttu-id="427b6-131">StrongNameSignatureVerificationFromImage, méthode</span><span class="sxs-lookup"><span data-stu-id="427b6-131">StrongNameSignatureVerificationFromImage Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverificationfromimage-method.md)
- [<span data-ttu-id="427b6-132">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="427b6-132">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
