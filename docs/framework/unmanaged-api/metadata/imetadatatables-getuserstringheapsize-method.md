---
title: IMetaDataTables::GetUserStringHeapSize, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetUserStringHeapSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetUserStringHeapSize
helpviewer_keywords:
- IMetaDataTables::GetUserStringHeapSize method [.NET Framework metadata]
- GetUserStringHeapSize method [.NET Framework metadata]
ms.assetid: cba9e4d6-9461-4420-9614-96ff7039ec9c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d35231e4c36639722635796891056a8902b95940
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59097458"
---
# <a name="imetadatatablesgetuserstringheapsize-method"></a><span data-ttu-id="55918-102">IMetaDataTables::GetUserStringHeapSize, méthode</span><span class="sxs-lookup"><span data-stu-id="55918-102">IMetaDataTables::GetUserStringHeapSize Method</span></span>
<span data-ttu-id="55918-103">Obtient la taille, en octets, du tas de chaîne utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55918-103">Gets the size, in bytes, of the user string heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="55918-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55918-104">Syntax</span></span>  
  
```  
HRESULT GetUserStringHeapSize (  
    [out] ULONG   *pcbBlobs  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="55918-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55918-105">Parameters</span></span>  
 `pcbBlobs`  
 <span data-ttu-id="55918-106">[out] Pointeur vers la taille, en octets, du tas de chaîne utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55918-106">[out] A pointer to the size, in bytes, of the user string heap.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="55918-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55918-107">Requirements</span></span>  
 <span data-ttu-id="55918-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="55918-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="55918-109">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="55918-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="55918-110">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="55918-110">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="55918-111">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="55918-111">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="55918-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55918-112">See also</span></span>

- [<span data-ttu-id="55918-113">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="55918-113">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)
- [<span data-ttu-id="55918-114">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="55918-114">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
