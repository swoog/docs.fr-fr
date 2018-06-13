---
title: COR_SEGMENT, structure
ms.date: 03/30/2017
api_name:
- COR_SEGMENT
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_SEGMENT
helpviewer_keywords:
- COR_SEGMENT structure [.NET Framework debugging]
ms.assetid: 93aeecb9-7fef-4545-8daf-f566dfc47084
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b816087f54e652f07dc791b7d66eb1af8f52f55e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33406505"
---
# <a name="corsegment-structure"></a><span data-ttu-id="f3de6-102">COR_SEGMENT, structure</span><span class="sxs-lookup"><span data-stu-id="f3de6-102">COR_SEGMENT Structure</span></span>
<span data-ttu-id="f3de6-103">Contient des informations sur une région de la mémoire dans le tas managé.</span><span class="sxs-lookup"><span data-stu-id="f3de6-103">Contains information about a region of memory in the managed heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f3de6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3de6-104">Syntax</span></span>  
  
```  
typedef struct _COR_SEGMENT {  
    CORDB_ADDRESS start;            
    CORDB_ADDRESS end;              
    CorDebugGenerationTypes gen;    
    ULONG heap;                     
} COR_SEGMENT;  
```  
  
## <a name="members"></a><span data-ttu-id="f3de6-105">Membres</span><span class="sxs-lookup"><span data-stu-id="f3de6-105">Members</span></span>  
  
|<span data-ttu-id="f3de6-106">Membre</span><span class="sxs-lookup"><span data-stu-id="f3de6-106">Member</span></span>|<span data-ttu-id="f3de6-107">Description</span><span class="sxs-lookup"><span data-stu-id="f3de6-107">Description</span></span>|  
|------------|-----------------|  
|`start`|<span data-ttu-id="f3de6-108">Adresse de départ de la région de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f3de6-108">The starting address of the memory region.</span></span>|  
|`end`|<span data-ttu-id="f3de6-109">L’adresse de fin de la région de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f3de6-109">The ending address of the memory region.</span></span>|  
|`gen`|<span data-ttu-id="f3de6-110">A [CorDebugGenerationTypes](../../../../docs/framework/unmanaged-api/debugging/cordebuggenerationtypes-enumeration.md) membre d’énumération qui indique la génération de la région de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f3de6-110">A [CorDebugGenerationTypes](../../../../docs/framework/unmanaged-api/debugging/cordebuggenerationtypes-enumeration.md) enumeration member that indicates the generation of the memory region.</span></span>|  
|`heap`|<span data-ttu-id="f3de6-111">Le numéro de segment de mémoire dans lequel réside la région de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f3de6-111">The heap number in which the memory region resides.</span></span> <span data-ttu-id="f3de6-112">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="f3de6-112">See the Remarks section for more information.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f3de6-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f3de6-113">Remarks</span></span>  
 <span data-ttu-id="f3de6-114">Le `COR_SEGMENTS` structure représente une région de mémoire dans le tas managé.</span><span class="sxs-lookup"><span data-stu-id="f3de6-114">The `COR_SEGMENTS` structure represents a region of memory in the managed heap.</span></span>  <span data-ttu-id="f3de6-115">`COR_SEGMENTS` les objets sont membres de la [ICorDebugHeapRegionEnum](../../../../docs/framework/unmanaged-api/debugging/icordebugheapsegmentenum-interface.md) objet de collection, qui est remplie en appelant le[ICorDebugProcess5::EnumerateHeapRegions](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerateheapregions-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="f3de6-115">`COR_SEGMENTS` objects are members of the [ICorDebugHeapRegionEnum](../../../../docs/framework/unmanaged-api/debugging/icordebugheapsegmentenum-interface.md) collection object, which is populated by calling the[ICorDebugProcess5::EnumerateHeapRegions](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerateheapregions-method.md) method.</span></span>  
  
 <span data-ttu-id="f3de6-116">Le `heap` champ est le nombre de processeur, ce qui correspond au segment de mémoire signalée.</span><span class="sxs-lookup"><span data-stu-id="f3de6-116">The `heap` field is the processor number, which corresponds to the heap being reported.</span></span> <span data-ttu-id="f3de6-117">Pour la station de travail des garbage collectors, sa valeur est toujours égal à zéro, car les stations de travail ont uniquement un tas de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="f3de6-117">For workstation garbage collectors, its value is always zero, because workstations have only one garbage collection heap.</span></span> <span data-ttu-id="f3de6-118">Pour le serveur des garbage collectors, sa valeur correspond au processeur d’à que tas est attaché.</span><span class="sxs-lookup"><span data-stu-id="f3de6-118">For server garbage collectors, its value corresponds to the processor the heap is attached to.</span></span> <span data-ttu-id="f3de6-119">Notez qu’il existe peut-être plus ou moins le garbage collection segments de mémoire qu’il ne sont processeurs réelles en raison des détails d’implémentation du garbage collector.</span><span class="sxs-lookup"><span data-stu-id="f3de6-119">Note that there may be more or fewer garbage collection heaps than there are actual processors due to the implementation details of the garbage collector.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f3de6-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f3de6-120">Requirements</span></span>  
 <span data-ttu-id="f3de6-121">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f3de6-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f3de6-122">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f3de6-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f3de6-123">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f3de6-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f3de6-124">**Versions du .NET framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f3de6-124">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3de6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3de6-125">See Also</span></span>  
 [<span data-ttu-id="f3de6-126">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="f3de6-126">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)  
 [<span data-ttu-id="f3de6-127">Débogage</span><span class="sxs-lookup"><span data-stu-id="f3de6-127">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
