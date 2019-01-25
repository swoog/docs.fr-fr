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
ms.openlocfilehash: fe15b855044a7bf45ea172f42436c3557b562037
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54687062"
---
# <a name="strongnametokenfromassembly-function"></a><span data-ttu-id="c7fc3-102">StrongNameTokenFromAssembly, fonction</span><span class="sxs-lookup"><span data-stu-id="c7fc3-102">StrongNameTokenFromAssembly Function</span></span>
<span data-ttu-id="c7fc3-103">Crée un jeton de nom fort à partir du fichier d’assembly spécifié.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-103">Creates a strong name token from the specified assembly file.</span></span>  
  
 <span data-ttu-id="c7fc3-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-104">This function has been deprecated.</span></span> <span data-ttu-id="c7fc3-105">Utilisez le [ICLRStrongName::StrongNameTokenFromAssembly](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassembly-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-105">Use the [ICLRStrongName::StrongNameTokenFromAssembly](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassembly-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7fc3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7fc3-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameTokenFromAssembly (  
    [in]  LPCWSTR   wszFilePath,  
    [out] BYTE      **ppbStrongNameToken,  
    [out] ULONG     *pcbStrongNameToken  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c7fc3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7fc3-107">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="c7fc3-108">[in] Le chemin d’accès au fichier exécutable portable (PE) pour l’assembly.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-108">[in] The path to the portable executable (PE) file for the assembly.</span></span>  
  
 `ppbStrongNameToken`  
 <span data-ttu-id="c7fc3-109">[out] Le jeton de nom fort retourné.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-109">[out] The returned strong name token.</span></span>  
  
 `pcbStrongNameToken`  
 <span data-ttu-id="c7fc3-110">[out] La taille, en octets, du jeton de nom fort.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-110">[out] The size, in bytes, of the strong name token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c7fc3-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c7fc3-111">Return Value</span></span>  
 <span data-ttu-id="c7fc3-112">`true` de réussite ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-112">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c7fc3-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c7fc3-113">Remarks</span></span>  
 <span data-ttu-id="c7fc3-114">Un jeton de nom fort est la forme abrégée d’une clé publique.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-114">A strong name token is the shortened form of a public key.</span></span> <span data-ttu-id="c7fc3-115">Le jeton est un hachage 64 bits qui est créé à partir de la clé publique utilisée pour signer l’assembly.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-115">The token is a 64-bit hash that is created from the public key used to sign the assembly.</span></span> <span data-ttu-id="c7fc3-116">Le jeton est une partie du nom fort pour l’assembly et peut être lues à partir des métadonnées d’assembly.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-116">The token is a part of the strong name for the assembly, and can be read from the assembly metadata.</span></span>  
  
 <span data-ttu-id="c7fc3-117">Une fois que le jeton est créé, vous devez appeler la [StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/strong-naming/strongnamefreebuffer-function.md) (fonction) pour libérer la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-117">After the token is created, you should call the [StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/strong-naming/strongnamefreebuffer-function.md) function to release the allocated memory.</span></span>  
  
 <span data-ttu-id="c7fc3-118">Si le `StrongNameTokenFromAssembly` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-118">If the `StrongNameTokenFromAssembly` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c7fc3-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c7fc3-119">Requirements</span></span>  
 <span data-ttu-id="c7fc3-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c7fc3-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c7fc3-121">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="c7fc3-121">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="c7fc3-122">**Bibliothèque :** Inclus en tant que ressource dans mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="c7fc3-122">**Library:** Included as a resource in mscoree.dll</span></span>  
  
 <span data-ttu-id="c7fc3-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c7fc3-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c7fc3-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7fc3-124">See also</span></span>
- [<span data-ttu-id="c7fc3-125">StrongNameTokenFromAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="c7fc3-125">StrongNameTokenFromAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassembly-method.md)
- [<span data-ttu-id="c7fc3-126">StrongNameTokenFromAssemblyEx, méthode</span><span class="sxs-lookup"><span data-stu-id="c7fc3-126">StrongNameTokenFromAssemblyEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassemblyex-method.md)
- [<span data-ttu-id="c7fc3-127">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="c7fc3-127">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
