---
title: ICorDebugMergedAssemblyRecord::GetIndex, méthode
ms.date: 03/30/2017
ms.assetid: 98701444-b9bc-4978-9548-89ac3394147d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b8ba470325098125aee8ef7de01fa6aa70596d42
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59202597"
---
# <a name="icordebugmergedassemblyrecordgetindex-method"></a><span data-ttu-id="a9fc5-102">ICorDebugMergedAssemblyRecord::GetIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="a9fc5-102">ICorDebugMergedAssemblyRecord::GetIndex Method</span></span>
<span data-ttu-id="a9fc5-103">Obtient l'index de préfixe de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="a9fc5-103">Gets the assembly's prefix index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a9fc5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9fc5-104">Syntax</span></span>  
  
```  
HRESULT GetIndex(  
   [out] ULONG32 *pIndex  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a9fc5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9fc5-105">Parameters</span></span>  
 `pIndex`  
 <span data-ttu-id="a9fc5-106">[out] Pointeur vers l'index de préfixe.</span><span class="sxs-lookup"><span data-stu-id="a9fc5-106">[out] A pointer to the prefix index.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a9fc5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a9fc5-107">Remarks</span></span>  
 <span data-ttu-id="a9fc5-108">L'index de préfixe est utilisé pour empêcher les collisions de noms dans les noms de types de métadonnées fusionnées.</span><span class="sxs-lookup"><span data-stu-id="a9fc5-108">The prefix index is used to prevent name collisions in the merged metadata type names.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a9fc5-109">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="a9fc5-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a9fc5-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9fc5-110">Requirements</span></span>  
 <span data-ttu-id="a9fc5-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a9fc5-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a9fc5-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a9fc5-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a9fc5-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a9fc5-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a9fc5-114">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a9fc5-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9fc5-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9fc5-115">See also</span></span>

- [<span data-ttu-id="a9fc5-116">ICorDebugMergedAssemblyRecord, interface</span><span class="sxs-lookup"><span data-stu-id="a9fc5-116">ICorDebugMergedAssemblyRecord Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmergedassemblyrecord-interface.md)
- [<span data-ttu-id="a9fc5-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="a9fc5-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
