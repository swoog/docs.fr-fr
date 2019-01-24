---
title: ICorDebugAppDomain2, Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain2
helpviewer_keywords:
- ICorDebugAppDomain2 interface [.NET Framework debugging]
ms.assetid: 314d29f3-feb0-4a92-9530-b569c280cc31
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f4549b0fe6379979a7b9bd6344d65ff465f33f17
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506132"
---
# <a name="icordebugappdomain2-interface1"></a><span data-ttu-id="b7ad4-102">ICorDebugAppDomain2, Interface1</span><span class="sxs-lookup"><span data-stu-id="b7ad4-102">ICorDebugAppDomain2 Interface1</span></span>
<span data-ttu-id="b7ad4-103">Fournit des méthodes pour travailler avec des tableaux, les pointeurs, les pointeurs de fonction et les types référence.</span><span class="sxs-lookup"><span data-stu-id="b7ad4-103">Provides methods to work with arrays, pointers, function pointers, and reference types.</span></span> <span data-ttu-id="b7ad4-104">Cette interface est une extension de l’interface ICorDebugAppDomain.</span><span class="sxs-lookup"><span data-stu-id="b7ad4-104">This interface is an extension of the ICorDebugAppDomain interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b7ad4-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b7ad4-105">Methods</span></span>  
  
|<span data-ttu-id="b7ad4-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="b7ad4-106">Method</span></span>|<span data-ttu-id="b7ad4-107">Description</span><span class="sxs-lookup"><span data-stu-id="b7ad4-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b7ad4-108">GetArrayOrPointerType, méthode</span><span class="sxs-lookup"><span data-stu-id="b7ad4-108">GetArrayOrPointerType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain2-getarrayorpointertype-method.md)|<span data-ttu-id="b7ad4-109">Obtient un tableau du type spécifié, ou un pointeur ou une référence vers le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="b7ad4-109">Gets an array of the specified type, or a pointer or reference to the specified type.</span></span>|  
|[<span data-ttu-id="b7ad4-110">GetFunctionPointerType</span><span class="sxs-lookup"><span data-stu-id="b7ad4-110">GetFunctionPointerType</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain2-getfunctionpointertype-method.md)|<span data-ttu-id="b7ad4-111">Obtient un pointeur vers une fonction qui a une signature donnée.</span><span class="sxs-lookup"><span data-stu-id="b7ad4-111">Gets a pointer to a function that has a given signature.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b7ad4-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b7ad4-112">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b7ad4-113">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="b7ad4-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7ad4-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b7ad4-114">Requirements</span></span>  
 <span data-ttu-id="b7ad4-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b7ad4-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7ad4-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b7ad4-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b7ad4-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b7ad4-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b7ad4-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b7ad4-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7ad4-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7ad4-119">See also</span></span>
- [<span data-ttu-id="b7ad4-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="b7ad4-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
