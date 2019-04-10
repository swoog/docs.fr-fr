---
title: StrongNameSignatureGeneration, fonction
ms.date: 03/30/2017
api_name:
- StrongNameSignatureGeneration
api_location:
- mscoree.dll
- mscorsn.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameSignatureGeneration
helpviewer_keywords:
- StrongNameSignatureGeneration function [.NET Framework strong naming]
ms.assetid: 839b765c-3e41-44ce-bf1b-dc10453db18e
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0e7df65c28fad6fa79ec7a18d8511955330b2817
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59227741"
---
# <a name="strongnamesignaturegeneration-function"></a><span data-ttu-id="f026e-102">StrongNameSignatureGeneration, fonction</span><span class="sxs-lookup"><span data-stu-id="f026e-102">StrongNameSignatureGeneration Function</span></span>
<span data-ttu-id="f026e-103">Génère une signature de nom fort pour l’assembly spécifié.</span><span class="sxs-lookup"><span data-stu-id="f026e-103">Generates a strong name signature for the specified assembly.</span></span>  
  
 <span data-ttu-id="f026e-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f026e-104">This function has been deprecated.</span></span> <span data-ttu-id="f026e-105">Utilisez le [ICLRStrongName::StrongNameSignatureGeneration](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignaturegeneration-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="f026e-105">Use the [ICLRStrongName::StrongNameSignatureGeneration](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignaturegeneration-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f026e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f026e-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameSignatureGeneration (   
    [in]  LPCWSTR   wszFilePath,  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob,  
    [out] BYTE      **ppbSignatureBlob,  
    [out] ULONG     *pcbSignatureBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f026e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f026e-107">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="f026e-108">[in] Le chemin d’accès au fichier qui contient le manifeste de l’assembly pour lequel la signature de nom fort est générée.</span><span class="sxs-lookup"><span data-stu-id="f026e-108">[in] The path to the file that contains the manifest of the assembly for which the strong name signature will be generated.</span></span>  
  
 `wszKeyContainer`  
 <span data-ttu-id="f026e-109">[in] Le nom du conteneur de clé qui contient la paire de clés publique/privée.</span><span class="sxs-lookup"><span data-stu-id="f026e-109">[in] The name of the key container that contains the public/private key pair.</span></span>  
  
 <span data-ttu-id="f026e-110">Si `pbKeyBlob` a la valeur null, `wszKeyContainer` doit spécifier un conteneur valid dans le fournisseur de services de chiffrement (CSP).</span><span class="sxs-lookup"><span data-stu-id="f026e-110">If `pbKeyBlob` is null, `wszKeyContainer` must specify a valid container within the cryptographic service provider (CSP).</span></span> <span data-ttu-id="f026e-111">Dans ce cas, la paire de clés stockée dans le conteneur est utilisée pour signer le fichier.</span><span class="sxs-lookup"><span data-stu-id="f026e-111">In this case, the key pair stored in the container is used to sign the file.</span></span>  
  
 <span data-ttu-id="f026e-112">Si `pbKeyBlob` n’est pas null, la paire de clés est supposée être contenue dans l’objet binaire volumineux (BLOB) de clé.</span><span class="sxs-lookup"><span data-stu-id="f026e-112">If `pbKeyBlob` is not null, the key pair is assumed to be contained in the key binary large object (BLOB).</span></span>  
  
 <span data-ttu-id="f026e-113">Les clés doivent être Rivest-Shamir-Adleman (RSA 1024 bits) clés de signature.</span><span class="sxs-lookup"><span data-stu-id="f026e-113">The keys must be 1024-bit Rivest-Shamir-Adleman (RSA) signing keys.</span></span> <span data-ttu-id="f026e-114">Aucun autre type de clés n’est pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="f026e-114">No other types of keys are supported at this time.</span></span>  
  
 `pbKeyBlob`  
 <span data-ttu-id="f026e-115">[in] Pointeur vers la paire de clés publique/privée.</span><span class="sxs-lookup"><span data-stu-id="f026e-115">[in] A pointer to the public/private key pair.</span></span> <span data-ttu-id="f026e-116">Cette paire est au format créé par Win32 `CryptExportKey` (fonction).</span><span class="sxs-lookup"><span data-stu-id="f026e-116">This pair is in the format created by the Win32 `CryptExportKey` function.</span></span> <span data-ttu-id="f026e-117">Si `pbKeyBlob` est null, le conteneur de clé spécifié par `wszKeyContainer` est supposée pour contenir la paire de clés.</span><span class="sxs-lookup"><span data-stu-id="f026e-117">If `pbKeyBlob` is null, the key container specified by `wszKeyContainer` is assumed to contain the key pair.</span></span>  
  
 `cbKeyBlob`  
 <span data-ttu-id="f026e-118">[in] La taille, en octets, de `pbKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="f026e-118">[in] The size, in bytes, of `pbKeyBlob`.</span></span>  
  
 `ppbSignatureBlob`  
 <span data-ttu-id="f026e-119">[out] Pointeur vers l’emplacement auquel le common language runtime retourne la signature.</span><span class="sxs-lookup"><span data-stu-id="f026e-119">[out] A pointer to the location to which the common language runtime returns the signature.</span></span> <span data-ttu-id="f026e-120">Si `ppbSignatureBlob` est null, le runtime stocke la signature dans le fichier spécifié par `wszFilePath`.</span><span class="sxs-lookup"><span data-stu-id="f026e-120">If `ppbSignatureBlob` is null, the runtime stores the signature in the file specified by `wszFilePath`.</span></span>  
  
 <span data-ttu-id="f026e-121">Si `ppbSignatureBlob` est non null, le common language runtime alloue de l’espace dans lequel retourner la signature.</span><span class="sxs-lookup"><span data-stu-id="f026e-121">If `ppbSignatureBlob` is not null, the common language runtime allocates space in which to return the signature.</span></span> <span data-ttu-id="f026e-122">L’appelant doit libérer cet espace à l’aide de la [StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/strong-naming/strongnamefreebuffer-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="f026e-122">The caller must free this space using the [StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/strong-naming/strongnamefreebuffer-function.md) function.</span></span>  
  
 `pcbSignatureBlob`  
 <span data-ttu-id="f026e-123">[out] La taille, en octets, de la signature retournée.</span><span class="sxs-lookup"><span data-stu-id="f026e-123">[out] The size, in bytes, of the returned signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f026e-124">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f026e-124">Return Value</span></span>  
 `true` <span data-ttu-id="f026e-125">de réussite ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="f026e-125">on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f026e-126">Notes</span><span class="sxs-lookup"><span data-stu-id="f026e-126">Remarks</span></span>  
 <span data-ttu-id="f026e-127">Spécifiez null pour `wszFilePath` pour calculer la taille de la signature sans créer la signature.</span><span class="sxs-lookup"><span data-stu-id="f026e-127">Specify null for `wszFilePath` to calculate the size of the signature without creating the signature.</span></span>  
  
 <span data-ttu-id="f026e-128">La signature peut être enregistrés directement dans le fichier, ou retourné à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f026e-128">The signature can be stored either directly in the file, or returned to the caller.</span></span>  
  
 <span data-ttu-id="f026e-129">Si le `StrongNameSignatureGeneration` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.</span><span class="sxs-lookup"><span data-stu-id="f026e-129">If the `StrongNameSignatureGeneration` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f026e-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f026e-130">Requirements</span></span>  
 <span data-ttu-id="f026e-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f026e-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f026e-132">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="f026e-132">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="f026e-133">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f026e-133">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="f026e-134">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="f026e-134">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="f026e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f026e-135">See also</span></span>

- [<span data-ttu-id="f026e-136">StrongNameSignatureGeneration, méthode</span><span class="sxs-lookup"><span data-stu-id="f026e-136">StrongNameSignatureGeneration Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignaturegeneration-method.md)
- [<span data-ttu-id="f026e-137">StrongNameSignatureGenerationEx, méthode</span><span class="sxs-lookup"><span data-stu-id="f026e-137">StrongNameSignatureGenerationEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignaturegenerationex-method.md)
- [<span data-ttu-id="f026e-138">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="f026e-138">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
