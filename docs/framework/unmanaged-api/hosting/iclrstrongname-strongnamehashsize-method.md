---
title: Méthode ICLRStrongName::StrongNameHashSize
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameHashSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameHashSize
helpviewer_keywords:
- ICLRStrongName::StrongNameHashSize method [.NET Framework hosting]
- StrongNameHashSize method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 4a05ee56-08e4-4f3a-86a9-9b52083d5c0f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 91b84a980e8a670b8e8b2970cfc96ddd6f4c33b5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59218483"
---
# <a name="iclrstrongnamestrongnamehashsize-method"></a><span data-ttu-id="5ed3c-102">Méthode ICLRStrongName::StrongNameHashSize</span><span class="sxs-lookup"><span data-stu-id="5ed3c-102">ICLRStrongName::StrongNameHashSize Method</span></span>
<span data-ttu-id="5ed3c-103">Obtient la taille de mémoire tampon requise pour un hachage, à l’aide de l’algorithme de hachage spécifié.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-103">Gets the buffer size required for a hash, using the specified hash algorithm.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5ed3c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ed3c-104">Syntax</span></span>  
  
```  
HRESULT StrongNameHashSize (  
    [in]  ULONG   ulHashAlg,  
    [out] DWORD   *pcbSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5ed3c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ed3c-105">Parameters</span></span>  
 `ulHashAlg`  
 <span data-ttu-id="5ed3c-106">[in] L’algorithme de hachage utilisé pour calculer la taille du tampon.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-106">[in] The hash algorithm used to compute the buffer size.</span></span>  
  
 `pcbSize`  
 <span data-ttu-id="5ed3c-107">[out] La taille de la mémoire tampon retournée, en octets.</span><span class="sxs-lookup"><span data-stu-id="5ed3c-107">[out] The returned buffer size, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5ed3c-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5ed3c-108">Return Value</span></span>  
 `S_OK` <span data-ttu-id="5ed3c-109">Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (consultez [valeurs HRESULT courantes](https://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).</span><span class="sxs-lookup"><span data-stu-id="5ed3c-109">if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5ed3c-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ed3c-110">Requirements</span></span>  
 <span data-ttu-id="5ed3c-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5ed3c-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5ed3c-112">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="5ed3c-112">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="5ed3c-113">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5ed3c-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="5ed3c-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="5ed3c-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="5ed3c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ed3c-115">See also</span></span>

- [<span data-ttu-id="5ed3c-116">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="5ed3c-116">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
