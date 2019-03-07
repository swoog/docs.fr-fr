---
title: IMetaDataTables::GetNextString, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetNextString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetNextString
helpviewer_keywords:
- IMetaDataTables::GetNextString method [.NET Framework metadata]
- GetNextString method [.NET Framework metadata]
ms.assetid: d9720428-c353-4f07-a7e8-899e106a1b37
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9b057b0537bbeff7433b776e64456ccc810cee54
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57473485"
---
# <a name="imetadatatablesgetnextstring-method"></a><span data-ttu-id="a9ccc-102">IMetaDataTables::GetNextString, méthode</span><span class="sxs-lookup"><span data-stu-id="a9ccc-102">IMetaDataTables::GetNextString Method</span></span>
<span data-ttu-id="a9ccc-103">Obtient l’index de la chaîne suivante dans la colonne de table actuelle.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-103">Gets the index of the next string in the current table column.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a9ccc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9ccc-104">Syntax</span></span>  
  
```  
HRESULT GetNextString (   
    [in]  ULONG   ixString,  
    [out] ULONG   *pNext  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a9ccc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9ccc-105">Parameters</span></span>  
 `ixString`  
 <span data-ttu-id="a9ccc-106">[in] La valeur d’index d’une colonne de table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-106">[in] The index value from a string table column.</span></span>  
  
 `pNext`  
 <span data-ttu-id="a9ccc-107">[out] Pointeur vers l’index de la chaîne suivante dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="a9ccc-107">[out] A pointer to the index of the next string in the column.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a9ccc-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a9ccc-108">Requirements</span></span>  
 <span data-ttu-id="a9ccc-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a9ccc-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a9ccc-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a9ccc-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a9ccc-111">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a9ccc-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a9ccc-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a9ccc-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9ccc-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9ccc-113">See also</span></span>
- [<span data-ttu-id="a9ccc-114">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="a9ccc-114">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)
- [<span data-ttu-id="a9ccc-115">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="a9ccc-115">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
