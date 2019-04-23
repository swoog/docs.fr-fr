---
title: StrongNameTokenFromAssembly, fonction
ms.date: 03/30/2017
api_name:
- StrongNameTokenFromAssembly
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameTokenFromAssembly
helpviewer_keywords:
- StrongNameTokenFromAssembly function [.NET Framework strong naming]
ms.assetid: 0a4b47ee-02f6-4a98-864e-a6f11ca3f2d9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f88c0feea48ee96745effc36798bb26b4ccbf3cc
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59168673"
---
# <a name="strongnametokenfromassembly-function"></a><span data-ttu-id="e252c-102">StrongNameTokenFromAssembly, fonction</span><span class="sxs-lookup"><span data-stu-id="e252c-102">StrongNameTokenFromAssembly Function</span></span>
<span data-ttu-id="e252c-103">Crée un jeton de nom fort à partir du fichier d’assembly spécifié.</span><span class="sxs-lookup"><span data-stu-id="e252c-103">Creates a strong name token from the specified assembly file.</span></span>  
  
 <span data-ttu-id="e252c-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e252c-104">This function has been deprecated.</span></span> <span data-ttu-id="e252c-105">Utilisez le [ICLRStrongName::StrongNameTokenFromAssembly](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassembly-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="e252c-105">Use the [ICLRStrongName::StrongNameTokenFromAssembly](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassembly-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e252c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e252c-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameTokenFromAssembly (  
    [in]  LPCWSTR   wszFilePath,  
    [out] BYTE      **ppbStrongNameToken,  
    [out] ULONG     *pcbStrongNameToken  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e252c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e252c-107">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="e252c-108">[in] Le chemin d’accès au fichier exécutable portable (PE) pour l’assembly.</span><span class="sxs-lookup"><span data-stu-id="e252c-108">[in] The path to the portable executable (PE) file for the assembly.</span></span>  
  
 `ppbStrongNameToken`  
 <span data-ttu-id="e252c-109">[out] Le jeton de nom fort retourné.</span><span class="sxs-lookup"><span data-stu-id="e252c-109">[out] The returned strong name token.</span></span>  
  
 `pcbStrongNameToken`  
 <span data-ttu-id="e252c-110">[out] La taille, en octets, du jeton de nom fort.</span><span class="sxs-lookup"><span data-stu-id="e252c-110">[out] The size, in bytes, of the strong name token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e252c-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e252c-111">Return Value</span></span>  
 <span data-ttu-id="e252c-112">`true` de réussite ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="e252c-112">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e252c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e252c-113">Remarks</span></span>  
 <span data-ttu-id="e252c-114">Un jeton de nom fort est la forme abrégée d’une clé publique.</span><span class="sxs-lookup"><span data-stu-id="e252c-114">A strong name token is the shortened form of a public key.</span></span> <span data-ttu-id="e252c-115">Le jeton est un hachage 64 bits qui est créé à partir de la clé publique utilisée pour signer l’assembly.</span><span class="sxs-lookup"><span data-stu-id="e252c-115">The token is a 64-bit hash that is created from the public key used to sign the assembly.</span></span> <span data-ttu-id="e252c-116">Le jeton est une partie du nom fort pour l’assembly et peut être lues à partir des métadonnées d’assembly.</span><span class="sxs-lookup"><span data-stu-id="e252c-116">The token is a part of the strong name for the assembly, and can be read from the assembly metadata.</span></span>  
  
 <span data-ttu-id="e252c-117">Une fois que le jeton est créé, vous devez appeler la [StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/strong-naming/strongnamefreebuffer-function.md) (fonction) pour libérer la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="e252c-117">After the token is created, you should call the [StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/strong-naming/strongnamefreebuffer-function.md) function to release the allocated memory.</span></span>  
  
 <span data-ttu-id="e252c-118">Si le `StrongNameTokenFromAssembly` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.</span><span class="sxs-lookup"><span data-stu-id="e252c-118">If the `StrongNameTokenFromAssembly` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e252c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e252c-119">Requirements</span></span>  
 <span data-ttu-id="e252c-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e252c-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e252c-121">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="e252c-121">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="e252c-122">**Bibliothèque :** Inclus en tant que ressource dans mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="e252c-122">**Library:** Included as a resource in mscoree.dll</span></span>  
  
 <span data-ttu-id="e252c-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e252c-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e252c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e252c-124">See also</span></span>

- [<span data-ttu-id="e252c-125">StrongNameTokenFromAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="e252c-125">StrongNameTokenFromAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassembly-method.md)
- [<span data-ttu-id="e252c-126">StrongNameTokenFromAssemblyEx, méthode</span><span class="sxs-lookup"><span data-stu-id="e252c-126">StrongNameTokenFromAssemblyEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassemblyex-method.md)
- [<span data-ttu-id="e252c-127">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="e252c-127">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
