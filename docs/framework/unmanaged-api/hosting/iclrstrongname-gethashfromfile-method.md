---
title: Méthode ICLRStrongName::GetHashFromFile
ms.date: 03/30/2017
api_name:
- ICLRStrongName.GetHashFromFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::GetHashFromFile
helpviewer_keywords:
- ICLRStrongName::GetHashFromFile method [.NET Framework hosting]
- GetHashFromFile method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 9e50480a-8ada-4044-b2a5-97bb14ed3525
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 94d17b6c8150744d4beca5e74827d235f81af08c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33433313"
---
# <a name="iclrstrongnamegethashfromfile-method"></a><span data-ttu-id="3af50-102">Méthode ICLRStrongName::GetHashFromFile</span><span class="sxs-lookup"><span data-stu-id="3af50-102">ICLRStrongName::GetHashFromFile Method</span></span>
<span data-ttu-id="3af50-103">Génère un hachage sur le contenu du fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="3af50-103">Generates a hash over the contents of the specified file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3af50-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3af50-104">Syntax</span></span>  
  
```  
HRESULT GetHashFromFile (  
    [in]  LPCSTR   szFilePath,  
    [in, out] unsigned int   *piHashAlg,   
    [out] BYTE     *pbHash,      
    [in]  DWORD    cchHash,      
    [out] DWORD    *pchHash  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3af50-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3af50-105">Parameters</span></span>  
 `szFilePath`  
 <span data-ttu-id="3af50-106">[in] Le nom du fichier à hacher.</span><span class="sxs-lookup"><span data-stu-id="3af50-106">[in] The name of the file to hash.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="3af50-107">[dans, out] L’algorithme à utiliser lors de la génération du hachage.</span><span class="sxs-lookup"><span data-stu-id="3af50-107">[in, out] The algorithm to use when generating the hash.</span></span> <span data-ttu-id="3af50-108">Les algorithmes valides sont ceux définis par le CryptoAPI Win32.</span><span class="sxs-lookup"><span data-stu-id="3af50-108">Valid algorithms are those defined by the Win32 CryptoAPI.</span></span> <span data-ttu-id="3af50-109">Si `piHashAlg` est définie sur 0, l’algorithme par défaut CALG_SHA-1 est utilisé.</span><span class="sxs-lookup"><span data-stu-id="3af50-109">If `piHashAlg` is set to 0, the default algorithm CALG_SHA-1 is used.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="3af50-110">[out] Tableau d’octets contenant le hachage généré.</span><span class="sxs-lookup"><span data-stu-id="3af50-110">[out] A byte array containing the generated hash.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="3af50-111">[in] La taille maximale de la mémoire tampon qui `pbHash` pointe vers.</span><span class="sxs-lookup"><span data-stu-id="3af50-111">[in] The maximum size of the buffer that `pbHash` points to.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="3af50-112">[out] La taille, en octets, de retourné `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="3af50-112">[out] The size, in bytes, of the returned `pbHash`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3af50-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3af50-113">Return Value</span></span>  
 <span data-ttu-id="3af50-114">`S_OK` Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (voir [valeurs HRESULT courantes](http://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).</span><span class="sxs-lookup"><span data-stu-id="3af50-114">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](http://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3af50-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3af50-115">Remarks</span></span>  
 <span data-ttu-id="3af50-116">Cette méthode est identique à la [ICLRStrongName::GetHashFromFileW](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfilew-method.md) , à ceci près que le nom de fichier spécification est ANSI au lieu d’Unicode.</span><span class="sxs-lookup"><span data-stu-id="3af50-116">This method is the same as the [ICLRStrongName::GetHashFromFileW](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfilew-method.md) method, except that the file name specification is ANSI instead of Unicode.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3af50-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3af50-117">Requirements</span></span>  
 <span data-ttu-id="3af50-118">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3af50-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3af50-119">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="3af50-119">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="3af50-120">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3af50-120">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3af50-121">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3af50-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3af50-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3af50-122">See Also</span></span>  
 [<span data-ttu-id="3af50-123">GetHashFromFileW, méthode</span><span class="sxs-lookup"><span data-stu-id="3af50-123">GetHashFromFileW Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfilew-method.md)  
 [<span data-ttu-id="3af50-124">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="3af50-124">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
