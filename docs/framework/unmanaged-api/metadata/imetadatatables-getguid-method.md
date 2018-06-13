---
title: IMetaDataTables::GetGuid, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetGuid
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetGuid
helpviewer_keywords:
- GetGuid method [.NET Framework metadata]
- IMetaDataTables::GetGuid method [.NET Framework metadata]
ms.assetid: a3546316-e24d-417f-9909-e45d42c9d471
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 97f1bbd8ff04ccfbfe93fd5b75fc89fc28f393d0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33449106"
---
# <a name="imetadatatablesgetguid-method"></a><span data-ttu-id="41f5c-102">IMetaDataTables::GetGuid, méthode</span><span class="sxs-lookup"><span data-stu-id="41f5c-102">IMetaDataTables::GetGuid Method</span></span>
<span data-ttu-id="41f5c-103">Obtient un GUID à partir de la ligne à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="41f5c-103">Gets a GUID from the row at the specified index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="41f5c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41f5c-104">Syntax</span></span>  
  
```  
HRESULT GetGuid (   
    [in]  ULONG       ixGuid,  
    [out] const GUID  **ppGUID  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="41f5c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41f5c-105">Parameters</span></span>  
 `ixGuid`  
 <span data-ttu-id="41f5c-106">[in] L’index de la ligne à partir de laquelle obtenir le GUID.</span><span class="sxs-lookup"><span data-stu-id="41f5c-106">[in] The index of the row from which to get the GUID.</span></span>  
  
 `ppGuid`  
 <span data-ttu-id="41f5c-107">[out] Pointeur vers un pointeur vers le GUID.</span><span class="sxs-lookup"><span data-stu-id="41f5c-107">[out] A pointer to a pointer to the GUID.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="41f5c-108">Notes</span><span class="sxs-lookup"><span data-stu-id="41f5c-108">Remarks</span></span>  
 <span data-ttu-id="41f5c-109">Nous déconseillons l’utilisation de cette méthode, car elle ne retourne pas de résultats cohérents.</span><span class="sxs-lookup"><span data-stu-id="41f5c-109">We do not recommend the use of this method, because it does not return consistent results.</span></span> <span data-ttu-id="41f5c-110">Pour plus d’informations sur la table GUID, consultez la documentation du Common Language Infrastructure (CLI), en particulier « Partition II : Metadata Definition et Semantics ».</span><span class="sxs-lookup"><span data-stu-id="41f5c-110">For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics".</span></span> <span data-ttu-id="41f5c-111">La documentation est disponible en ligne. Consultez [ECMA C# and Common Language Infrastructure Standards](http://go.microsoft.com/fwlink/?LinkID=99212) sur MSDN et [Standard ECMA-335 - Common Language Infrastructure (CLI)](http://go.microsoft.com/fwlink/?LinkID=65552) sur le site web d’Ecma International.</span><span class="sxs-lookup"><span data-stu-id="41f5c-111">The documentation is available online; see [ECMA C# and Common Language Infrastructure Standards](http://go.microsoft.com/fwlink/?LinkID=99212) on MSDN and [Standard ECMA-335 - Common Language Infrastructure (CLI)](http://go.microsoft.com/fwlink/?LinkID=65552) on the Ecma International Web site.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="41f5c-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="41f5c-112">Requirements</span></span>  
 <span data-ttu-id="41f5c-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="41f5c-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="41f5c-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="41f5c-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="41f5c-115">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="41f5c-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="41f5c-116">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="41f5c-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="41f5c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41f5c-117">See Also</span></span>  
 [<span data-ttu-id="41f5c-118">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="41f5c-118">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)  
 [<span data-ttu-id="41f5c-119">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="41f5c-119">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
