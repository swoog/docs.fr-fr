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
ms.openlocfilehash: d60e1e503cd48b9b9e2ed91a6bfea000aeeea2af
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43527874"
---
# <a name="iclrstrongnamestrongnamekeyinstall-method"></a><span data-ttu-id="4f5bc-102">Méthode ICLRStrongName::StrongNameKeyInstall</span><span class="sxs-lookup"><span data-stu-id="4f5bc-102">ICLRStrongName::StrongNameKeyInstall Method</span></span>
<span data-ttu-id="4f5bc-103">Importe une paire de clés publique/privée dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="4f5bc-103">Imports a public/private key pair into a container.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f5bc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f5bc-104">Syntax</span></span>  
  
```  
HRESULT StrongNameKeyInstall (  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4f5bc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f5bc-105">Parameters</span></span>  
 `wszKeyContainer`  
 <span data-ttu-id="4f5bc-106">[in] Le nom du conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="4f5bc-106">[in] The name of the key container.</span></span> <span data-ttu-id="4f5bc-107">`wszKeyContainer` doit être une chaîne non vide.</span><span class="sxs-lookup"><span data-stu-id="4f5bc-107">`wszKeyContainer` must be a non-empty string.</span></span>  
  
 `pbKeyBlob`  
 <span data-ttu-id="4f5bc-108">[in] La paire de clés binaire.</span><span class="sxs-lookup"><span data-stu-id="4f5bc-108">[in] The binary key pair.</span></span>  
  
 `cbKeyBlob`  
 <span data-ttu-id="4f5bc-109">[in] La taille, en octets, de `pbKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="4f5bc-109">[in] The size, in bytes, of `pbKeyBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4f5bc-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4f5bc-110">Return Value</span></span>  
 <span data-ttu-id="4f5bc-111">`S_OK` Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (consultez [valeurs HRESULT courantes](https://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).</span><span class="sxs-lookup"><span data-stu-id="4f5bc-111">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4f5bc-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4f5bc-112">Remarks</span></span>  
 <span data-ttu-id="4f5bc-113">Utilisez le [ICLRStrongName::StrongNameKeyDelete](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeydelete-method.md) méthode pour supprimer le conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="4f5bc-113">Use the [ICLRStrongName::StrongNameKeyDelete](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeydelete-method.md) method to delete the key container.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4f5bc-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f5bc-114">Requirements</span></span>  
 <span data-ttu-id="4f5bc-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4f5bc-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4f5bc-116">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="4f5bc-116">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="4f5bc-117">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4f5bc-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4f5bc-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4f5bc-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4f5bc-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f5bc-119">See Also</span></span>  
 [<span data-ttu-id="4f5bc-120">StrongNameKeyDelete, méthode</span><span class="sxs-lookup"><span data-stu-id="4f5bc-120">StrongNameKeyDelete Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeydelete-method.md)  
 [<span data-ttu-id="4f5bc-121">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="4f5bc-121">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
