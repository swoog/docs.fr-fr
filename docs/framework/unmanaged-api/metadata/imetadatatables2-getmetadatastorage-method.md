---
title: IMetaDataTables2::GetMetaDataStorage, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables2.GetMetaDataStorage
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables2::GetMetaDataStorage
helpviewer_keywords:
- GetMetaDataStorage method [.NET Framework metadata]
- IMetaDataTables2::GetMetaDataStorage method [.NET Framework metadata]
ms.assetid: 667a6d1e-753d-4ea2-8fd8-a8337d1bb9cd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 33064fe8292eb7a8079d2f68bcdea767d306be6f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33452317"
---
# <a name="imetadatatables2getmetadatastorage-method"></a><span data-ttu-id="e6756-102">IMetaDataTables2::GetMetaDataStorage, méthode</span><span class="sxs-lookup"><span data-stu-id="e6756-102">IMetaDataTables2::GetMetaDataStorage Method</span></span>
<span data-ttu-id="e6756-103">Obtient la taille et le contenu des métadonnées stockées dans la section spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e6756-103">Gets the size and contents of the metadata stored in the specified section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e6756-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6756-104">Syntax</span></span>  
  
```  
HRESULT GetMetaDataStorage (  
   [in, out] const void   **ppvMd,  
   [out] ULONG   *pcbMd  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e6756-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6756-105">Parameters</span></span>  
 `ppvMd`  
 <span data-ttu-id="e6756-106">[dans, out] Pointeur vers une section de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="e6756-106">[in, out] A pointer to a metadata section.</span></span>  
  
 `pcbMd`  
 <span data-ttu-id="e6756-107">[out] La taille du flux de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="e6756-107">[out] The size of the metadata stream.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e6756-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e6756-108">Requirements</span></span>  
 <span data-ttu-id="e6756-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e6756-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e6756-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e6756-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e6756-111">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e6756-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e6756-112">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e6756-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e6756-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6756-113">See Also</span></span>  
 [<span data-ttu-id="e6756-114">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="e6756-114">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)  
 [<span data-ttu-id="e6756-115">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="e6756-115">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)
