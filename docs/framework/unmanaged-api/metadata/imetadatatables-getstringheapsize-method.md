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
ms.openlocfilehash: 1d814a741bc88bb50bfe9ddc3db57635a7266a82
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33449918"
---
# <a name="imetadatatablesgetstringheapsize-method"></a><span data-ttu-id="1298e-102">IMetaDataTables::GetStringHeapSize, méthode</span><span class="sxs-lookup"><span data-stu-id="1298e-102">IMetaDataTables::GetStringHeapSize Method</span></span>
<span data-ttu-id="1298e-103">Obtient la taille, en octets, du tas de chaîne.</span><span class="sxs-lookup"><span data-stu-id="1298e-103">Gets the size, in bytes, of the string heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1298e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1298e-104">Syntax</span></span>  
  
```  
HRESULT GetStringHeapSize (  
    [out] ULONG   *pcbStrings  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1298e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1298e-105">Parameters</span></span>  
 `pcbStrings`  
 <span data-ttu-id="1298e-106">[out] Pointeur vers la taille, en octets, du tas de chaîne.</span><span class="sxs-lookup"><span data-stu-id="1298e-106">[out] A pointer to the size, in bytes, of the string heap.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1298e-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1298e-107">Requirements</span></span>  
 <span data-ttu-id="1298e-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1298e-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1298e-109">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="1298e-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1298e-110">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1298e-110">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="1298e-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1298e-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1298e-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1298e-112">See Also</span></span>  
 [<span data-ttu-id="1298e-113">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="1298e-113">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)  
 [<span data-ttu-id="1298e-114">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="1298e-114">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
