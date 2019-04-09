---
title: GetHashFromFile, fonction
ms.date: 03/30/2017
api_name:
- GetHashFromFile
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromFile
helpviewer_keywords:
- GetHashFromFile function [.NET Framework strong naming]
ms.assetid: b3c526a4-8fb4-4ad6-b6af-42ce9c06492e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5774b7cdcfedfc407b626ab5052f5b4a77461e9b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59155907"
---
# <a name="gethashfromfile-function"></a><span data-ttu-id="d403c-102">GetHashFromFile, fonction</span><span class="sxs-lookup"><span data-stu-id="d403c-102">GetHashFromFile Function</span></span>
<span data-ttu-id="d403c-103">Génère un hachage sur le contenu du fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="d403c-103">Generates a hash over the contents of the specified file.</span></span>  
  
 <span data-ttu-id="d403c-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d403c-104">This function has been deprecated.</span></span> <span data-ttu-id="d403c-105">Utilisez le [ICLRStrongName::GetHashFromFile](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfile-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="d403c-105">Use the [ICLRStrongName::GetHashFromFile](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfile-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d403c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d403c-106">Syntax</span></span>  
  
```  
HRESULT GetHashFromFile (  
    [in]  LPCSTR   szFilePath,  
    [in, out] unsigned int   *piHashAlg,   
    [out] BYTE     *pbHash,      
    [in]  DWORD    cchHash,      
    [out] DWORD    *pchHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d403c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d403c-107">Parameters</span></span>  
 `szFilePath`  
 <span data-ttu-id="d403c-108">[in] Le nom du fichier à hacher.</span><span class="sxs-lookup"><span data-stu-id="d403c-108">[in] The name of the file to hash.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="d403c-109">[in, out] L’algorithme à utiliser lors de la génération du hachage.</span><span class="sxs-lookup"><span data-stu-id="d403c-109">[in, out] The algorithm to use when generating the hash.</span></span> <span data-ttu-id="d403c-110">Les algorithmes valides sont ceux définis par l’interface CryptoAPI Win32.</span><span class="sxs-lookup"><span data-stu-id="d403c-110">Valid algorithms are those defined by the Win32 CryptoAPI.</span></span> <span data-ttu-id="d403c-111">Si `piHashAlg` est définie sur 0, l’algorithme par défaut CALG_SHA-1 est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d403c-111">If `piHashAlg` is set to 0, the default algorithm CALG_SHA-1 is used.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="d403c-112">[out] Tableau d’octets contenant le hachage généré.</span><span class="sxs-lookup"><span data-stu-id="d403c-112">[out] A byte array containing the generated hash.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="d403c-113">[in] La taille maximale de la mémoire tampon qui `pbHash` pointe vers.</span><span class="sxs-lookup"><span data-stu-id="d403c-113">[in] The maximum size of the buffer that `pbHash` points to.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="d403c-114">[out] La taille, en octets, de retourné `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="d403c-114">[out] The size, in bytes, of the returned `pbHash`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d403c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d403c-115">Remarks</span></span>  
 <span data-ttu-id="d403c-116">Cette fonction est identique à [GetHashFromFileW](../../../../docs/framework/unmanaged-api/strong-naming/gethashfromfilew-function.md), sauf que la spécification de nom de fichier est ANSI au lieu d’Unicode.</span><span class="sxs-lookup"><span data-stu-id="d403c-116">This function is the same as [GetHashFromFileW](../../../../docs/framework/unmanaged-api/strong-naming/gethashfromfilew-function.md), except that the file name specification is ANSI instead of Unicode.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d403c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d403c-117">Requirements</span></span>  
 <span data-ttu-id="d403c-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d403c-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d403c-119">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="d403c-119">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="d403c-120">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d403c-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="d403c-121">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="d403c-121">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="d403c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d403c-122">See also</span></span>

- [<span data-ttu-id="d403c-123">GetHashFromFile, méthode</span><span class="sxs-lookup"><span data-stu-id="d403c-123">GetHashFromFile Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfile-method.md)
- [<span data-ttu-id="d403c-124">GetHashFromFileW, méthode</span><span class="sxs-lookup"><span data-stu-id="d403c-124">GetHashFromFileW Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfilew-method.md)
- [<span data-ttu-id="d403c-125">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="d403c-125">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
