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
ms.openlocfilehash: 64634f961064feb3d2db11d421fea920f1e2d16b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54669053"
---
# <a name="imetadatatablesgetuserstringheapsize-method"></a><span data-ttu-id="d85e8-102">IMetaDataTables::GetUserStringHeapSize, méthode</span><span class="sxs-lookup"><span data-stu-id="d85e8-102">IMetaDataTables::GetUserStringHeapSize Method</span></span>
<span data-ttu-id="d85e8-103">Obtient la taille, en octets, du tas de chaîne utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d85e8-103">Gets the size, in bytes, of the user string heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d85e8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d85e8-104">Syntax</span></span>  
  
```  
HRESULT GetUserStringHeapSize (  
    [out] ULONG   *pcbBlobs  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d85e8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d85e8-105">Parameters</span></span>  
 `pcbBlobs`  
 <span data-ttu-id="d85e8-106">[out] Pointeur vers la taille, en octets, du tas de chaîne utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d85e8-106">[out] A pointer to the size, in bytes, of the user string heap.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d85e8-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d85e8-107">Requirements</span></span>  
 <span data-ttu-id="d85e8-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d85e8-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d85e8-109">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="d85e8-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d85e8-110">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d85e8-110">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d85e8-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d85e8-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d85e8-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d85e8-112">See also</span></span>
- [<span data-ttu-id="d85e8-113">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="d85e8-113">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)
- [<span data-ttu-id="d85e8-114">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="d85e8-114">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
