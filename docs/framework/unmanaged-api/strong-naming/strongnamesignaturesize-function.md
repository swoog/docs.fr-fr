---
title: StrongNameSignatureSize, fonction
ms.date: 03/30/2017
api_name:
- StrongNameSignatureSize
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameSignatureSize
helpviewer_keywords:
- StrongNameSignatureSize function [.NET Framework strong naming]
ms.assetid: 4fde4cd0-f53e-4411-a2fe-fc5c54472f95
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 01c0f9ca0299e817618d93133c0eaca9fc63788e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61767505"
---
# <a name="strongnamesignaturesize-function"></a><span data-ttu-id="18823-102">StrongNameSignatureSize, fonction</span><span class="sxs-lookup"><span data-stu-id="18823-102">StrongNameSignatureSize Function</span></span>
<span data-ttu-id="18823-103">Retourne la taille de la signature de nom fort.</span><span class="sxs-lookup"><span data-stu-id="18823-103">Returns the size of the strong name signature.</span></span> <span data-ttu-id="18823-104">`StrongNameSignatureSize` est généralement utilisé par les compilateurs pour déterminer la quantité d’espace à réserver dans le fichier lors de la création d’un assembly à signature différée.</span><span class="sxs-lookup"><span data-stu-id="18823-104">`StrongNameSignatureSize` is typically used by compilers to determine how much space to reserve in the file when creating a delay-signed assembly.</span></span>  
  
 <span data-ttu-id="18823-105">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="18823-105">This function has been deprecated.</span></span> <span data-ttu-id="18823-106">Utilisez le [ICLRStrongName::StrongNameSignatureSize](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignaturesize-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="18823-106">Use the [ICLRStrongName::StrongNameSignatureSize](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignaturesize-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="18823-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18823-107">Syntax</span></span>  
  
```  
BOOLEAN StrongNameSignatureSize (   
    [in]  BYTE   *pbPublicKeyBlob,  
    [in]  ULONG  cbPublicKeyBlob,   
    [in]  DWORD  *pcbSize  
);   
```  
  
## <a name="parameters"></a><span data-ttu-id="18823-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18823-108">Parameters</span></span>  
 `pbPublicKeyBlob`  
 <span data-ttu-id="18823-109">[in] Une structure de type [PublicKeyBlob](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md) qui contient la partie publique de la paire de clés utilisée pour générer la signature de nom fort.</span><span class="sxs-lookup"><span data-stu-id="18823-109">[in] A structure of type [PublicKeyBlob](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md) that contains the public portion of the key pair used to generate the strong name signature.</span></span>  
  
 `cbPublicKeyBlob`  
 <span data-ttu-id="18823-110">[in] La taille, en octets, de `pbPublicKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="18823-110">[in] The size, in bytes, of `pbPublicKeyBlob`.</span></span>  
  
 `pcbSize`  
 <span data-ttu-id="18823-111">[in] Le nombre d’octets requis pour stocker la signature de nom fort.</span><span class="sxs-lookup"><span data-stu-id="18823-111">[in] The number of bytes required to store the strong name signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="18823-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="18823-112">Return Value</span></span>  
 <span data-ttu-id="18823-113">`true` de réussite ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="18823-113">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="18823-114">Notes</span><span class="sxs-lookup"><span data-stu-id="18823-114">Remarks</span></span>  
 <span data-ttu-id="18823-115">Si le `StrongNameSignatureSize` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.</span><span class="sxs-lookup"><span data-stu-id="18823-115">If the `StrongNameSignatureSize` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="18823-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18823-116">Requirements</span></span>  
 <span data-ttu-id="18823-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="18823-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="18823-118">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="18823-118">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="18823-119">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="18823-119">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="18823-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="18823-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="18823-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18823-121">See also</span></span>

- [<span data-ttu-id="18823-122">StrongNameSignatureSize, méthode</span><span class="sxs-lookup"><span data-stu-id="18823-122">StrongNameSignatureSize Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignaturesize-method.md)
- [<span data-ttu-id="18823-123">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="18823-123">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
