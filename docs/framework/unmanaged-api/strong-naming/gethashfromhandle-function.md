---
title: GetHashFromHandle, fonction
ms.date: 03/30/2017
api_name:
- GetHashFromHandle
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromHandle
helpviewer_keywords:
- GetHashFromHandle function [.NET Framework strong naming]
ms.assetid: 9e00337f-b307-4602-9bc3-965a8dbf02cd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 48dd987896536006fe81bc01528cadb507123e27
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59203403"
---
# <a name="gethashfromhandle-function"></a><span data-ttu-id="0f4ef-102">GetHashFromHandle, fonction</span><span class="sxs-lookup"><span data-stu-id="0f4ef-102">GetHashFromHandle Function</span></span>
<span data-ttu-id="0f4ef-103">Génère un hachage sur le contenu du fichier avec le handle de fichier spécifié, à l’aide de l’algorithme de hachage spécifié.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-103">Generates a hash over the contents of the file with the specified file handle, using the specified hash algorithm.</span></span>  
  
 <span data-ttu-id="0f4ef-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-104">This function has been deprecated.</span></span> <span data-ttu-id="0f4ef-105">Utilisez le [ICLRStrongName::GetHashFromHandle](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromhandle-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-105">Use the [ICLRStrongName::GetHashFromHandle](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromhandle-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f4ef-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f4ef-106">Syntax</span></span>  
  
```  
HRESULT GetHashFromHandle (  
    [in]  HANDLE   hFile,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE     *pbHash,  
    [in]  DWORD    cchHash,  
    [out] DWORD    *pchHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0f4ef-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f4ef-107">Parameters</span></span>  
 `hFile`  
 <span data-ttu-id="0f4ef-108">[in] Le handle du fichier à hacher.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-108">[in] The handle of the file to be hashed.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="0f4ef-109">[in, out] Constante qui spécifie l’algorithme de hachage.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-109">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="0f4ef-110">Utilisez zéro pour l’algorithme par défaut.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-110">Use zero for the default algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="0f4ef-111">[out] La mémoire tampon de hachage retournée.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-111">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="0f4ef-112">[in] La taille maximale demandée de `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-112">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="0f4ef-113">[out] La taille, en octets, de retourné `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-113">[out] The size, in bytes, of the returned `pbHash`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0f4ef-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f4ef-114">Requirements</span></span>  
 <span data-ttu-id="0f4ef-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0f4ef-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0f4ef-116">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="0f4ef-116">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="0f4ef-117">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0f4ef-117">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="0f4ef-118">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="0f4ef-118">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0f4ef-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f4ef-119">See also</span></span>

- [<span data-ttu-id="0f4ef-120">GetHashFromHandle, méthode</span><span class="sxs-lookup"><span data-stu-id="0f4ef-120">GetHashFromHandle Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromhandle-method.md)
- [<span data-ttu-id="0f4ef-121">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="0f4ef-121">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
