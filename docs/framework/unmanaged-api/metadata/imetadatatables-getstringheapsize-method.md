---
title: IMetaDataTables::GetStringHeapSize, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetStringHeapSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetStringHeapSize
helpviewer_keywords:
- IMetaDataTables::GetStringHeapSize method [.NET Framework metadata]
- GetStringHeapSize method [.NET Framework metadata]
ms.assetid: ed8f6335-81f5-4c09-81a9-2a909fc530c9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a46f7b277987df7e15eb2d534d1bbacc3250f4e1
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57466009"
---
# <a name="imetadatatablesgetstringheapsize-method"></a><span data-ttu-id="1e171-102">IMetaDataTables::GetStringHeapSize, méthode</span><span class="sxs-lookup"><span data-stu-id="1e171-102">IMetaDataTables::GetStringHeapSize Method</span></span>
<span data-ttu-id="1e171-103">Obtient la taille, en octets, du tas de chaîne.</span><span class="sxs-lookup"><span data-stu-id="1e171-103">Gets the size, in bytes, of the string heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1e171-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e171-104">Syntax</span></span>  
  
```  
HRESULT GetStringHeapSize (  
    [out] ULONG   *pcbStrings  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1e171-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e171-105">Parameters</span></span>  
 `pcbStrings`  
 <span data-ttu-id="1e171-106">[out] Pointeur vers la taille, en octets, du tas de chaîne.</span><span class="sxs-lookup"><span data-stu-id="1e171-106">[out] A pointer to the size, in bytes, of the string heap.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1e171-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1e171-107">Requirements</span></span>  
 <span data-ttu-id="1e171-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1e171-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1e171-109">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="1e171-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1e171-110">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1e171-110">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="1e171-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1e171-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1e171-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e171-112">See also</span></span>
- [<span data-ttu-id="1e171-113">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="1e171-113">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)
- [<span data-ttu-id="1e171-114">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="1e171-114">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
