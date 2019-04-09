---
title: IMetaDataTables::GetNextUserString, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetNextUserString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetNextUserString
helpviewer_keywords:
- GetNextUserString method [.NET Framework metadata]
- IMetaDataTables::GetNextUserString method [.NET Framework metadata]
ms.assetid: b7cb40ee-67b7-4f4e-8dcc-ee7ac8bc986b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3ce6cfd6a331c9d9695f65eb3a670305de38d010
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59191172"
---
# <a name="imetadatatablesgetnextuserstring-method"></a><span data-ttu-id="2dbff-102">IMetaDataTables::GetNextUserString, méthode</span><span class="sxs-lookup"><span data-stu-id="2dbff-102">IMetaDataTables::GetNextUserString Method</span></span>
<span data-ttu-id="2dbff-103">Obtient l’index de la ligne qui contient la chaîne codée en dur suivante dans la colonne de table actuelle.</span><span class="sxs-lookup"><span data-stu-id="2dbff-103">Gets the index of the row that contains the next hard-coded string in the current table column.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2dbff-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2dbff-104">Syntax</span></span>  
  
```  
HRESULT GetNextUserString (  
    [in]  ULONG   ixUserString,  
    [out] ULONG   *pNext  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2dbff-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2dbff-105">Parameters</span></span>  
 `ixUserString`  
 <span data-ttu-id="2dbff-106">[in] Une valeur d’index à partir de la colonne de chaîne actuelle.</span><span class="sxs-lookup"><span data-stu-id="2dbff-106">[in] An index value from the current string column.</span></span>  
  
 `pNext`  
 <span data-ttu-id="2dbff-107">[out] Pointeur vers l’index de ligne de la chaîne suivante dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="2dbff-107">[out] A pointer to the row index of the next string in the column.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2dbff-108">Notes</span><span class="sxs-lookup"><span data-stu-id="2dbff-108">Remarks</span></span>  
 <span data-ttu-id="2dbff-109">Nous déconseillons l’utilisation de cette méthode, car elle ne retourne pas de résultats cohérents.</span><span class="sxs-lookup"><span data-stu-id="2dbff-109">We do not recommend the use of this method, because it does not return consistent results.</span></span> <span data-ttu-id="2dbff-110">Pour plus d’informations sur le tableau GUID, consultez la documentation de Common Language Infrastructure (CLI), en particulier « Partition II : Metadata Definition and Semantics ».</span><span class="sxs-lookup"><span data-stu-id="2dbff-110">For information about the GUID table, see the Common Language Infrastructure (CLI) documentation, especially "Partition II: Metadata Definition and Semantics".</span></span> <span data-ttu-id="2dbff-111">La documentation est disponible en ligne. Consultez [ECMA C# and Common Language Infrastructure Standards](https://go.microsoft.com/fwlink/?LinkID=99212) sur MSDN et [Standard ECMA-335 - Common Language Infrastructure (CLI)](https://go.microsoft.com/fwlink/?LinkID=65552) sur le site web d’Ecma International.</span><span class="sxs-lookup"><span data-stu-id="2dbff-111">The documentation is available online; see [ECMA C# and Common Language Infrastructure Standards](https://go.microsoft.com/fwlink/?LinkID=99212) on MSDN and [Standard ECMA-335 - Common Language Infrastructure (CLI)](https://go.microsoft.com/fwlink/?LinkID=65552) on the Ecma International Web site.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2dbff-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2dbff-112">Requirements</span></span>  
 <span data-ttu-id="2dbff-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2dbff-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2dbff-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="2dbff-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="2dbff-115">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2dbff-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="2dbff-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="2dbff-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="2dbff-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2dbff-117">See also</span></span>

- [<span data-ttu-id="2dbff-118">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="2dbff-118">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)
- [<span data-ttu-id="2dbff-119">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="2dbff-119">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
