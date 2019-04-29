---
title: Méthode ICLRStrongName::StrongNameGetPublicKey
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameGetPublicKey
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameGetPublicKey
helpviewer_keywords:
- StrongNameGetPublicKey method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameGetPublicKey method [.NET Framework hosting]
ms.assetid: a31dcaa9-a404-4c1d-8cc7-081827c52935
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2acade14f9d30ca7bf0d098d6f58c80a367f621c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61795939"
---
# <a name="iclrstrongnamestrongnamegetpublickey-method"></a><span data-ttu-id="8be5a-102">Méthode ICLRStrongName::StrongNameGetPublicKey</span><span class="sxs-lookup"><span data-stu-id="8be5a-102">ICLRStrongName::StrongNameGetPublicKey Method</span></span>
<span data-ttu-id="8be5a-103">Obtient la clé publique à partir d’une paire de clés publique/privée.</span><span class="sxs-lookup"><span data-stu-id="8be5a-103">Gets the public key from a public/private key pair.</span></span> <span data-ttu-id="8be5a-104">La paire de clés peut être fournie sous la forme d’un nom de conteneur de clé au sein d’un fournisseur de services de chiffrement (CSP) ou une collection brute d’octets.</span><span class="sxs-lookup"><span data-stu-id="8be5a-104">The key pair can be supplied either as a key container name within a cryptographic service provider (CSP) or as a raw collection of bytes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8be5a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8be5a-105">Syntax</span></span>  
  
```  
HRESULT StrongNameGetPublicKey (   
    [in]  LPCWSTR   szKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob,  
    [out] BYTE      **ppbPublicKeyBlob,  
    [out] ULONG     *pcbPublicKeyBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8be5a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8be5a-106">Parameters</span></span>  
 `szKeyContainer`  
 <span data-ttu-id="8be5a-107">[in] Le nom du conteneur de clé qui contient la paire de clés publique/privée.</span><span class="sxs-lookup"><span data-stu-id="8be5a-107">[in] The name of the key container that contains the public/private key pair.</span></span> <span data-ttu-id="8be5a-108">Si `pbKeyBlob` a la valeur null, `szKeyContainer` doit spécifier un conteneur valid dans le CSP.</span><span class="sxs-lookup"><span data-stu-id="8be5a-108">If `pbKeyBlob` is null, `szKeyContainer` must specify a valid container within the CSP.</span></span> <span data-ttu-id="8be5a-109">Dans ce cas, le [ICLRStrongName::StrongNameGetPublicKey](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetpublickey-method.md) méthode extrait la clé publique de la paire de clés stockée dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="8be5a-109">In this case, the [ICLRStrongName::StrongNameGetPublicKey](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetpublickey-method.md) method extracts the public key from the key pair stored in the container.</span></span>  
  
 <span data-ttu-id="8be5a-110">Si `pbKeyBlob` n’est pas null, la paire de clés est supposée être contenue dans l’objet binaire volumineux (BLOB) de clé.</span><span class="sxs-lookup"><span data-stu-id="8be5a-110">If `pbKeyBlob` is not null, the key pair is assumed to be contained in the key binary large object (BLOB).</span></span>  
  
 <span data-ttu-id="8be5a-111">Les clés doivent être Rivest-Shamir-Adleman (RSA 1024 bits) clés de signature.</span><span class="sxs-lookup"><span data-stu-id="8be5a-111">The keys must be 1024-bit Rivest-Shamir-Adleman (RSA) signing keys.</span></span> <span data-ttu-id="8be5a-112">Aucun autre type de clés n’est pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="8be5a-112">No other types of keys are supported at this time.</span></span>  
  
 `pbKeyBlob`  
 <span data-ttu-id="8be5a-113">[in] Pointeur vers la paire de clés publique/privée.</span><span class="sxs-lookup"><span data-stu-id="8be5a-113">[in] A pointer to the public/private key pair.</span></span> <span data-ttu-id="8be5a-114">Cette paire est au format créé par Win32 `CryptExportKey` (fonction).</span><span class="sxs-lookup"><span data-stu-id="8be5a-114">This pair is in the format created by the Win32 `CryptExportKey` function.</span></span> <span data-ttu-id="8be5a-115">Si `pbKeyBlob` est null, le conteneur de clé spécifié par `szKeyContainer` est supposée pour contenir la paire de clés.</span><span class="sxs-lookup"><span data-stu-id="8be5a-115">If `pbKeyBlob` is null, the key container specified by `szKeyContainer` is assumed to contain the key pair.</span></span>  
  
 `cbKeyBlob`  
 <span data-ttu-id="8be5a-116">[in] La taille, en octets, de `pbKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="8be5a-116">[in] The size, in bytes, of `pbKeyBlob`.</span></span>  
  
 `ppbPublicKeyBlob`  
 <span data-ttu-id="8be5a-117">[out] La clé publique BLOB retournée.</span><span class="sxs-lookup"><span data-stu-id="8be5a-117">[out] The returned public key BLOB.</span></span> <span data-ttu-id="8be5a-118">Le `ppbPublicKeyBlob` paramètre est allouée par le common language runtime et retourné à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="8be5a-118">The `ppbPublicKeyBlob` parameter is allocated by the common language runtime and returned to the caller.</span></span> <span data-ttu-id="8be5a-119">L’appelant doit libérer la mémoire à l’aide de la [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="8be5a-119">The caller must free the memory by using the [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) method.</span></span>  
  
 `pcbPublicKeyBlob`  
 <span data-ttu-id="8be5a-120">[out] La taille de la clé publique retournée BLOB.</span><span class="sxs-lookup"><span data-stu-id="8be5a-120">[out] The size of the returned public key BLOB.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8be5a-121">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8be5a-121">Return Value</span></span>  
 <span data-ttu-id="8be5a-122">`S_OK` Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (consultez [valeurs HRESULT courantes](https://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).</span><span class="sxs-lookup"><span data-stu-id="8be5a-122">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8be5a-123">Notes</span><span class="sxs-lookup"><span data-stu-id="8be5a-123">Remarks</span></span>  
 <span data-ttu-id="8be5a-124">La clé publique est contenue dans un [PublicKeyBlob](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md) structure.</span><span class="sxs-lookup"><span data-stu-id="8be5a-124">The public key is contained in a [PublicKeyBlob](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md) structure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8be5a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8be5a-125">Requirements</span></span>  
 <span data-ttu-id="8be5a-126">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8be5a-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8be5a-127">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="8be5a-127">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="8be5a-128">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8be5a-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8be5a-129">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8be5a-129">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8be5a-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8be5a-130">See also</span></span>

- [<span data-ttu-id="8be5a-131">StrongNameTokenFromPublicKey, méthode</span><span class="sxs-lookup"><span data-stu-id="8be5a-131">StrongNameTokenFromPublicKey Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfrompublickey-method.md)
- [<span data-ttu-id="8be5a-132">PublicKeyBlob, structure</span><span class="sxs-lookup"><span data-stu-id="8be5a-132">PublicKeyBlob Structure</span></span>](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md)
- [<span data-ttu-id="8be5a-133">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="8be5a-133">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
