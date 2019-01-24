---
title: StrongNameKeyInstall, fonction
ms.date: 03/30/2017
api_name:
- StrongNameKeyInstall
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameKeyInstall
helpviewer_keywords:
- StrongNameKeyInstall function [.NET Framework strong naming]
ms.assetid: e32fd546-7757-4681-be3d-658e93281e50
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ecd52fce8033876f0599fa0ba25fae0850c0e01f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54508484"
---
# <a name="strongnamekeyinstall-function"></a><span data-ttu-id="b9a96-102">StrongNameKeyInstall, fonction</span><span class="sxs-lookup"><span data-stu-id="b9a96-102">StrongNameKeyInstall Function</span></span>
<span data-ttu-id="b9a96-103">Importe une paire de clés publique/privée dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="b9a96-103">Imports a public/private key pair into a container.</span></span>  
  
 <span data-ttu-id="b9a96-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b9a96-104">This function has been deprecated.</span></span> <span data-ttu-id="b9a96-105">Utilisez le [ICLRStrongName::StrongNameKeyInstall](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeyinstall-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="b9a96-105">Use the [ICLRStrongName::StrongNameKeyInstall](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeyinstall-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b9a96-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9a96-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameKeyInstall (  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b9a96-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9a96-107">Parameters</span></span>  
 `wszKeyContainer`  
 <span data-ttu-id="b9a96-108">[in] Le nom du conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="b9a96-108">[in] The name of the key container.</span></span> <span data-ttu-id="b9a96-109">`wszKeyContainer` doit être une chaîne non vide.</span><span class="sxs-lookup"><span data-stu-id="b9a96-109">`wszKeyContainer` must be a non-empty string.</span></span>  
  
 `pbKeyBlob`  
 <span data-ttu-id="b9a96-110">[in] La paire de clés binaire.</span><span class="sxs-lookup"><span data-stu-id="b9a96-110">[in] The binary key pair.</span></span>  
  
 `cbKeyBlob`  
 <span data-ttu-id="b9a96-111">[in] La taille, en octets, de `pbKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="b9a96-111">[in] The size, in bytes, of `pbKeyBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b9a96-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b9a96-112">Return Value</span></span>  
 <span data-ttu-id="b9a96-113">`true` de réussite ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="b9a96-113">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b9a96-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b9a96-114">Remarks</span></span>  
 <span data-ttu-id="b9a96-115">Utilisez le [StrongNameKeyDelete](../../../../docs/framework/unmanaged-api/strong-naming/strongnamekeydelete-function.md) (fonction) pour supprimer le conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="b9a96-115">Use the [StrongNameKeyDelete](../../../../docs/framework/unmanaged-api/strong-naming/strongnamekeydelete-function.md) function to delete the key container.</span></span>  
  
 <span data-ttu-id="b9a96-116">Si le `StrongNameKeyInstall` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.</span><span class="sxs-lookup"><span data-stu-id="b9a96-116">If the `StrongNameKeyInstall` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b9a96-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b9a96-117">Requirements</span></span>  
 <span data-ttu-id="b9a96-118">**Plateformes :** WindSee [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b9a96-118">**Platforms:** WindSee [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b9a96-119">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="b9a96-119">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="b9a96-120">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b9a96-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b9a96-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b9a96-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b9a96-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9a96-122">See also</span></span>
- [<span data-ttu-id="b9a96-123">StrongNameKeyInstall, méthode</span><span class="sxs-lookup"><span data-stu-id="b9a96-123">StrongNameKeyInstall Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeyinstall-method.md)
- [<span data-ttu-id="b9a96-124">StrongNameKeyDelete, méthode</span><span class="sxs-lookup"><span data-stu-id="b9a96-124">StrongNameKeyDelete Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeydelete-method.md)
- [<span data-ttu-id="b9a96-125">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="b9a96-125">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
