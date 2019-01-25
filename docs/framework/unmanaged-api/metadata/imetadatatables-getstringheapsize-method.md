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
ms.openlocfilehash: 7f6f16ebe57be0d09e97fe8aa95df892c2b02394
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54696254"
---
# <a name="imetadatatablesgetstringheapsize-method"></a><span data-ttu-id="20d57-102">IMetaDataTables::GetStringHeapSize, méthode</span><span class="sxs-lookup"><span data-stu-id="20d57-102">IMetaDataTables::GetStringHeapSize Method</span></span>
<span data-ttu-id="20d57-103">Obtient la taille, en octets, du tas de chaîne.</span><span class="sxs-lookup"><span data-stu-id="20d57-103">Gets the size, in bytes, of the string heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20d57-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20d57-104">Syntax</span></span>  
  
```  
HRESULT GetStringHeapSize (  
    [out] ULONG   *pcbStrings  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="20d57-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20d57-105">Parameters</span></span>  
 `pcbStrings`  
 <span data-ttu-id="20d57-106">[out] Pointeur vers la taille, en octets, du tas de chaîne.</span><span class="sxs-lookup"><span data-stu-id="20d57-106">[out] A pointer to the size, in bytes, of the string heap.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="20d57-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="20d57-107">Requirements</span></span>  
 <span data-ttu-id="20d57-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="20d57-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="20d57-109">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="20d57-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="20d57-110">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="20d57-110">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="20d57-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="20d57-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20d57-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20d57-112">See also</span></span>
- [<span data-ttu-id="20d57-113">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="20d57-113">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)
- [<span data-ttu-id="20d57-114">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="20d57-114">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
