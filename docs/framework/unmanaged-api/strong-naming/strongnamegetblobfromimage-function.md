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
ms.openlocfilehash: 9d562aef58c1e3b5bbbe690b54eb08384052c657
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33456773"
---
# <a name="strongnamegetblobfromimage-function"></a><span data-ttu-id="cb718-102">StrongNameGetBlobFromImage, fonction</span><span class="sxs-lookup"><span data-stu-id="cb718-102">StrongNameGetBlobFromImage Function</span></span>
<span data-ttu-id="cb718-103">Obtient une représentation binaire de l’image d’assembly à l’adresse mémoire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cb718-103">Gets a binary representation of the assembly image at the specified memory address.</span></span>  
  
 <span data-ttu-id="cb718-104">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="cb718-104">This function has been deprecated.</span></span> <span data-ttu-id="cb718-105">Utilisez le [ICLRStrongName::StrongNameGetBlobFromImage](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblobfromimage-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="cb718-105">Use the [ICLRStrongName::StrongNameGetBlobFromImage](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblobfromimage-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cb718-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb718-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameGetBlobFromImage (  
    [in]  BYTE        *pbBase,  
    [in]  DWORD       dwLength,  
    [in]  BYTE        *pbBlob,  
    [in, out] DWORD   *pcbBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cb718-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb718-107">Parameters</span></span>  
 `pbBase`  
 <span data-ttu-id="cb718-108">[in] Adresse mémoire du manifeste d’assembly mappé.</span><span class="sxs-lookup"><span data-stu-id="cb718-108">[in] The memory address of the mapped assembly manifest.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="cb718-109">[in] La taille, en octets, de l’image à `pbBase`.</span><span class="sxs-lookup"><span data-stu-id="cb718-109">[in] The size, in bytes, of the image at `pbBase`.</span></span>  
  
 `pbBlob`  
 <span data-ttu-id="cb718-110">[in] Une mémoire tampon pour contenir la représentation binaire de l’image.</span><span class="sxs-lookup"><span data-stu-id="cb718-110">[in] A buffer to contain the binary representation of the image.</span></span>  
  
 `pcbBlob`  
 <span data-ttu-id="cb718-111">[dans, out] La taille maximale, en octets, demandée `pbBlob`.</span><span class="sxs-lookup"><span data-stu-id="cb718-111">[in, out] The requested maximum size, in bytes, of `pbBlob`.</span></span> <span data-ttu-id="cb718-112">Au retour, la taille réelle, en octets, de `pbBlob`.</span><span class="sxs-lookup"><span data-stu-id="cb718-112">Upon return, the actual size, in bytes, of `pbBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cb718-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cb718-113">Return Value</span></span>  
 <span data-ttu-id="cb718-114">`true` de réussite ; dans le cas contraire, `false`.</span><span class="sxs-lookup"><span data-stu-id="cb718-114">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cb718-115">Notes</span><span class="sxs-lookup"><span data-stu-id="cb718-115">Remarks</span></span>  
 <span data-ttu-id="cb718-116">Si le `StrongNameGetBlobFromImage` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.</span><span class="sxs-lookup"><span data-stu-id="cb718-116">If the `StrongNameGetBlobFromImage` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cb718-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cb718-117">Requirements</span></span>  
 <span data-ttu-id="cb718-118">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cb718-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cb718-119">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="cb718-119">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="cb718-120">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cb718-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="cb718-121">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cb718-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cb718-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb718-122">See Also</span></span>  
 [<span data-ttu-id="cb718-123">StrongNameGetBlobFromImage, méthode</span><span class="sxs-lookup"><span data-stu-id="cb718-123">StrongNameGetBlobFromImage Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblobfromimage-method.md)  
 [<span data-ttu-id="cb718-124">StrongNameGetBlob, méthode</span><span class="sxs-lookup"><span data-stu-id="cb718-124">StrongNameGetBlob Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblob-method.md)  
 [<span data-ttu-id="cb718-125">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="cb718-125">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
