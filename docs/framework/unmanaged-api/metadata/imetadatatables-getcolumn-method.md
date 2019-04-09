---
title: IMetaDataTables::GetColumn, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetColumn
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetColumn
helpviewer_keywords:
- IMetaDataTables::GetColumn method [.NET Framework metadata]
- GetColumn method [.NET Framework metadata]
ms.assetid: 1032055b-cabb-45c5-a50e-7e853201b175
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 90ce56b3959c4768ef9cb6a9c551d53c5300a39e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59208356"
---
# <a name="imetadatatablesgetcolumn-method"></a><span data-ttu-id="8943a-102">IMetaDataTables::GetColumn, méthode</span><span class="sxs-lookup"><span data-stu-id="8943a-102">IMetaDataTables::GetColumn Method</span></span>
<span data-ttu-id="8943a-103">Obtient un pointeur vers la valeur contenue dans la cellule de la colonne spécifiée et la ligne dans la table donnée.</span><span class="sxs-lookup"><span data-stu-id="8943a-103">Gets a pointer to the value contained in the cell of the specified column and row in the given table.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8943a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8943a-104">Syntax</span></span>  
  
```  
HRESULT GetColumn (   
    [in]  ULONG   ixTbl,  
    [in]  ULONG   ixCol,  
    [in]  ULONG   rid,  
    [out] ULONG   *pVal  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8943a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8943a-105">Parameters</span></span>  
 `ixTbl`  
 <span data-ttu-id="8943a-106">[in] L’index de la table.</span><span class="sxs-lookup"><span data-stu-id="8943a-106">[in] The index of the table.</span></span>  
  
 `ixCol`  
 <span data-ttu-id="8943a-107">[in] L’index de la colonne dans la table.</span><span class="sxs-lookup"><span data-stu-id="8943a-107">[in] The index of the column in the table.</span></span>  
  
 `rid`  
 <span data-ttu-id="8943a-108">[in] L’index de la ligne dans la table.</span><span class="sxs-lookup"><span data-stu-id="8943a-108">[in] The index of the row in the table.</span></span>  
  
 `pVal`  
 <span data-ttu-id="8943a-109">[out] Pointeur vers la valeur dans la cellule.</span><span class="sxs-lookup"><span data-stu-id="8943a-109">[out] A pointer to the value in the cell.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8943a-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8943a-110">Requirements</span></span>  
 <span data-ttu-id="8943a-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8943a-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8943a-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="8943a-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8943a-113">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8943a-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="8943a-114">Versions du .NET framework</span><span class="sxs-lookup"><span data-stu-id="8943a-114">.NET Framework Versions</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="8943a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8943a-115">See also</span></span>

- [<span data-ttu-id="8943a-116">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="8943a-116">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)
- [<span data-ttu-id="8943a-117">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="8943a-117">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
