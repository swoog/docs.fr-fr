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
ms.openlocfilehash: e56a509d08b19cf449177984e7b59481eb7b09a9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049399"
---
# <a name="gethashfromassemblyfile-function"></a><span data-ttu-id="d9bbd-102">GetHashFromAssemblyFile, fonction</span><span class="sxs-lookup"><span data-stu-id="d9bbd-102">GetHashFromAssemblyFile Function</span></span>
<span data-ttu-id="d9bbd-103">Obtient un hachage du fichier d’assembly spécifié, à l’aide de l’algorithme de hachage spécifié.</span><span class="sxs-lookup"><span data-stu-id="d9bbd-103">Gets a hash of the specified assembly file, using the specified hash algorithm.</span></span>  
  
 <span data-ttu-id="d9bbd-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d9bbd-104">This function has been deprecated.</span></span> <span data-ttu-id="d9bbd-105">Utilisez le [ICLRStrongName::GetHashFromAssemblyFile](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfile-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="d9bbd-105">Use the [ICLRStrongName::GetHashFromAssemblyFile](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfile-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9bbd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9bbd-106">Syntax</span></span>  
  
```  
HRESULT GetHashFromAssemblyFile (  
    [in]  LPCSTR   szFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE     *pbHash,  
    [in]  DWORD    cchHash,  
    [out] DWORD    *pchHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d9bbd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9bbd-107">Parameters</span></span>  
 `szFilePath`  
 <span data-ttu-id="d9bbd-108">[in] Le chemin d’accès au fichier à hacher.</span><span class="sxs-lookup"><span data-stu-id="d9bbd-108">[in] The path to the file to be hashed.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="d9bbd-109">[in, out] Constante qui spécifie l’algorithme de hachage.</span><span class="sxs-lookup"><span data-stu-id="d9bbd-109">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="d9bbd-110">Utilisez zéro pour l’algorithme de hachage par défaut.</span><span class="sxs-lookup"><span data-stu-id="d9bbd-110">Use zero for the default hash algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="d9bbd-111">[out] La mémoire tampon de hachage retournée.</span><span class="sxs-lookup"><span data-stu-id="d9bbd-111">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="d9bbd-112">[in] La taille maximale demandée de `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="d9bbd-112">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="d9bbd-113">[out] L’a retourné la taille, en octets, de `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="d9bbd-113">[out] The returned size, in bytes, of `pbHash`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d9bbd-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9bbd-114">Requirements</span></span>  
 <span data-ttu-id="d9bbd-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d9bbd-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d9bbd-116">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="d9bbd-116">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="d9bbd-117">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d9bbd-117">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d9bbd-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d9bbd-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9bbd-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9bbd-119">See also</span></span>

- [<span data-ttu-id="d9bbd-120">GetHashFromAssemblyFile, méthode</span><span class="sxs-lookup"><span data-stu-id="d9bbd-120">GetHashFromAssemblyFile Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfile-method.md)
- [<span data-ttu-id="d9bbd-121">GetHashFromAssemblyFileW, méthode</span><span class="sxs-lookup"><span data-stu-id="d9bbd-121">GetHashFromAssemblyFileW Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfilew-method.md)
- [<span data-ttu-id="d9bbd-122">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="d9bbd-122">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
