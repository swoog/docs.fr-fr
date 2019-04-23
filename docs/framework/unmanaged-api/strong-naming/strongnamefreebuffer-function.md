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
ms.openlocfilehash: 9bfc6491a1d18c81a44a7d9c5084f744c9b76281
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59072571"
---
# <a name="strongnamefreebuffer-function"></a><span data-ttu-id="2bd28-102">StrongNameFreeBuffer, fonction</span><span class="sxs-lookup"><span data-stu-id="2bd28-102">StrongNameFreeBuffer Function</span></span>
<span data-ttu-id="2bd28-103">Libère la mémoire qui a été alloué avec un appel précédent à une fonction de nom fort comme [StrongNameGetPublicKey](../../../../docs/framework/unmanaged-api/strong-naming/strongnamegetpublickey-function.md), [StrongNameTokenFromPublicKey](../../../../docs/framework/unmanaged-api/strong-naming/strongnametokenfrompublickey-function.md) ou [StrongNameSignatureGeneration ](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignaturegeneration-function.md).</span><span class="sxs-lookup"><span data-stu-id="2bd28-103">Frees memory that was allocated with a previous call to a strong name function such as [StrongNameGetPublicKey](../../../../docs/framework/unmanaged-api/strong-naming/strongnamegetpublickey-function.md), [StrongNameTokenFromPublicKey](../../../../docs/framework/unmanaged-api/strong-naming/strongnametokenfrompublickey-function.md), or [StrongNameSignatureGeneration](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignaturegeneration-function.md).</span></span>  
  
 <span data-ttu-id="2bd28-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="2bd28-104">This function has been deprecated.</span></span> <span data-ttu-id="2bd28-105">Utilisez le [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="2bd28-105">Use the [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2bd28-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2bd28-106">Syntax</span></span>  
  
```  
VOID StrongNameFreeBuffer (   
   [in] BYTE   *pbMemory  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2bd28-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2bd28-107">Parameters</span></span>  
 `pbMemory`  
 <span data-ttu-id="2bd28-108">[in] Pointeur vers la mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="2bd28-108">[in] A pointer to the memory to free.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2bd28-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bd28-109">Requirements</span></span>  
 <span data-ttu-id="2bd28-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2bd28-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2bd28-111">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="2bd28-111">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="2bd28-112">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2bd28-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="2bd28-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2bd28-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2bd28-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bd28-114">See also</span></span>

- [<span data-ttu-id="2bd28-115">StrongNameFreeBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="2bd28-115">StrongNameFreeBuffer Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md)
- [<span data-ttu-id="2bd28-116">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="2bd28-116">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
