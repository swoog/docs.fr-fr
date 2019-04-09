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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59160314"
---
# <a name="strongnamesignaturesize-function"></a><span data-ttu-id="24ce0-102">StrongNameSignatureSize, fonction</span><span class="sxs-lookup"><span data-stu-id="24ce0-102">StrongNameSignatureSize Function</span></span>
<span data-ttu-id="24ce0-103">Retourne la taille de la signature de nom fort.</span><span class="sxs-lookup"><span data-stu-id="24ce0-103">Returns the size of the strong name signature.</span></span> `StrongNameSignatureSize` <span data-ttu-id="24ce0-104">est généralement utilisé par les compilateurs pour déterminer la quantité d’espace à réserver dans le fichier lors de la création d’un assembly à signature différée.</span><span class="sxs-lookup"><span data-stu-id="24ce0-104">is typically used by compilers to determine how much space to reserve in the file when creating a delay-signed assembly.</span></span>  
  
 <span data-ttu-id="24ce0-105">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="24ce0-105">This function has been deprecated.</span></span> <span data-ttu-id="24ce0-106">Utilisez le [ICLRStrongName::StrongNameSignatureSize](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignaturesize-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="24ce0-106">Use the [ICLRStrongName::StrongNameSignatureSize](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignaturesize-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24ce0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24ce0-107">Syntax</span></span>  
  
```  
BOOLEAN StrongNameSignatureSize (   
    [in]  BYTE   *pbPublicKeyBlob,  
    [in]  ULONG  cbPublicKeyBlob,   
    [in]  DWORD  *pcbSize  
);   
```  
  
## <a name="parameters"></a><span data-ttu-id="24ce0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24ce0-108">Parameters</span></span>  
 `pbPublicKeyBlob`  
 <span data-ttu-id="24ce0-109">[in] Une structure de type [PublicKeyBlob](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md) qui contient la partie publique de la paire de clés utilisée pour générer la signature de nom fort.</span><span class="sxs-lookup"><span data-stu-id="24ce0-109">[in] A structure of type [PublicKeyBlob](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md) that contains the public portion of the key pair used to generate the strong name signature.</span></span>  
  
 `cbPublicKeyBlob`  
 <span data-ttu-id="24ce0-110">[in] La taille, en octets, de `pbPublicKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="24ce0-110">[in] The size, in bytes, of `pbPublicKeyBlob`.</span></span>  
  
 `pcbSize`  
 <span data-ttu-id="24ce0-111">[in] Le nombre d’octets requis pour stocker la signature de nom fort.</span><span class="sxs-lookup"><span data-stu-id="24ce0-111">[in] The number of bytes required to store the strong name signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="24ce0-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="24ce0-112">Return Value</span></span>  
 `true` <span data-ttu-id="24ce0-113">de réussite ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="24ce0-113">on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="24ce0-114">Notes</span><span class="sxs-lookup"><span data-stu-id="24ce0-114">Remarks</span></span>  
 <span data-ttu-id="24ce0-115">Si le `StrongNameSignatureSize` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.</span><span class="sxs-lookup"><span data-stu-id="24ce0-115">If the `StrongNameSignatureSize` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="24ce0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24ce0-116">Requirements</span></span>  
 <span data-ttu-id="24ce0-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="24ce0-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="24ce0-118">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="24ce0-118">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="24ce0-119">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="24ce0-119">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="24ce0-120">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="24ce0-120">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="24ce0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24ce0-121">See also</span></span>

- [<span data-ttu-id="24ce0-122">StrongNameSignatureSize, méthode</span><span class="sxs-lookup"><span data-stu-id="24ce0-122">StrongNameSignatureSize Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignaturesize-method.md)
- [<span data-ttu-id="24ce0-123">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="24ce0-123">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
