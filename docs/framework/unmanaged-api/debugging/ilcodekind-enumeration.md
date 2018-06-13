---
title: ILCodeKind, énumération
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ILCodeKind
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: b91765e4-82db-46f9-a6dc-6b80610276af
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0881b3903200c023cfa2fe32bf89f62234da29c3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33424025"
---
# <a name="ilcodekind-enumeration"></a><span data-ttu-id="6bae6-102">ILCodeKind, énumération</span><span class="sxs-lookup"><span data-stu-id="6bae6-102">ILCodeKind Enumeration</span></span>
<span data-ttu-id="6bae6-103">[Pris en charge dans .NET Framework 4.5.2 et ultérieur]</span><span class="sxs-lookup"><span data-stu-id="6bae6-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="6bae6-104">Fournit des valeurs qui spécifient si le débogueur peut accéder aux variables locales ou au code ajoutés dans l'instrumentation ReJIT du profileur.</span><span class="sxs-lookup"><span data-stu-id="6bae6-104">Provides values that specify whether the debugger is able to access local variables or code added in profiler ReJIT instrumentation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6bae6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6bae6-105">Syntax</span></span>  
  
```cpp
typedef enum ILCodeKind {  
   ILCODE_ORIGINAL_IL = 0x1,  
   ILCODE_REJIT_IL = 0x2,  
} ILCodeKind;  
```  
  
## <a name="members"></a><span data-ttu-id="6bae6-106">Membres</span><span class="sxs-lookup"><span data-stu-id="6bae6-106">Members</span></span>  
  
|<span data-ttu-id="6bae6-107">Nom de membre</span><span class="sxs-lookup"><span data-stu-id="6bae6-107">Member name</span></span>|<span data-ttu-id="6bae6-108">Description</span><span class="sxs-lookup"><span data-stu-id="6bae6-108">Description</span></span>|  
|-----------------|-----------------|  
|`ILCODE_ORIGINAL_IL`|<span data-ttu-id="6bae6-109">Le débogueur n'a pas accès aux informations de l'instrumentation ReJIT.</span><span class="sxs-lookup"><span data-stu-id="6bae6-109">The debugger does not have access to information from ReJIT instrumentation.</span></span>|  
|`ILCODE_REJIT_IL`|<span data-ttu-id="6bae6-110">Le débogueur a accès aux informations de l'instrumentation ReJIT.</span><span class="sxs-lookup"><span data-stu-id="6bae6-110">The debugger has access to information from ReJIT instrumentation.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6bae6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6bae6-111">Remarks</span></span>  
 <span data-ttu-id="6bae6-112">Un membre de la `ILCodeKind` énumération peut être passée à la [EnumerateLocalVariablesEx](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-enumeratelocalvariablesex-method.md) et [GetLocalVariableEx](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-getlocalvariableex-method.md) méthodes permettent de déterminer si le débogueur peut accéder aux variables ajoutées dans le Générateur de profils L’instrumentation ReJIT et à la [GetCodeEx](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-getcodeex-method.md) langage intermédiaire instrumenté de méthode pour déterminer si le débogueur peut accéder.</span><span class="sxs-lookup"><span data-stu-id="6bae6-112">A member of the `ILCodeKind` enumeration can be passed to the [EnumerateLocalVariablesEx](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-enumeratelocalvariablesex-method.md) and [GetLocalVariableEx](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-getlocalvariableex-method.md) methods to determine whether the debugger can access variables added in profiler ReJIT instrumentation, and to the [GetCodeEx](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-getcodeex-method.md) method to determine whether the debugger can access instrumented IL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6bae6-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6bae6-113">Requirements</span></span>  
 <span data-ttu-id="6bae6-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6bae6-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6bae6-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6bae6-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6bae6-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6bae6-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6bae6-117">**Versions du .NET framework :** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6bae6-117">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6bae6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bae6-118">See Also</span></span>  
 [<span data-ttu-id="6bae6-119">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="6bae6-119">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)  
 [<span data-ttu-id="6bae6-120">ICorDebugILFrame4, interface</span><span class="sxs-lookup"><span data-stu-id="6bae6-120">ICorDebugILFrame4 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-interface.md)  
 [<span data-ttu-id="6bae6-121">ReJIT : Un Guide de procédures relatives</span><span class="sxs-lookup"><span data-stu-id="6bae6-121">ReJIT: A How-To Guide</span></span>](http://blogs.msdn.com/b/davbr/archive/2011/10/12/rejit-a-how-to-guide.aspx)
