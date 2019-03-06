---
title: StrongNameKeyInstall, fonction
ms.date: 03/30/2017
api_name:
- StrongNameKeyInstall
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameKeyInstall
helpviewer_keywords:
- StrongNameKeyInstall function [.NET Framework strong naming]
ms.assetid: e32fd546-7757-4681-be3d-658e93281e50
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6b3fc69b2edf611383402b13555cf33be10dbad3
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57366580"
---
# <a name="strongnamekeyinstall-function"></a><span data-ttu-id="084b9-102">StrongNameKeyInstall, fonction</span><span class="sxs-lookup"><span data-stu-id="084b9-102">StrongNameKeyInstall Function</span></span>

<span data-ttu-id="084b9-103">Importe une paire de clés publique/privée dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="084b9-103">Imports a public/private key pair into a container.</span></span>

<span data-ttu-id="084b9-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="084b9-104">This function has been deprecated.</span></span> <span data-ttu-id="084b9-105">Utilisez le [ICLRStrongName::StrongNameKeyInstall](../hosting/iclrstrongname-strongnamekeyinstall-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="084b9-105">Use the [ICLRStrongName::StrongNameKeyInstall](../hosting/iclrstrongname-strongnamekeyinstall-method.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="084b9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="084b9-106">Syntax</span></span>

```cpp
BOOLEAN StrongNameKeyInstall (
    [in]  LPCWSTR   wszKeyContainer,
    [in]  BYTE      *pbKeyBlob,
    [in]  ULONG     cbKeyBlob
);
```

## <a name="parameters"></a><span data-ttu-id="084b9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="084b9-107">Parameters</span></span>

`wszKeyContainer`\
<span data-ttu-id="084b9-108">[in] Le nom du conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="084b9-108">[in] The name of the key container.</span></span> <span data-ttu-id="084b9-109">`wszKeyContainer` doit être une chaîne non vide.</span><span class="sxs-lookup"><span data-stu-id="084b9-109">`wszKeyContainer` must be a non-empty string.</span></span>

`pbKeyBlob`\
<span data-ttu-id="084b9-110">[in] La paire de clés binaire.</span><span class="sxs-lookup"><span data-stu-id="084b9-110">[in] The binary key pair.</span></span>

`cbKeyBlob`\
<span data-ttu-id="084b9-111">[in] La taille, en octets, de `pbKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="084b9-111">[in] The size, in bytes, of `pbKeyBlob`.</span></span>

## <a name="return-value"></a><span data-ttu-id="084b9-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="084b9-112">Return Value</span></span>

<span data-ttu-id="084b9-113">`true` de réussite ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="084b9-113">`true` on successful completion; otherwise, `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="084b9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="084b9-114">Remarks</span></span>

<span data-ttu-id="084b9-115">Utilisez le [StrongNameKeyDelete](strongnamekeydelete-function.md) (fonction) pour supprimer le conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="084b9-115">Use the [StrongNameKeyDelete](strongnamekeydelete-function.md) function to delete the key container.</span></span>

<span data-ttu-id="084b9-116">Si le `StrongNameKeyInstall` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.</span><span class="sxs-lookup"><span data-stu-id="084b9-116">If the `StrongNameKeyInstall` function does not complete successfully, call the [StrongNameErrorInfo](strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>

## <a name="requirements"></a><span data-ttu-id="084b9-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="084b9-117">Requirements</span></span>

<span data-ttu-id="084b9-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="084b9-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

<span data-ttu-id="084b9-119">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="084b9-119">**Header:** StrongName.h</span></span>

<span data-ttu-id="084b9-120">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="084b9-120">**Library:** Included as a resource in MsCorEE.dll</span></span>

<span data-ttu-id="084b9-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="084b9-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="084b9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="084b9-122">See also</span></span>

- [<span data-ttu-id="084b9-123">StrongNameKeyInstall, méthode</span><span class="sxs-lookup"><span data-stu-id="084b9-123">StrongNameKeyInstall Method</span></span>](../hosting/iclrstrongname-strongnamekeyinstall-method.md)
- [<span data-ttu-id="084b9-124">StrongNameKeyDelete, méthode</span><span class="sxs-lookup"><span data-stu-id="084b9-124">StrongNameKeyDelete Method</span></span>](../hosting/iclrstrongname-strongnamekeydelete-method.md)
- [<span data-ttu-id="084b9-125">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="084b9-125">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)