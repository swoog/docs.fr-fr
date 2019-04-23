---
title: COR_FIELD, structure
ms.date: 03/30/2017
api_name:
- COR_FIELD
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_FIELD
helpviewer_keywords:
- COR_FIELD structure [.NET Framework debugging]
ms.assetid: c0822423-a9df-4961-950d-50dcc152f863
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 691041632312bf8ac7c82a11724dcd725e14a420
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59231056"
---
# <a name="corfield-structure"></a><span data-ttu-id="2a898-102">COR_FIELD, structure</span><span class="sxs-lookup"><span data-stu-id="2a898-102">COR_FIELD Structure</span></span>
<span data-ttu-id="2a898-103">Fournit des informations sur un champ dans un objet.</span><span class="sxs-lookup"><span data-stu-id="2a898-103">Provides information about a field in an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2a898-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a898-104">Syntax</span></span>  
  
```  
typedef struct COR_FIELD{  
    mdFieldDef token;  
    ULONG32 offset;  
    COR_TYPEID id;  
    CorElementType fieldType;  
} COR_FIELD;  
```  
  
## <a name="members"></a><span data-ttu-id="2a898-105">Membres</span><span class="sxs-lookup"><span data-stu-id="2a898-105">Members</span></span>  
  
|<span data-ttu-id="2a898-106">Membre</span><span class="sxs-lookup"><span data-stu-id="2a898-106">Member</span></span>|<span data-ttu-id="2a898-107">Description</span><span class="sxs-lookup"><span data-stu-id="2a898-107">Description</span></span>|  
|------------|-----------------|  
|`token`|<span data-ttu-id="2a898-108">Un `mdFieldDef` jeton qui peut être utilisé pour obtenir des informations de champ.</span><span class="sxs-lookup"><span data-stu-id="2a898-108">An `mdFieldDef` token that can be used to get field information.</span></span>|  
|`offset`|<span data-ttu-id="2a898-109">Offset, en octets, pour les données de champ dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="2a898-109">The offset, in bytes, to the field data in the object.</span></span>|  
|`id`|<span data-ttu-id="2a898-110">Un [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) valeur qui identifie le type de ce champ.</span><span class="sxs-lookup"><span data-stu-id="2a898-110">A [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) value that identifies the type of this field.</span></span>|  
|`fieldType`|<span data-ttu-id="2a898-111">Une valeur d’énumération CorElementType qui indique le type du champ.</span><span class="sxs-lookup"><span data-stu-id="2a898-111">A CorElementType enumeration value that indicates the type of the field.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2a898-112">Notes</span><span class="sxs-lookup"><span data-stu-id="2a898-112">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2a898-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a898-113">Requirements</span></span>  
 <span data-ttu-id="2a898-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2a898-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2a898-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2a898-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2a898-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2a898-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2a898-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2a898-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2a898-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a898-118">See also</span></span>

- [<span data-ttu-id="2a898-119">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="2a898-119">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="2a898-120">Débogage</span><span class="sxs-lookup"><span data-stu-id="2a898-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
