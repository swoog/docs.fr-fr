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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59231056"
---
# <a name="corfield-structure"></a><span data-ttu-id="137b5-102">COR_FIELD, structure</span><span class="sxs-lookup"><span data-stu-id="137b5-102">COR_FIELD Structure</span></span>
<span data-ttu-id="137b5-103">Fournit des informations sur un champ dans un objet.</span><span class="sxs-lookup"><span data-stu-id="137b5-103">Provides information about a field in an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="137b5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="137b5-104">Syntax</span></span>  
  
```  
typedef struct COR_FIELD{  
    mdFieldDef token;  
    ULONG32 offset;  
    COR_TYPEID id;  
    CorElementType fieldType;  
} COR_FIELD;  
```  
  
## <a name="members"></a><span data-ttu-id="137b5-105">Membres</span><span class="sxs-lookup"><span data-stu-id="137b5-105">Members</span></span>  
  
|<span data-ttu-id="137b5-106">Membre</span><span class="sxs-lookup"><span data-stu-id="137b5-106">Member</span></span>|<span data-ttu-id="137b5-107">Description</span><span class="sxs-lookup"><span data-stu-id="137b5-107">Description</span></span>|  
|------------|-----------------|  
|`token`|<span data-ttu-id="137b5-108">Un `mdFieldDef` jeton qui peut être utilisé pour obtenir des informations de champ.</span><span class="sxs-lookup"><span data-stu-id="137b5-108">An `mdFieldDef` token that can be used to get field information.</span></span>|  
|`offset`|<span data-ttu-id="137b5-109">Offset, en octets, pour les données de champ dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="137b5-109">The offset, in bytes, to the field data in the object.</span></span>|  
|`id`|<span data-ttu-id="137b5-110">Un [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) valeur qui identifie le type de ce champ.</span><span class="sxs-lookup"><span data-stu-id="137b5-110">A [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) value that identifies the type of this field.</span></span>|  
|`fieldType`|<span data-ttu-id="137b5-111">Une valeur d’énumération CorElementType qui indique le type du champ.</span><span class="sxs-lookup"><span data-stu-id="137b5-111">A CorElementType enumeration value that indicates the type of the field.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="137b5-112">Notes</span><span class="sxs-lookup"><span data-stu-id="137b5-112">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="137b5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="137b5-113">Requirements</span></span>  
 <span data-ttu-id="137b5-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="137b5-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="137b5-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="137b5-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="137b5-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="137b5-116">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="137b5-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="137b5-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="137b5-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="137b5-118">See also</span></span>

- [<span data-ttu-id="137b5-119">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="137b5-119">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="137b5-120">Débogage</span><span class="sxs-lookup"><span data-stu-id="137b5-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
