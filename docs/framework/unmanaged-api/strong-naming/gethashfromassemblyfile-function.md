---
title: GetHashFromAssemblyFile, fonction
ms.date: 03/30/2017
api_name:
- GetHashFromAssemblyFile
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromAssemblyFile
helpviewer_keywords:
- GetHashFromAssemblyFile function [.NET Framework strong naming]
ms.assetid: 751ed69f-b7ab-4e07-80de-e17ca9319b0c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5e9c0abcd395caf09ebe11e060a4b922e78ad1e6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33457930"
---
# <a name="gethashfromassemblyfile-function"></a><span data-ttu-id="13af2-102">GetHashFromAssemblyFile, fonction</span><span class="sxs-lookup"><span data-stu-id="13af2-102">GetHashFromAssemblyFile Function</span></span>
<span data-ttu-id="13af2-103">Obtient un hachage du fichier d’assembly spécifié, à l’aide de l’algorithme de hachage spécifié.</span><span class="sxs-lookup"><span data-stu-id="13af2-103">Gets a hash of the specified assembly file, using the specified hash algorithm.</span></span>  
  
 <span data-ttu-id="13af2-104">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="13af2-104">This function has been deprecated.</span></span> <span data-ttu-id="13af2-105">Utilisez le [ICLRStrongName::GetHashFromAssemblyFile](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfile-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="13af2-105">Use the [ICLRStrongName::GetHashFromAssemblyFile](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfile-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="13af2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13af2-106">Syntax</span></span>  
  
```  
HRESULT GetHashFromAssemblyFile (  
    [in]  LPCSTR   szFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE     *pbHash,  
    [in]  DWORD    cchHash,  
    [out] DWORD    *pchHash  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="13af2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13af2-107">Parameters</span></span>  
 `szFilePath`  
 <span data-ttu-id="13af2-108">[in] Le chemin d’accès au fichier à hacher.</span><span class="sxs-lookup"><span data-stu-id="13af2-108">[in] The path to the file to be hashed.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="13af2-109">[dans, out] Constante qui spécifie l’algorithme de hachage.</span><span class="sxs-lookup"><span data-stu-id="13af2-109">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="13af2-110">Utilisez zéro pour l’algorithme de hachage par défaut.</span><span class="sxs-lookup"><span data-stu-id="13af2-110">Use zero for the default hash algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="13af2-111">[out] La mémoire tampon de hachage retournée.</span><span class="sxs-lookup"><span data-stu-id="13af2-111">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="13af2-112">[in] La taille maximum demandée `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="13af2-112">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="13af2-113">[out] Le retournée, la taille, en octets, `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="13af2-113">[out] The returned size, in bytes, of `pbHash`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="13af2-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="13af2-114">Requirements</span></span>  
 <span data-ttu-id="13af2-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="13af2-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="13af2-116">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="13af2-116">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="13af2-117">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="13af2-117">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="13af2-118">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="13af2-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="13af2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13af2-119">See Also</span></span>  
 [<span data-ttu-id="13af2-120">GetHashFromAssemblyFile, méthode</span><span class="sxs-lookup"><span data-stu-id="13af2-120">GetHashFromAssemblyFile Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfile-method.md)  
 [<span data-ttu-id="13af2-121">GetHashFromAssemblyFileW, méthode</span><span class="sxs-lookup"><span data-stu-id="13af2-121">GetHashFromAssemblyFileW Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfilew-method.md)  
 [<span data-ttu-id="13af2-122">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="13af2-122">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
