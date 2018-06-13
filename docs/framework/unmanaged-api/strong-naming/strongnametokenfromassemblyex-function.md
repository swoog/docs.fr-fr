---
title: StrongNameTokenFromAssemblyEx, fonction
ms.date: 03/30/2017
api_name:
- StrongNameTokenFromAssemblyEx
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameTokenFromAssemblyEx
helpviewer_keywords:
- StrongNameTokenFromAssemblyEx function [.NET Framework strong naming]
ms.assetid: 67a8a9f2-dee3-44b2-a1c0-f307a3bdf90f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 20bafd0dfc455538292e47ca33508c251ad68614
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33458173"
---
# <a name="strongnametokenfromassemblyex-function"></a><span data-ttu-id="ae29f-102">StrongNameTokenFromAssemblyEx, fonction</span><span class="sxs-lookup"><span data-stu-id="ae29f-102">StrongNameTokenFromAssemblyEx Function</span></span>
<span data-ttu-id="ae29f-103">Crée un jeton de nom fort à partir du fichier d’assembly spécifié et retourne la clé publique que le jeton représente.</span><span class="sxs-lookup"><span data-stu-id="ae29f-103">Creates a strong name token from the specified assembly file, and returns the public key that the token represents.</span></span>  
  
 <span data-ttu-id="ae29f-104">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="ae29f-104">This function has been deprecated.</span></span> <span data-ttu-id="ae29f-105">Utilisez le [ICLRStrongName::StrongNameTokenFromAssemblyEx](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassemblyex-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="ae29f-105">Use the [ICLRStrongName::StrongNameTokenFromAssemblyEx](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassemblyex-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae29f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae29f-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameTokenFromAssemblyEx (  
    [in]  LPCWSTR   wszFilePath,  
    [out] BYTE      **ppbStrongNameToken,  
    [out] ULONG     *pcbStrongNameToken,  
    [out] BYTE      **ppbPublicKeyBlob,  
    [out] ULONG     *pcbPublicKeyBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ae29f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae29f-107">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="ae29f-108">[in] Le chemin d’accès au fichier exécutable portable (PE) pour l’assembly.</span><span class="sxs-lookup"><span data-stu-id="ae29f-108">[in] The path to the portable executable (PE) file for the assembly.</span></span>  
  
 `ppbStrongNameToken`  
 <span data-ttu-id="ae29f-109">[out] Le jeton de nom fort retourné.</span><span class="sxs-lookup"><span data-stu-id="ae29f-109">[out] The returned strong name token.</span></span>  
  
 `pcbStrongNameToken`  
 <span data-ttu-id="ae29f-110">[out] La taille, en octets, du jeton de nom fort.</span><span class="sxs-lookup"><span data-stu-id="ae29f-110">[out] The size, in bytes, of the strong name token.</span></span>  
  
 `ppbPublicKeyBlob`  
 <span data-ttu-id="ae29f-111">[out] La clé publique retournée.</span><span class="sxs-lookup"><span data-stu-id="ae29f-111">[out] The returned public key.</span></span>  
  
 `pcbPublicKeyBlob`  
 <span data-ttu-id="ae29f-112">[out] La taille, en octets, de la clé publique.</span><span class="sxs-lookup"><span data-stu-id="ae29f-112">[out] The size, in bytes, of the public key.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ae29f-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ae29f-113">Return Value</span></span>  
 <span data-ttu-id="ae29f-114">`true` de réussite ; dans le cas contraire, `false`.</span><span class="sxs-lookup"><span data-stu-id="ae29f-114">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ae29f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ae29f-115">Remarks</span></span>  
 <span data-ttu-id="ae29f-116">Un jeton de nom fort est la forme abrégée d’une clé publique.</span><span class="sxs-lookup"><span data-stu-id="ae29f-116">A strong name token is the shortened form of a public key.</span></span> <span data-ttu-id="ae29f-117">Le jeton est un hachage 64 bits qui est créé à partir de la clé publique utilisée pour signer l’assembly.</span><span class="sxs-lookup"><span data-stu-id="ae29f-117">The token is a 64-bit hash that is created from the public key used to sign the assembly.</span></span> <span data-ttu-id="ae29f-118">Le jeton fait partie du nom fort de l’assembly et peut être lus à partir des métadonnées de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="ae29f-118">The token is a part of the strong name for the assembly, and can be read from the assembly metadata.</span></span>  
  
 <span data-ttu-id="ae29f-119">Une fois que la clé est récupérée et le jeton est créé, vous devez appeler la [StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/strong-naming/strongnamefreebuffer-function.md) afin de libérer la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="ae29f-119">After the key is retrieved and the token is created, you should call the [StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/strong-naming/strongnamefreebuffer-function.md) function to release the allocated memory.</span></span>  
  
 <span data-ttu-id="ae29f-120">Si le `StrongNameTokenFromAssemblyEx` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.</span><span class="sxs-lookup"><span data-stu-id="ae29f-120">If the `StrongNameTokenFromAssemblyEx` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae29f-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ae29f-121">Requirements</span></span>  
 <span data-ttu-id="ae29f-122">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ae29f-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae29f-123">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="ae29f-123">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="ae29f-124">**Bibliothèque :** inclus en tant que ressource dans mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ae29f-124">**Library:** Included as a resource in mscoree.dll</span></span>  
  
 <span data-ttu-id="ae29f-125">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae29f-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae29f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae29f-126">See Also</span></span>  
 [<span data-ttu-id="ae29f-127">StrongNameTokenFromAssemblyEx, méthode</span><span class="sxs-lookup"><span data-stu-id="ae29f-127">StrongNameTokenFromAssemblyEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassemblyex-method.md)  
 [<span data-ttu-id="ae29f-128">StrongNameTokenFromAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="ae29f-128">StrongNameTokenFromAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassembly-method.md)  
 [<span data-ttu-id="ae29f-129">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="ae29f-129">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
