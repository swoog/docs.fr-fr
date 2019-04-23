---
title: COR_FIELD_OFFSET, structure
ms.date: 03/30/2017
api_name:
- COR_FIELD_OFFSET
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_FIELD_OFFSET
helpviewer_keywords:
- COR_FIELD_OFFSET structure [.NET Framework metadata]
ms.assetid: cced5298-277f-4a5a-8ecf-a0050c1096ea
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 820c99de1bdb108a24203a3438b1709ca54490b7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59078120"
---
# <a name="corfieldoffset-structure"></a><span data-ttu-id="3d719-102">COR_FIELD_OFFSET, structure</span><span class="sxs-lookup"><span data-stu-id="3d719-102">COR_FIELD_OFFSET Structure</span></span>
<span data-ttu-id="3d719-103">Stocke l'offset, dans une classe, du champ spécifié.</span><span class="sxs-lookup"><span data-stu-id="3d719-103">Stores the offset, within a class, of the specified field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3d719-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d719-104">Syntax</span></span>  
  
```  
typedef struct COR_FIELD_OFFSET {  
    mdFieldDef  ridOfField;  
    ULONG       ulOffset;  
} COR_FIELD_OFFSET;  
```  
  
## <a name="members"></a><span data-ttu-id="3d719-105">Membres</span><span class="sxs-lookup"><span data-stu-id="3d719-105">Members</span></span>  
  
|<span data-ttu-id="3d719-106">Membre</span><span class="sxs-lookup"><span data-stu-id="3d719-106">Member</span></span>|<span data-ttu-id="3d719-107">Description</span><span class="sxs-lookup"><span data-stu-id="3d719-107">Description</span></span>|  
|------------|-----------------|  
|`ridOfField`|<span data-ttu-id="3d719-108">Un `mdFieldDef` jeton de métadonnées qui représente le champ.</span><span class="sxs-lookup"><span data-stu-id="3d719-108">An `mdFieldDef` metadata token that represents the field.</span></span>|  
|`ulOffset`|<span data-ttu-id="3d719-109">Offset du champ dans sa classe.</span><span class="sxs-lookup"><span data-stu-id="3d719-109">The field's offset within its class.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3d719-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3d719-110">Remarks</span></span>  
 <span data-ttu-id="3d719-111">[IMetaDataImport::GetClassLayout](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-getclasslayout-method.md) et [IMetaDataEmit::SetClassLayout](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setclasslayout-method.md) méthodes prennent un paramètre de type `COR_FIELD_OFFSET`.</span><span class="sxs-lookup"><span data-stu-id="3d719-111">[IMetaDataImport::GetClassLayout](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-getclasslayout-method.md) and [IMetaDataEmit::SetClassLayout](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setclasslayout-method.md) methods take a parameter of type `COR_FIELD_OFFSET`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3d719-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d719-112">Requirements</span></span>  
 <span data-ttu-id="3d719-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3d719-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3d719-114">**En-tête :** CorHdr.h, CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="3d719-114">**Header:** CorHdr.h, CorProf.idl</span></span>  
  
 <span data-ttu-id="3d719-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3d719-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3d719-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d719-116">See also</span></span>

- [<span data-ttu-id="3d719-117">Structures de métadonnées</span><span class="sxs-lookup"><span data-stu-id="3d719-117">Metadata Structures</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-structures.md)
- [<span data-ttu-id="3d719-118">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="3d719-118">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="3d719-119">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="3d719-119">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
