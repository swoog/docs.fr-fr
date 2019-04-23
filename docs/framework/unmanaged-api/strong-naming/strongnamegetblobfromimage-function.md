---
title: StrongNameGetBlobFromImage, fonction
ms.date: 03/30/2017
api_name:
- StrongNameGetBlobFromImage
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameGetBlobFromImage
helpviewer_keywords:
- StrongNameGetBlobFromImage function [.NET Framework strong naming]
ms.assetid: 1de658e6-da32-4d01-9097-6f43c92222e1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b136e1fa480e53bcacfd9ea832d1dc4d1bd69f74
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59162774"
---
# <a name="strongnamegetblobfromimage-function"></a><span data-ttu-id="f3802-102">StrongNameGetBlobFromImage, fonction</span><span class="sxs-lookup"><span data-stu-id="f3802-102">StrongNameGetBlobFromImage Function</span></span>
<span data-ttu-id="f3802-103">Obtient une représentation binaire de l’image de l’assembly à l’adresse mémoire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f3802-103">Gets a binary representation of the assembly image at the specified memory address.</span></span>  
  
 <span data-ttu-id="f3802-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f3802-104">This function has been deprecated.</span></span> <span data-ttu-id="f3802-105">Utilisez le [ICLRStrongName::StrongNameGetBlobFromImage](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblobfromimage-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="f3802-105">Use the [ICLRStrongName::StrongNameGetBlobFromImage](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblobfromimage-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f3802-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3802-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameGetBlobFromImage (  
    [in]  BYTE        *pbBase,  
    [in]  DWORD       dwLength,  
    [in]  BYTE        *pbBlob,  
    [in, out] DWORD   *pcbBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f3802-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3802-107">Parameters</span></span>  
 `pbBase`  
 <span data-ttu-id="f3802-108">[in] L’adresse mémoire du manifeste d’assembly mappé.</span><span class="sxs-lookup"><span data-stu-id="f3802-108">[in] The memory address of the mapped assembly manifest.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="f3802-109">[in] La taille, en octets, de l’image à `pbBase`.</span><span class="sxs-lookup"><span data-stu-id="f3802-109">[in] The size, in bytes, of the image at `pbBase`.</span></span>  
  
 `pbBlob`  
 <span data-ttu-id="f3802-110">[in] Une mémoire tampon pour contenir la représentation binaire de l’image.</span><span class="sxs-lookup"><span data-stu-id="f3802-110">[in] A buffer to contain the binary representation of the image.</span></span>  
  
 `pcbBlob`  
 <span data-ttu-id="f3802-111">[in, out] La taille maximale en octets, demandée de `pbBlob`.</span><span class="sxs-lookup"><span data-stu-id="f3802-111">[in, out] The requested maximum size, in bytes, of `pbBlob`.</span></span> <span data-ttu-id="f3802-112">Au retour, la taille réelle, en octets, de `pbBlob`.</span><span class="sxs-lookup"><span data-stu-id="f3802-112">Upon return, the actual size, in bytes, of `pbBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f3802-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f3802-113">Return Value</span></span>  
 <span data-ttu-id="f3802-114">`true` de réussite ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="f3802-114">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f3802-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f3802-115">Remarks</span></span>  
 <span data-ttu-id="f3802-116">Si le `StrongNameGetBlobFromImage` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.</span><span class="sxs-lookup"><span data-stu-id="f3802-116">If the `StrongNameGetBlobFromImage` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f3802-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3802-117">Requirements</span></span>  
 <span data-ttu-id="f3802-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f3802-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f3802-119">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="f3802-119">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="f3802-120">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f3802-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f3802-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f3802-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3802-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3802-122">See also</span></span>

- [<span data-ttu-id="f3802-123">StrongNameGetBlobFromImage, méthode</span><span class="sxs-lookup"><span data-stu-id="f3802-123">StrongNameGetBlobFromImage Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblobfromimage-method.md)
- [<span data-ttu-id="f3802-124">StrongNameGetBlob, méthode</span><span class="sxs-lookup"><span data-stu-id="f3802-124">StrongNameGetBlob Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblob-method.md)
- [<span data-ttu-id="f3802-125">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="f3802-125">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
