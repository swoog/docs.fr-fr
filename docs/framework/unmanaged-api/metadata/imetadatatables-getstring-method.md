---
title: IMetaDataTables::GetString, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetString
helpviewer_keywords:
- IMetaDataTables::GetString method [.NET Framework metadata]
- GetString method, IMetaDataTables interface [.NET Framework metadata]
ms.assetid: 895c35cf-b95d-4e3b-93b5-cfc1cf9044fc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8fed98521c0609ebd8b5f65885d69c77814e9e85
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59119338"
---
# <a name="imetadatatablesgetstring-method"></a><span data-ttu-id="fa2e9-102">IMetaDataTables::GetString, méthode</span><span class="sxs-lookup"><span data-stu-id="fa2e9-102">IMetaDataTables::GetString Method</span></span>
<span data-ttu-id="fa2e9-103">Obtient la chaîne à l’index spécifié à partir de la colonne de table dans l’étendue actuelle de la référence.</span><span class="sxs-lookup"><span data-stu-id="fa2e9-103">Gets the string at the specified index from the table column in the current reference scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa2e9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa2e9-104">Syntax</span></span>  
  
```  
HRESULT GetString (   
    [in]  ULONG       ixString,  
    [out] const char  **ppString  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fa2e9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa2e9-105">Parameters</span></span>  
 `ixString`  
 <span data-ttu-id="fa2e9-106">[in] Index auquel commencer à rechercher la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="fa2e9-106">[in] The index at which to start to search for the next value.</span></span>  
  
 `ppString`  
 <span data-ttu-id="fa2e9-107">[out] Pointeur vers un pointeur vers la valeur de la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="fa2e9-107">[out] A pointer to a pointer to the returned string value.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fa2e9-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa2e9-108">Requirements</span></span>  
 <span data-ttu-id="fa2e9-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fa2e9-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fa2e9-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="fa2e9-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="fa2e9-111">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fa2e9-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="fa2e9-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="fa2e9-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="fa2e9-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa2e9-113">See also</span></span>

- [<span data-ttu-id="fa2e9-114">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="fa2e9-114">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)
- [<span data-ttu-id="fa2e9-115">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="fa2e9-115">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
