---
title: StrongNameFreeBuffer, fonction
ms.date: 03/30/2017
api_name:
- StrongNameFreeBuffer
api_location:
- mscoree.dll
- mscorsn.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameFreeBuffer
helpviewer_keywords:
- StrongNameFreeBuffer function [.NET Framework strong naming]
ms.assetid: eda21ecf-4734-4f92-aaba-9f34884385db
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1a129608370cd72967e0c441eff12b4aca7e638c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33455086"
---
# <a name="strongnamefreebuffer-function"></a><span data-ttu-id="682a8-102">StrongNameFreeBuffer, fonction</span><span class="sxs-lookup"><span data-stu-id="682a8-102">StrongNameFreeBuffer Function</span></span>
<span data-ttu-id="682a8-103">Libère la mémoire qui a été allouée avec un appel précédent à une fonction de nom fort, tel que [StrongNameGetPublicKey](../../../../docs/framework/unmanaged-api/strong-naming/strongnamegetpublickey-function.md), [StrongNameTokenFromPublicKey](../../../../docs/framework/unmanaged-api/strong-naming/strongnametokenfrompublickey-function.md), ou [StrongNameSignatureGeneration ](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignaturegeneration-function.md).</span><span class="sxs-lookup"><span data-stu-id="682a8-103">Frees memory that was allocated with a previous call to a strong name function such as [StrongNameGetPublicKey](../../../../docs/framework/unmanaged-api/strong-naming/strongnamegetpublickey-function.md), [StrongNameTokenFromPublicKey](../../../../docs/framework/unmanaged-api/strong-naming/strongnametokenfrompublickey-function.md), or [StrongNameSignatureGeneration](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignaturegeneration-function.md).</span></span>  
  
 <span data-ttu-id="682a8-104">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="682a8-104">This function has been deprecated.</span></span> <span data-ttu-id="682a8-105">Utilisez le [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="682a8-105">Use the [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="682a8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="682a8-106">Syntax</span></span>  
  
```  
VOID StrongNameFreeBuffer (   
   [in] BYTE   *pbMemory  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="682a8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="682a8-107">Parameters</span></span>  
 `pbMemory`  
 <span data-ttu-id="682a8-108">[in] Pointeur vers la mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="682a8-108">[in] A pointer to the memory to free.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="682a8-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="682a8-109">Requirements</span></span>  
 <span data-ttu-id="682a8-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="682a8-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="682a8-111">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="682a8-111">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="682a8-112">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="682a8-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="682a8-113">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="682a8-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="682a8-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="682a8-114">See Also</span></span>  
 [<span data-ttu-id="682a8-115">StrongNameFreeBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="682a8-115">StrongNameFreeBuffer Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md)  
 [<span data-ttu-id="682a8-116">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="682a8-116">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
