---
title: GetHashFromBlob, fonction
ms.date: 03/30/2017
api_name:
- GetHashFromBlob
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromBlob
helpviewer_keywords:
- GetHashFromBlob function [.NET Framework strong naming]
ms.assetid: b712d862-f2d0-4b55-87d4-65bbeadef982
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3d9e7b52c9061a1a7b470f9d4abf735e605087dc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62000530"
---
# <a name="gethashfromblob-function"></a><span data-ttu-id="7b6e0-102">GetHashFromBlob, fonction</span><span class="sxs-lookup"><span data-stu-id="7b6e0-102">GetHashFromBlob Function</span></span>

<span data-ttu-id="7b6e0-103">Obtient un hachage de l’assembly à l’adresse mémoire spécifiée, à l’aide de l’algorithme de hachage spécifié.</span><span class="sxs-lookup"><span data-stu-id="7b6e0-103">Gets a hash of the assembly at the specified memory address, using the specified hash algorithm.</span></span>

<span data-ttu-id="7b6e0-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7b6e0-104">This function has been deprecated.</span></span> <span data-ttu-id="7b6e0-105">Utilisez le [ICLRStrongName::GetHashFromBlob](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromblob-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="7b6e0-105">Use the [ICLRStrongName::GetHashFromBlob](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromblob-method.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b6e0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b6e0-106">Syntax</span></span>

```cpp
HRESULT GetHashFromBlob (
    [in]  BYTE    *pbBlob,
    [in]  DWORD   cchBlob,
    [in, out] unsigned int   *piHashAlg,
    [out] BYTE    *pbHash,
    [in]  DWORD   cchHash,
    [out] DWORD   *pchHash
);
```

## <a name="parameters"></a><span data-ttu-id="7b6e0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b6e0-107">Parameters</span></span>

`pbBlob`\
<span data-ttu-id="7b6e0-108">[in] Pointeur vers l’adresse du bloc de mémoire à hacher.</span><span class="sxs-lookup"><span data-stu-id="7b6e0-108">[in] A pointer to the address of the memory block to be hashed.</span></span>

`cchBlob`\
<span data-ttu-id="7b6e0-109">[in] La longueur, en octets, du bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="7b6e0-109">[in] The length, in bytes, of the memory block.</span></span>

`piHashAlg`\
<span data-ttu-id="7b6e0-110">[in, out] Constante qui spécifie l’algorithme de hachage.</span><span class="sxs-lookup"><span data-stu-id="7b6e0-110">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="7b6e0-111">Utilisez zéro pour l’algorithme par défaut.</span><span class="sxs-lookup"><span data-stu-id="7b6e0-111">Use zero for the default algorithm.</span></span>

`pbHash`\
<span data-ttu-id="7b6e0-112">[out] La mémoire tampon de hachage retournée.</span><span class="sxs-lookup"><span data-stu-id="7b6e0-112">[out] The returned hash buffer.</span></span>

`cchHash`\
<span data-ttu-id="7b6e0-113">[in] La taille maximale demandée de `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="7b6e0-113">[in] The requested maximum size of `pbHash`.</span></span>

`pchHash`\
<span data-ttu-id="7b6e0-114">[out] La taille, en octets, de retourné `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="7b6e0-114">[out] The size, in bytes, of the returned `pbHash`.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b6e0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b6e0-115">Requirements</span></span>

<span data-ttu-id="7b6e0-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7b6e0-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

<span data-ttu-id="7b6e0-117">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="7b6e0-117">**Header:** StrongName.h</span></span>

<span data-ttu-id="7b6e0-118">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7b6e0-118">**Library:** Included as a resource in MsCorEE.dll</span></span>

<span data-ttu-id="7b6e0-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7b6e0-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="7b6e0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b6e0-120">See also</span></span>

- [<span data-ttu-id="7b6e0-121">GetHashFromBlob, méthode</span><span class="sxs-lookup"><span data-stu-id="7b6e0-121">GetHashFromBlob Method</span></span>](../hosting/iclrstrongname-gethashfromblob-method.md)
- [<span data-ttu-id="7b6e0-122">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="7b6e0-122">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)