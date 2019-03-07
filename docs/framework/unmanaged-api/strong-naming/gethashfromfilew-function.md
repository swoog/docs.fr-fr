---
title: GetHashFromFileW, fonction
ms.date: 03/30/2017
api_name:
- GetHashFromFileW
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromFileW
helpviewer_keywords:
- GetHashFromFileW function [.NET Framework strong naming]
ms.assetid: 97c2d7a6-5376-45a1-ba65-146a249147cc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6fc69ab8b2d3565c49eeee09d8860c81ec8818fe
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57473853"
---
# <a name="gethashfromfilew-function"></a><span data-ttu-id="8097c-102">GetHashFromFileW, fonction</span><span class="sxs-lookup"><span data-stu-id="8097c-102">GetHashFromFileW Function</span></span>
<span data-ttu-id="8097c-103">Génère un hachage sur le contenu du fichier spécifié par une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="8097c-103">Generates a hash over the contents of the file specified by a Unicode string.</span></span>  
  
 <span data-ttu-id="8097c-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8097c-104">This function has been deprecated.</span></span> <span data-ttu-id="8097c-105">Utilisez le [ICLRStrongName::GetHashFromFileW](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfilew-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="8097c-105">Use the [ICLRStrongName::GetHashFromFileW](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfilew-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8097c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8097c-106">Syntax</span></span>  
  
```  
HRESULT GetHashFromFileW (   
    [in]  LPCWSTR   wszFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE      *pbHash,  
    [in]  DWORD     cchHash,  
    [out] DWORD     *pchHash  
);   
```  
  
## <a name="parameters"></a><span data-ttu-id="8097c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8097c-107">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="8097c-108">[in] Le nom Unicode du fichier à hacher.</span><span class="sxs-lookup"><span data-stu-id="8097c-108">[in] The Unicode name of the file to hash.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="8097c-109">[in, out] L’algorithme à utiliser lors de la génération du hachage.</span><span class="sxs-lookup"><span data-stu-id="8097c-109">[in, out] The algorithm to use when generating the hash.</span></span> <span data-ttu-id="8097c-110">Les algorithmes valides sont ceux définis par l’interface CryptoAPI Win32.</span><span class="sxs-lookup"><span data-stu-id="8097c-110">Valid algorithms are those defined by the Win32 CryptoAPI.</span></span> <span data-ttu-id="8097c-111">Si `piHashAlg` est définie sur 0, l’algorithme par défaut CALG_SHA-1 est utilisé.</span><span class="sxs-lookup"><span data-stu-id="8097c-111">If `piHashAlg` is set to 0, the default algorithm CALG_SHA-1 is used.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="8097c-112">[out] Tableau d’octets contenant le hachage généré.</span><span class="sxs-lookup"><span data-stu-id="8097c-112">[out] A byte array containing the generated hash.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="8097c-113">[in] La taille maximale de la mémoire tampon vers laquelle pointe `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="8097c-113">[in] The maximum size of the buffer pointed to by `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="8097c-114">[out] La taille, en octets, de `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="8097c-114">[out] The size, in bytes, of `pbHash`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8097c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8097c-115">Remarks</span></span>  
 <span data-ttu-id="8097c-116">Cette fonction est identique à [GetHashFromFile](../../../../docs/framework/unmanaged-api/strong-naming/gethashfromfile-function.md), sauf que la spécification de nom de fichier est au format Unicode et non ANSI.</span><span class="sxs-lookup"><span data-stu-id="8097c-116">This function is the same as [GetHashFromFile](../../../../docs/framework/unmanaged-api/strong-naming/gethashfromfile-function.md), except that the file name specification is Unicode instead of ANSI.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8097c-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8097c-117">Requirements</span></span>  
 <span data-ttu-id="8097c-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8097c-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8097c-119">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="8097c-119">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="8097c-120">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8097c-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="8097c-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8097c-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8097c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8097c-122">See also</span></span>
- [<span data-ttu-id="8097c-123">GetHashFromFileW, méthode</span><span class="sxs-lookup"><span data-stu-id="8097c-123">GetHashFromFileW Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfilew-method.md)
- [<span data-ttu-id="8097c-124">GetHashFromFile, méthode</span><span class="sxs-lookup"><span data-stu-id="8097c-124">GetHashFromFile Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfile-method.md)
- [<span data-ttu-id="8097c-125">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="8097c-125">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
