---
title: Méthode ICLRStrongName::StrongNameKeyGen
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameKeyGen
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameKeyGen
helpviewer_keywords:
- StrongNameKeyGen method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameKeyGen method [.NET Framework hosting]
ms.assetid: ac5c1245-9acf-4271-9c08-3d9b7c670df3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 55b4fbb8785f788c9eb34f32b5078201f8253066
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33433326"
---
# <a name="iclrstrongnamestrongnamekeygen-method"></a><span data-ttu-id="314a9-102">Méthode ICLRStrongName::StrongNameKeyGen</span><span class="sxs-lookup"><span data-stu-id="314a9-102">ICLRStrongName::StrongNameKeyGen Method</span></span>
<span data-ttu-id="314a9-103">Crée une nouvelle paire de clés publique/privée pour l’utiliser avec un nom fort.</span><span class="sxs-lookup"><span data-stu-id="314a9-103">Creates a new public/private key pair for strong name use.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="314a9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="314a9-104">Syntax</span></span>  
  
```  
HRESULT StrongNameKeyGen (  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  DWORD     dwFlags,  
    [out] BYTE      **ppbKeyBlob,  
    [out] ULONG     *pcbKeyBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="314a9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="314a9-105">Parameters</span></span>  
 `wszKeyContainer`  
 <span data-ttu-id="314a9-106">[in] Le nom du conteneur de clé demandé.</span><span class="sxs-lookup"><span data-stu-id="314a9-106">[in] The requested key container name.</span></span> <span data-ttu-id="314a9-107">`wszKeyContainer` doit être une chaîne non vide ou la valeur null pour générer un nom temporaire.</span><span class="sxs-lookup"><span data-stu-id="314a9-107">`wszKeyContainer` must either be a non-empty string or null to generate a temporary name.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="314a9-108">[in] Une valeur qui spécifie s’il faut laisser la clé enregistrée.</span><span class="sxs-lookup"><span data-stu-id="314a9-108">[in] A value that specifies whether to leave the key registered.</span></span> <span data-ttu-id="314a9-109">Les valeurs suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="314a9-109">The following values are supported:</span></span>  
  
-   <span data-ttu-id="314a9-110">0 x 00000000 - utilisée lorsque `wszKeyContainer` a la valeur null pour générer un nom de conteneur de clé temporaire.</span><span class="sxs-lookup"><span data-stu-id="314a9-110">0x00000000 - Used when `wszKeyContainer` is null to generate a temporary key container name.</span></span>  
  
-   <span data-ttu-id="314a9-111">0 x 00000001 (`SN_LEAVE_KEY`)-Spécifie que la clé doit rester enregistrée.</span><span class="sxs-lookup"><span data-stu-id="314a9-111">0x00000001 (`SN_LEAVE_KEY`) - Specifies that the key should be left registered.</span></span>  
  
 `ppbKeyBlob`  
 <span data-ttu-id="314a9-112">[out] La paire de clés publique/privée retournée.</span><span class="sxs-lookup"><span data-stu-id="314a9-112">[out] The returned public/private key pair.</span></span>  
  
 `pcbKeyBlob`  
 <span data-ttu-id="314a9-113">[out] La taille, en octets, de `ppbKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="314a9-113">[out] The size, in bytes, of `ppbKeyBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="314a9-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="314a9-114">Return Value</span></span>  
 <span data-ttu-id="314a9-115">`S_OK` Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (voir [valeurs HRESULT courantes](http://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).</span><span class="sxs-lookup"><span data-stu-id="314a9-115">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](http://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="314a9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="314a9-116">Remarks</span></span>  
 <span data-ttu-id="314a9-117">Le [ICLRStrongName::StrongNameKeyGen](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeygen-method.md) méthode crée une clé 1024 bits.</span><span class="sxs-lookup"><span data-stu-id="314a9-117">The [ICLRStrongName::StrongNameKeyGen](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeygen-method.md) method creates a 1024-bit key.</span></span> <span data-ttu-id="314a9-118">Une fois la clé est récupérée, vous devez appeler la [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) méthode pour libérer la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="314a9-118">After the key is retrieved, you should call the [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) method to release the allocated memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="314a9-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="314a9-119">Requirements</span></span>  
 <span data-ttu-id="314a9-120">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="314a9-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="314a9-121">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="314a9-121">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="314a9-122">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="314a9-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="314a9-123">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="314a9-123">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="314a9-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="314a9-124">See Also</span></span>  
 [<span data-ttu-id="314a9-125">StrongNameKeyGenEx, méthode</span><span class="sxs-lookup"><span data-stu-id="314a9-125">StrongNameKeyGenEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeygenex-method.md)  
 [<span data-ttu-id="314a9-126">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="314a9-126">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
