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
ms.openlocfilehash: 49290a37ca7ea101e3c8b458a5daa4995cb3beee
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54610043"
---
# <a name="cordebugguidtotypemapping-structure"></a><span data-ttu-id="1abdc-102">CorDebugGuidToTypeMapping, structure</span><span class="sxs-lookup"><span data-stu-id="1abdc-102">CorDebugGuidToTypeMapping Structure</span></span>
<span data-ttu-id="1abdc-103">Mappages une [!INCLUDE[wrt](../../../../includes/wrt-md.md)] GUID à son objet ICorDebugType correspondant.</span><span class="sxs-lookup"><span data-stu-id="1abdc-103">Maps a [!INCLUDE[wrt](../../../../includes/wrt-md.md)] GUID to its corresponding ICorDebugType object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1abdc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1abdc-104">Syntax</span></span>  
  
```cpp
typedef struct CorDebugGuidToTypeMapping {  
    GUID iid;  
    ICorDebugType *pType;  
} CorDebugGuidToTypeMapping;  
```  
  
## <a name="members"></a><span data-ttu-id="1abdc-105">Membres</span><span class="sxs-lookup"><span data-stu-id="1abdc-105">Members</span></span>  
  
|<span data-ttu-id="1abdc-106">Membre</span><span class="sxs-lookup"><span data-stu-id="1abdc-106">Member</span></span>|<span data-ttu-id="1abdc-107">Description</span><span class="sxs-lookup"><span data-stu-id="1abdc-107">Description</span></span>|  
|------------|-----------------|  
|`iid`|<span data-ttu-id="1abdc-108">Le GUID de la mise en cache [!INCLUDE[wrt](../../../../includes/wrt-md.md)] type.</span><span class="sxs-lookup"><span data-stu-id="1abdc-108">The GUID of the cached [!INCLUDE[wrt](../../../../includes/wrt-md.md)] type.</span></span>|  
|`pType`|<span data-ttu-id="1abdc-109">Pointeur vers un objet ICorDebugType qui fournit des informations sur le type mis en cache.</span><span class="sxs-lookup"><span data-stu-id="1abdc-109">A pointer to an ICorDebugType object that provides information about the cached type.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1abdc-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1abdc-110">Requirements</span></span>  
 <span data-ttu-id="1abdc-111">**Plateformes :** [!INCLUDE[wrt](../../../../includes/wrt-md.md)].</span><span class="sxs-lookup"><span data-stu-id="1abdc-111">**Platforms:** [!INCLUDE[wrt](../../../../includes/wrt-md.md)].</span></span>  
  
 <span data-ttu-id="1abdc-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1abdc-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1abdc-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1abdc-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1abdc-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1abdc-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1abdc-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1abdc-115">See also</span></span>
- [<span data-ttu-id="1abdc-116">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="1abdc-116">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="1abdc-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="1abdc-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
