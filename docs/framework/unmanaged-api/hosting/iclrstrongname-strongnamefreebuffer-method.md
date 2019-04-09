---
title: Méthode ICLRStrongName::StrongNameFreeBuffer
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameFreeBuffer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameFreeBuffer
helpviewer_keywords:
- StrongNameFreeBuffer method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameFreeBuffer method [.NET Framework hosting]
ms.assetid: 6148c508-bd1d-4a37-85c3-06ecb09cc857
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8e42f13d3d3ac0154cd1f8bbe9785e1e4ae16379
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59127560"
---
# <a name="iclrstrongnamestrongnamefreebuffer-method"></a><span data-ttu-id="ff434-102">Méthode ICLRStrongName::StrongNameFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ff434-102">ICLRStrongName::StrongNameFreeBuffer Method</span></span>
<span data-ttu-id="ff434-103">Libère la mémoire qui a été alloué avec un appel précédent à une méthode de nom fort comme [ICLRStrongName::StrongNameGetPublicKey](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetpublickey-method.md), [ICLRStrongName::StrongNameTokenFromPublicKey](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfrompublickey-method.md), ou [ ICLRStrongName::StrongNameSignatureGeneration](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignaturegeneration-method.md).</span><span class="sxs-lookup"><span data-stu-id="ff434-103">Frees memory that was allocated with a previous call to a strong name method such as [ICLRStrongName::StrongNameGetPublicKey](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetpublickey-method.md), [ICLRStrongName::StrongNameTokenFromPublicKey](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfrompublickey-method.md), or [ICLRStrongName::StrongNameSignatureGeneration](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignaturegeneration-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ff434-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff434-104">Syntax</span></span>  
  
```  
HRESULT StrongNameFreeBuffer (   
   [in] BYTE   *pbMemory  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ff434-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff434-105">Parameters</span></span>  
 `pbMemory`  
 <span data-ttu-id="ff434-106">[in] Pointeur vers la mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="ff434-106">[in] A pointer to the memory to free.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ff434-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ff434-107">Return Value</span></span>  
 `S_OK` <span data-ttu-id="ff434-108">Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (consultez [valeurs HRESULT courantes](https://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).</span><span class="sxs-lookup"><span data-stu-id="ff434-108">if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ff434-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff434-109">Requirements</span></span>  
 <span data-ttu-id="ff434-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ff434-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ff434-111">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="ff434-111">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="ff434-112">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ff434-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="ff434-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="ff434-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="ff434-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff434-114">See also</span></span>

- [<span data-ttu-id="ff434-115">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="ff434-115">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
