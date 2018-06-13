---
title: Méthode ICLRStrongName::StrongNameKeyInstall
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameKeyInstall
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameKeyInstall
helpviewer_keywords:
- ICLRStrongName::StrongNameKeyInstall method [.NET Framework hosting]
- StrongNameKeyInstall method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 5c15cf3b-164c-49d1-8e57-e42949d55acf
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 572afc5eb9ec3cf52199e5ad74406c876485461c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33434088"
---
# <a name="iclrstrongnamestrongnamekeyinstall-method"></a><span data-ttu-id="265c5-102">Méthode ICLRStrongName::StrongNameKeyInstall</span><span class="sxs-lookup"><span data-stu-id="265c5-102">ICLRStrongName::StrongNameKeyInstall Method</span></span>
<span data-ttu-id="265c5-103">Importe une paire de clés publique/privée dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="265c5-103">Imports a public/private key pair into a container.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="265c5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="265c5-104">Syntax</span></span>  
  
```  
HRESULT StrongNameKeyInstall (  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="265c5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="265c5-105">Parameters</span></span>  
 `wszKeyContainer`  
 <span data-ttu-id="265c5-106">[in] Le nom du conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="265c5-106">[in] The name of the key container.</span></span> <span data-ttu-id="265c5-107">`wszKeyContainer` doit être une chaîne non vide.</span><span class="sxs-lookup"><span data-stu-id="265c5-107">`wszKeyContainer` must be a non-empty string.</span></span>  
  
 `pbKeyBlob`  
 <span data-ttu-id="265c5-108">[in] La paire de clés binaire.</span><span class="sxs-lookup"><span data-stu-id="265c5-108">[in] The binary key pair.</span></span>  
  
 `cbKeyBlob`  
 <span data-ttu-id="265c5-109">[in] La taille, en octets, de `pbKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="265c5-109">[in] The size, in bytes, of `pbKeyBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="265c5-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="265c5-110">Return Value</span></span>  
 <span data-ttu-id="265c5-111">`S_OK` Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (voir [valeurs HRESULT courantes](http://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).</span><span class="sxs-lookup"><span data-stu-id="265c5-111">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](http://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="265c5-112">Notes</span><span class="sxs-lookup"><span data-stu-id="265c5-112">Remarks</span></span>  
 <span data-ttu-id="265c5-113">Utilisez le [ICLRStrongName::StrongNameKeyDelete](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeydelete-method.md) méthode pour supprimer le conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="265c5-113">Use the [ICLRStrongName::StrongNameKeyDelete](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeydelete-method.md) method to delete the key container.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="265c5-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="265c5-114">Requirements</span></span>  
 <span data-ttu-id="265c5-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="265c5-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="265c5-116">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="265c5-116">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="265c5-117">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="265c5-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="265c5-118">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="265c5-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="265c5-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="265c5-119">See Also</span></span>  
 [<span data-ttu-id="265c5-120">StrongNameKeyDelete, méthode</span><span class="sxs-lookup"><span data-stu-id="265c5-120">StrongNameKeyDelete Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeydelete-method.md)  
 [<span data-ttu-id="265c5-121">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="265c5-121">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
