---
title: Méthode ICLRStrongName::GetHashFromAssemblyFileW
ms.date: 03/30/2017
api_name:
- ICLRStrongName.GetHashFromAssemblyFileW
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::GetHashFromAssemblyFileW
helpviewer_keywords:
- ICLRStrongName::GetHashFromAssemblyFileW method [.NET Framework hosting]
- GetHashFromAssemblyFileW method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 5d0b44a2-5a14-44a2-9a0e-e8682fd4e106
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a7686a84759f8ac40a123d2c9a7b8f1b9b8096cb
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43749916"
---
# <a name="iclrstrongnamegethashfromassemblyfilew-method"></a><span data-ttu-id="85957-102">Méthode ICLRStrongName::GetHashFromAssemblyFileW</span><span class="sxs-lookup"><span data-stu-id="85957-102">ICLRStrongName::GetHashFromAssemblyFileW Method</span></span>
<span data-ttu-id="85957-103">Génère un hachage sur le contenu du fichier spécifié par une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="85957-103">Generates a hash over the contents of the file specified by a Unicode string.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="85957-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85957-104">Syntax</span></span>  
  
```  
HRESULT GetHashFromAssemblyFileW (  
    [in]  LPCWSTR   wszFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE      *pbHash,  
    [in]  DWORD     cchHash,  
    [out] DWORD     *pchHash  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="85957-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85957-105">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="85957-106">[in] Le chemin d’accès au fichier à hacher.</span><span class="sxs-lookup"><span data-stu-id="85957-106">[in] The path to the file to be hashed.</span></span> <span data-ttu-id="85957-107">Ce paramètre doit être une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="85957-107">This parameter must be a Unicode string.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="85957-108">[in, out] Constante qui spécifie l’algorithme de hachage.</span><span class="sxs-lookup"><span data-stu-id="85957-108">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="85957-109">Utilisez zéro pour l’algorithme de hachage par défaut.</span><span class="sxs-lookup"><span data-stu-id="85957-109">Use zero for the default hash algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="85957-110">[out] La mémoire tampon de hachage retournée.</span><span class="sxs-lookup"><span data-stu-id="85957-110">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="85957-111">[in] La taille maximale demandée de `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="85957-111">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="85957-112">[out] L’a retourné la taille, en octets, de `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="85957-112">[out] The returned size, in bytes, of `pbHash`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="85957-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="85957-113">Return Value</span></span>  
 <span data-ttu-id="85957-114">`S_OK` Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (consultez [valeurs HRESULT courantes](https://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).</span><span class="sxs-lookup"><span data-stu-id="85957-114">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="85957-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85957-115">Requirements</span></span>  
 <span data-ttu-id="85957-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="85957-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="85957-117">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="85957-117">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="85957-118">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="85957-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="85957-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="85957-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="85957-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85957-120">See Also</span></span>  
 [<span data-ttu-id="85957-121">GetHashFromAssemblyFile, méthode</span><span class="sxs-lookup"><span data-stu-id="85957-121">GetHashFromAssemblyFile Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfile-method.md)  
 [<span data-ttu-id="85957-122">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="85957-122">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
