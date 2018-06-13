---
title: CorDebugGuidToTypeMapping, structure
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- CorDebugGuidToTypeMapping
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugGuidToTypeMapping
helpviewer_keywords:
- CorDebugGuidToTypeMapping structure [.NET Framework debugging]
ms.assetid: 57dbccd9-b16d-4da3-ae25-7a2cf9adf679
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c803a805da605bd52fd50eb1e292c0e277143d7a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33405257"
---
# <a name="cordebugguidtotypemapping-structure"></a><span data-ttu-id="93e72-102">CorDebugGuidToTypeMapping, structure</span><span class="sxs-lookup"><span data-stu-id="93e72-102">CorDebugGuidToTypeMapping Structure</span></span>
<span data-ttu-id="93e72-103">Mappe un [!INCLUDE[wrt](../../../../includes/wrt-md.md)] GUID à son objet ICorDebugType correspondant.</span><span class="sxs-lookup"><span data-stu-id="93e72-103">Maps a [!INCLUDE[wrt](../../../../includes/wrt-md.md)] GUID to its corresponding ICorDebugType object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="93e72-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93e72-104">Syntax</span></span>  
  
```cpp
typedef struct CorDebugGuidToTypeMapping {  
    GUID iid;  
    ICorDebugType *pType;  
} CorDebugGuidToTypeMapping;  
```  
  
## <a name="members"></a><span data-ttu-id="93e72-105">Membres</span><span class="sxs-lookup"><span data-stu-id="93e72-105">Members</span></span>  
  
|<span data-ttu-id="93e72-106">Membre</span><span class="sxs-lookup"><span data-stu-id="93e72-106">Member</span></span>|<span data-ttu-id="93e72-107">Description</span><span class="sxs-lookup"><span data-stu-id="93e72-107">Description</span></span>|  
|------------|-----------------|  
|`iid`|<span data-ttu-id="93e72-108">Le GUID de la mise en cache [!INCLUDE[wrt](../../../../includes/wrt-md.md)] type.</span><span class="sxs-lookup"><span data-stu-id="93e72-108">The GUID of the cached [!INCLUDE[wrt](../../../../includes/wrt-md.md)] type.</span></span>|  
|`pType`|<span data-ttu-id="93e72-109">Pointeur vers un objet ICorDebugType qui fournit des informations sur le type de mise en cache.</span><span class="sxs-lookup"><span data-stu-id="93e72-109">A pointer to an ICorDebugType object that provides information about the cached type.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="93e72-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="93e72-110">Requirements</span></span>  
 <span data-ttu-id="93e72-111">**Plateformes :** [!INCLUDE[wrt](../../../../includes/wrt-md.md)].</span><span class="sxs-lookup"><span data-stu-id="93e72-111">**Platforms:** [!INCLUDE[wrt](../../../../includes/wrt-md.md)].</span></span>  
  
 <span data-ttu-id="93e72-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="93e72-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="93e72-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="93e72-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="93e72-114">**Versions du .NET framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="93e72-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93e72-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93e72-115">See Also</span></span>  
 [<span data-ttu-id="93e72-116">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="93e72-116">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)  
 [<span data-ttu-id="93e72-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="93e72-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
