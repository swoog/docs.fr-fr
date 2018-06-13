---
title: ICLRStrongName2, interface
ms.date: 03/30/2017
api_name:
- ICLRStrongName2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName2
helpviewer_keywords:
- ICLRStrongName2 interface [.NET Framework hosting]
ms.assetid: 9f098a74-201e-4628-a468-8dee9ab99b4a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6bf9e3d2df8f507e118b393007c3958358a830cc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33432971"
---
# <a name="iclrstrongname2-interface"></a><span data-ttu-id="f6d69-102">ICLRStrongName2, interface</span><span class="sxs-lookup"><span data-stu-id="f6d69-102">ICLRStrongName2 Interface</span></span>
<span data-ttu-id="f6d69-103">Fournit la possibilité de créer des noms forts dans le groupe de SHA-2 d’algorithmes de hachage sécurisé (SHA-256, SHA-384 et SHA-512).</span><span class="sxs-lookup"><span data-stu-id="f6d69-103">Provides the ability to create strong names using the SHA-2 group of Secure Hash Algorithms (SHA-256, SHA-384, and SHA-512).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f6d69-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f6d69-104">Methods</span></span>  
  
|<span data-ttu-id="f6d69-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="f6d69-105">Method</span></span>|<span data-ttu-id="f6d69-106">Description</span><span class="sxs-lookup"><span data-stu-id="f6d69-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f6d69-107">StrongNameGetPublicKeyEx, méthode</span><span class="sxs-lookup"><span data-stu-id="f6d69-107">StrongNameGetPublicKeyEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/strongnamegetpublickeyex-method.md)|<span data-ttu-id="f6d69-108">Obtient la clé publique à partir d’une paire de clés publique/privée et spécifie un algorithme de hachage et un algorithme de signature.</span><span class="sxs-lookup"><span data-stu-id="f6d69-108">Gets the public key from a public/private key pair, and specifies a hash algorithm and a signature algorithm.</span></span>|  
|[<span data-ttu-id="f6d69-109">StrongNameSignatureVerificationEx2, méthode</span><span class="sxs-lookup"><span data-stu-id="f6d69-109">StrongNameSignatureVerificationEx2 Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/strongnamesignatureverificationex2-method.md)|<span data-ttu-id="f6d69-110">Vérifie la signature d’un assembly portant un nom fort et fournit un mappage à partir de la clé ECMA à une clé réelle.</span><span class="sxs-lookup"><span data-stu-id="f6d69-110">Verifies the signature of a strongly named assembly, and provides a mapping from the ECMA key to a real key.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f6d69-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f6d69-111">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f6d69-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f6d69-112">Requirements</span></span>  
 <span data-ttu-id="f6d69-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f6d69-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f6d69-114">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="f6d69-114">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="f6d69-115">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f6d69-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f6d69-116">**Versions du .NET framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f6d69-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>
