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
ms.openlocfilehash: 578dd7941ad7a2cf1d39a3aeed7fa823eb7efa79
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59162161"
---
# <a name="iclrstrongnamegethashfromassemblyfilew-method"></a><span data-ttu-id="a0fc8-102">Méthode ICLRStrongName::GetHashFromAssemblyFileW</span><span class="sxs-lookup"><span data-stu-id="a0fc8-102">ICLRStrongName::GetHashFromAssemblyFileW Method</span></span>
<span data-ttu-id="a0fc8-103">Génère un hachage sur le contenu du fichier spécifié par une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="a0fc8-103">Generates a hash over the contents of the file specified by a Unicode string.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a0fc8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0fc8-104">Syntax</span></span>  
  
```  
HRESULT GetHashFromAssemblyFileW (  
    [in]  LPCWSTR   wszFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE      *pbHash,  
    [in]  DWORD     cchHash,  
    [out] DWORD     *pchHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a0fc8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0fc8-105">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="a0fc8-106">[in] Le chemin d’accès au fichier à hacher.</span><span class="sxs-lookup"><span data-stu-id="a0fc8-106">[in] The path to the file to be hashed.</span></span> <span data-ttu-id="a0fc8-107">Ce paramètre doit être une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="a0fc8-107">This parameter must be a Unicode string.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="a0fc8-108">[in, out] Constante qui spécifie l’algorithme de hachage.</span><span class="sxs-lookup"><span data-stu-id="a0fc8-108">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="a0fc8-109">Utilisez zéro pour l’algorithme de hachage par défaut.</span><span class="sxs-lookup"><span data-stu-id="a0fc8-109">Use zero for the default hash algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="a0fc8-110">[out] La mémoire tampon de hachage retournée.</span><span class="sxs-lookup"><span data-stu-id="a0fc8-110">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="a0fc8-111">[in] La taille maximale demandée de `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="a0fc8-111">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="a0fc8-112">[out] L’a retourné la taille, en octets, de `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="a0fc8-112">[out] The returned size, in bytes, of `pbHash`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a0fc8-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a0fc8-113">Return Value</span></span>  
 `S_OK` <span data-ttu-id="a0fc8-114">Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (consultez [valeurs HRESULT courantes](https://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).</span><span class="sxs-lookup"><span data-stu-id="a0fc8-114">if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a0fc8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0fc8-115">Requirements</span></span>  
 <span data-ttu-id="a0fc8-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a0fc8-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a0fc8-117">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="a0fc8-117">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="a0fc8-118">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a0fc8-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="a0fc8-119">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="a0fc8-119">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="a0fc8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0fc8-120">See also</span></span>

- [<span data-ttu-id="a0fc8-121">GetHashFromAssemblyFile, méthode</span><span class="sxs-lookup"><span data-stu-id="a0fc8-121">GetHashFromAssemblyFile Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfile-method.md)
- [<span data-ttu-id="a0fc8-122">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="a0fc8-122">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
