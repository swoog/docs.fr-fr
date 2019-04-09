---
title: StrongNameCompareAssemblies, fonction
ms.date: 03/30/2017
api_name:
- StrongNameCompareAssemblies
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameCompareAssemblies
helpviewer_keywords:
- StrongNameCompareAssemblies function [.NET Framework strong naming]
ms.assetid: 763f2375-efc6-4219-8806-a3b0567ef72b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2a49252d00f75b4d0b6325aeae0aab22f8ada5e4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59191378"
---
# <a name="strongnamecompareassemblies-function"></a><span data-ttu-id="dfd9f-102">StrongNameCompareAssemblies, fonction</span><span class="sxs-lookup"><span data-stu-id="dfd9f-102">StrongNameCompareAssemblies Function</span></span>
<span data-ttu-id="dfd9f-103">Détermine si deux assemblys diffèrent uniquement par leurs signatures avec nom fort.</span><span class="sxs-lookup"><span data-stu-id="dfd9f-103">Determines whether two assemblies differ only by their strong name signatures.</span></span>  
  
 <span data-ttu-id="dfd9f-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="dfd9f-104">This function has been deprecated.</span></span> <span data-ttu-id="dfd9f-105">Utilisez le [ICLRStrongName::StrongNameCompareAssemblies](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamecompareassemblies-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="dfd9f-105">Use the [ICLRStrongName::StrongNameCompareAssemblies](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamecompareassemblies-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dfd9f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfd9f-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameCompareAssemblies (  
    [in]  LPCWSTR   wszAssembly1,  
    [in]  LPCWSTR   wszAssembly2,  
    [out] DWORD     *pdwResult  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dfd9f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfd9f-107">Parameters</span></span>  
 `wszAssembly1`  
 <span data-ttu-id="dfd9f-108">[in] Le chemin d’accès à l’assembly en premier.</span><span class="sxs-lookup"><span data-stu-id="dfd9f-108">[in] The path to the first assembly.</span></span>  
  
 `wszAssembly2`  
 <span data-ttu-id="dfd9f-109">[in] Le chemin d’accès au deuxième assembly.</span><span class="sxs-lookup"><span data-stu-id="dfd9f-109">[in] The path to the second assembly.</span></span>  
  
 `pdwResult`  
 <span data-ttu-id="dfd9f-110">[out] Une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="dfd9f-110">[out] One of the following values:</span></span>  
  
-   `SN_CMP_DIFFERENT` <span data-ttu-id="dfd9f-111">(0) : Spécifie que les assemblys contiennent des données différentes.</span><span class="sxs-lookup"><span data-stu-id="dfd9f-111">(0) - Specifies that the assemblies contain different data.</span></span>  
  
-   `SN_CMP_IDENTICAL` <span data-ttu-id="dfd9f-112">(1) - Spécifie que les assemblys sont exactement identiques, y compris leurs signatures et la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="dfd9f-112">(1) - Specifies that the assemblies are exactly the same, including their signatures and checksum.</span></span>  
  
-   `SN_CMP_SIGONLY` <span data-ttu-id="dfd9f-113">(2) : Spécifie que les assemblys diffèrent uniquement par la signature et la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="dfd9f-113">(2) - Specifies that the assemblies differ only by signature and checksum.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="dfd9f-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="dfd9f-114">Return Value</span></span>  
 `true` <span data-ttu-id="dfd9f-115">de réussite ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="dfd9f-115">on successful completion; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dfd9f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfd9f-116">Requirements</span></span>  
 <span data-ttu-id="dfd9f-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dfd9f-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dfd9f-118">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="dfd9f-118">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="dfd9f-119">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="dfd9f-119">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="dfd9f-120">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="dfd9f-120">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="remarks"></a><span data-ttu-id="dfd9f-121">Notes</span><span class="sxs-lookup"><span data-stu-id="dfd9f-121">Remarks</span></span>  
 <span data-ttu-id="dfd9f-122">La signature de nom fort d’un assembly se compose du nom de texte, version, culture et jeton de clé publique de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="dfd9f-122">The strong name signature of an assembly consists of the assembly's text name, version, culture, and public key token.</span></span>  
  
 <span data-ttu-id="dfd9f-123">Si le `StrongNameCompareAssemblies` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.</span><span class="sxs-lookup"><span data-stu-id="dfd9f-123">If the `StrongNameCompareAssemblies` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dfd9f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfd9f-124">See also</span></span>

- [<span data-ttu-id="dfd9f-125">StrongNameCompareAssemblies, méthode</span><span class="sxs-lookup"><span data-stu-id="dfd9f-125">StrongNameCompareAssemblies Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamecompareassemblies-method.md)
- [<span data-ttu-id="dfd9f-126">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="dfd9f-126">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
