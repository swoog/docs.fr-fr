---
title: Méthode ICLRStrongName::StrongNameCompareAssemblies
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameCompareAssemblies
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameCompareAssemblies
helpviewer_keywords:
- ICLRStrongName::StrongNameCompareAssemblies method [.NET Framework hosting]
- StrongNameCompareAssemblies method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: b1fb356c-72cf-4aa4-8376-f291a6d97c01
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3eb23da5accd89931ee4b883bfa162035ec26ddd
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43384620"
---
# <a name="iclrstrongnamestrongnamecompareassemblies-method"></a><span data-ttu-id="c0490-102">Méthode ICLRStrongName::StrongNameCompareAssemblies</span><span class="sxs-lookup"><span data-stu-id="c0490-102">ICLRStrongName::StrongNameCompareAssemblies Method</span></span>
<span data-ttu-id="c0490-103">Détermine si deux assemblys diffèrent uniquement par leurs signatures de nom fort.</span><span class="sxs-lookup"><span data-stu-id="c0490-103">Determines whether two assemblies differ only by their strong name signatures.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0490-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0490-104">Syntax</span></span>  
  
```  
HRESULT StrongNameCompareAssemblies (  
    [in]  LPCWSTR   wszAssembly1,  
    [in]  LPCWSTR   wszAssembly2,  
    [out] DWORD     *pdwResult  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c0490-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0490-105">Parameters</span></span>  
 `wszAssembly1`  
 <span data-ttu-id="c0490-106">[in] Le chemin d’accès à l’assembly en premier.</span><span class="sxs-lookup"><span data-stu-id="c0490-106">[in] The path to the first assembly.</span></span>  
  
 `wszAssembly2`  
 <span data-ttu-id="c0490-107">[in] Le chemin d’accès au deuxième assembly.</span><span class="sxs-lookup"><span data-stu-id="c0490-107">[in] The path to the second assembly.</span></span>  
  
 `pdwResult`  
 <span data-ttu-id="c0490-108">[out] Une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c0490-108">[out] One of the following values:</span></span>  
  
-   <span data-ttu-id="c0490-109">`SN_CMP_DIFFERENT` (0) : Spécifie que les assemblys contiennent des données différentes.</span><span class="sxs-lookup"><span data-stu-id="c0490-109">`SN_CMP_DIFFERENT` (0) - Specifies that the assemblies contain different data.</span></span>  
  
-   <span data-ttu-id="c0490-110">`SN_CMP_IDENTICAL` (1) - Spécifie que les assemblys sont exactement identiques, y compris leurs signatures et la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c0490-110">`SN_CMP_IDENTICAL` (1) - Specifies that the assemblies are exactly the same, including their signatures and checksum.</span></span>  
  
-   <span data-ttu-id="c0490-111">`SN_CMP_SIGONLY` (2) : Spécifie que les assemblys diffèrent uniquement par la signature et la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c0490-111">`SN_CMP_SIGONLY` (2) - Specifies that the assemblies differ only by signature and checksum.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c0490-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c0490-112">Return Value</span></span>  
 <span data-ttu-id="c0490-113">`S_OK` Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (consultez [valeurs HRESULT courantes](https://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).</span><span class="sxs-lookup"><span data-stu-id="c0490-113">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c0490-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0490-114">Requirements</span></span>  
 <span data-ttu-id="c0490-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c0490-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0490-116">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="c0490-116">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="c0490-117">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c0490-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c0490-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c0490-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c0490-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c0490-119">Remarks</span></span>  
 <span data-ttu-id="c0490-120">La signature de nom fort d’un assembly se compose du nom de texte, version, culture et jeton de clé publique de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="c0490-120">The strong name signature of an assembly consists of the assembly's text name, version, culture, and public key token.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0490-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0490-121">See Also</span></span>  
 [<span data-ttu-id="c0490-122">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="c0490-122">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
