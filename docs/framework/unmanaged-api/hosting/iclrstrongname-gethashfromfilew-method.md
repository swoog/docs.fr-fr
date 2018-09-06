---
title: Méthode ICLRStrongName::GetHashFromFileW
ms.date: 03/30/2017
api_name:
- ICLRStrongName.GetHashFromFileW
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::GetHashFromFileW
helpviewer_keywords:
- GetHashFromFileW method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::GetHashFromFileW method [.NET Framework hosting]
ms.assetid: c6ff45fc-905d-4c6e-b00c-97c6c7c55d99
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: acfa5c138faa47c96600530ab923de102b173ed6
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43803455"
---
# <a name="iclrstrongnamegethashfromfilew-method"></a><span data-ttu-id="de9c2-102">Méthode ICLRStrongName::GetHashFromFileW</span><span class="sxs-lookup"><span data-stu-id="de9c2-102">ICLRStrongName::GetHashFromFileW Method</span></span>
<span data-ttu-id="de9c2-103">Génère un hachage sur le contenu du fichier spécifié par une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="de9c2-103">Generates a hash over the contents of the file specified by a Unicode string.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="de9c2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de9c2-104">Syntax</span></span>  
  
```  
HRESULT GetHashFromFileW (   
    [in]  LPCWSTR   wszFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE      *pbHash,  
    [in]  DWORD     cchHash,  
    [out] DWORD     *pchHash  
);   
```  
  
#### <a name="parameters"></a><span data-ttu-id="de9c2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de9c2-105">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="de9c2-106">[in] Le nom Unicode du fichier à hacher.</span><span class="sxs-lookup"><span data-stu-id="de9c2-106">[in] The Unicode name of the file to hash.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="de9c2-107">[in, out] L’algorithme à utiliser lors de la génération du hachage.</span><span class="sxs-lookup"><span data-stu-id="de9c2-107">[in, out] The algorithm to use when generating the hash.</span></span> <span data-ttu-id="de9c2-108">Les algorithmes valides sont ceux définis par l’interface CryptoAPI Win32.</span><span class="sxs-lookup"><span data-stu-id="de9c2-108">Valid algorithms are those defined by the Win32 CryptoAPI.</span></span> <span data-ttu-id="de9c2-109">Si `piHashAlg` est définie sur 0, l’algorithme par défaut CALG_SHA-1 est utilisé.</span><span class="sxs-lookup"><span data-stu-id="de9c2-109">If `piHashAlg` is set to 0, the default algorithm CALG_SHA-1 is used.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="de9c2-110">[out] Tableau d’octets contenant le hachage généré.</span><span class="sxs-lookup"><span data-stu-id="de9c2-110">[out] A byte array containing the generated hash.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="de9c2-111">[in] La taille maximale de la mémoire tampon vers laquelle pointe `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="de9c2-111">[in] The maximum size of the buffer pointed to by `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="de9c2-112">[out] La taille, en octets, de `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="de9c2-112">[out] The size, in bytes, of `pbHash`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="de9c2-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="de9c2-113">Return Value</span></span>  
 <span data-ttu-id="de9c2-114">`S_OK` Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (consultez [valeurs HRESULT courantes](https://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).</span><span class="sxs-lookup"><span data-stu-id="de9c2-114">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="de9c2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="de9c2-115">Remarks</span></span>  
 <span data-ttu-id="de9c2-116">Cette méthode est identique à la [ICLRStrongName::GetHashFromFile](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfile-method.md) , à ceci près que le nom du fichier spécification est Unicode et non ANSI.</span><span class="sxs-lookup"><span data-stu-id="de9c2-116">This method is the same as the [ICLRStrongName::GetHashFromFile](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfile-method.md) method, except that the file name specification is Unicode instead of ANSI.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="de9c2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de9c2-117">Requirements</span></span>  
 <span data-ttu-id="de9c2-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="de9c2-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="de9c2-119">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="de9c2-119">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="de9c2-120">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="de9c2-120">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="de9c2-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="de9c2-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="de9c2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de9c2-122">See Also</span></span>  
 [<span data-ttu-id="de9c2-123">GetHashFromFile, méthode</span><span class="sxs-lookup"><span data-stu-id="de9c2-123">GetHashFromFile Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfile-method.md)  
 [<span data-ttu-id="de9c2-124">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="de9c2-124">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
