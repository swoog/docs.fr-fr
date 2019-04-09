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
ms.openlocfilehash: 9dc7093edaf12e801a1e1adc52b0be823ff92b91
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59079914"
---
# <a name="cordebugguidtotypemapping-structure"></a><span data-ttu-id="4a2bc-102">CorDebugGuidToTypeMapping, structure</span><span class="sxs-lookup"><span data-stu-id="4a2bc-102">CorDebugGuidToTypeMapping Structure</span></span>
<span data-ttu-id="4a2bc-103">Mappages une [!INCLUDE[wrt](../../../../includes/wrt-md.md)] GUID à son objet ICorDebugType correspondant.</span><span class="sxs-lookup"><span data-stu-id="4a2bc-103">Maps a [!INCLUDE[wrt](../../../../includes/wrt-md.md)] GUID to its corresponding ICorDebugType object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4a2bc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a2bc-104">Syntax</span></span>  
  
```cpp
typedef struct CorDebugGuidToTypeMapping {  
    GUID iid;  
    ICorDebugType *pType;  
} CorDebugGuidToTypeMapping;  
```  
  
## <a name="members"></a><span data-ttu-id="4a2bc-105">Membres</span><span class="sxs-lookup"><span data-stu-id="4a2bc-105">Members</span></span>  
  
|<span data-ttu-id="4a2bc-106">Membre</span><span class="sxs-lookup"><span data-stu-id="4a2bc-106">Member</span></span>|<span data-ttu-id="4a2bc-107">Description</span><span class="sxs-lookup"><span data-stu-id="4a2bc-107">Description</span></span>|  
|------------|-----------------|  
|`iid`|<span data-ttu-id="4a2bc-108">Le GUID de la mise en cache [!INCLUDE[wrt](../../../../includes/wrt-md.md)] type.</span><span class="sxs-lookup"><span data-stu-id="4a2bc-108">The GUID of the cached [!INCLUDE[wrt](../../../../includes/wrt-md.md)] type.</span></span>|  
|`pType`|<span data-ttu-id="4a2bc-109">Pointeur vers un objet ICorDebugType qui fournit des informations sur le type mis en cache.</span><span class="sxs-lookup"><span data-stu-id="4a2bc-109">A pointer to an ICorDebugType object that provides information about the cached type.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="4a2bc-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a2bc-110">Requirements</span></span>  
 <span data-ttu-id="4a2bc-111">**Plateformes :** [!INCLUDE[wrt](../../../../includes/wrt-md.md)].</span><span class="sxs-lookup"><span data-stu-id="4a2bc-111">**Platforms:** [!INCLUDE[wrt](../../../../includes/wrt-md.md)].</span></span>  
  
 <span data-ttu-id="4a2bc-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4a2bc-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4a2bc-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4a2bc-113">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="4a2bc-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="4a2bc-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="4a2bc-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a2bc-115">See also</span></span>

- [<span data-ttu-id="4a2bc-116">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="4a2bc-116">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="4a2bc-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="4a2bc-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
