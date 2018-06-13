---
title: CorDebugIlToNativeMappingTypes, énumération
ms.date: 03/30/2017
api_name:
- CorDebugIlToNativeMappingTypes
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugIlToNativeMappingTypes
helpviewer_keywords:
- CorDebugIIToNativeMappingTypes enumeration [.NET Framework debugging]
ms.assetid: c35e2919-42c3-4ba0-ae28-443c35f66f93
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9fec0f4f31f45847dc092808b2d47c662213e9d2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402518"
---
# <a name="cordebugiltonativemappingtypes-enumeration"></a><span data-ttu-id="fa58f-102">CorDebugIlToNativeMappingTypes, énumération</span><span class="sxs-lookup"><span data-stu-id="fa58f-102">CorDebugIlToNativeMappingTypes Enumeration</span></span>
<span data-ttu-id="fa58f-103">Indique si une plage particulière d’instructions natives, représentée par une instance de la structure COR_DEBUG_IL_TO_NATIVE_MAP, correspond à une région de code spéciale.</span><span class="sxs-lookup"><span data-stu-id="fa58f-103">Indicates whether a particular range of native instructions, represented by an instance of the COR_DEBUG_IL_TO_NATIVE_MAP structure, corresponds to a special code region.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa58f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa58f-104">Syntax</span></span>  
  
```  
typedef enum CorDebugIlToNativeMappingTypes {  
    NO_MAPPING = -1,  
    PROLOG     = -2,  
    EPILOG     = -3  
} CorDebugIlToNativeMappingTypes;  
```  
  
## <a name="members"></a><span data-ttu-id="fa58f-105">Membres</span><span class="sxs-lookup"><span data-stu-id="fa58f-105">Members</span></span>  
  
|<span data-ttu-id="fa58f-106">Membre</span><span class="sxs-lookup"><span data-stu-id="fa58f-106">Member</span></span>|<span data-ttu-id="fa58f-107">Description</span><span class="sxs-lookup"><span data-stu-id="fa58f-107">Description</span></span>|  
|------------|-----------------|  
|`NO_MAPPING`|<span data-ttu-id="fa58f-108">La plage d’instructions natives ne correspond pas à n’importe quelle région de code spéciale.</span><span class="sxs-lookup"><span data-stu-id="fa58f-108">The range of native instructions does not correspond to any special code region.</span></span>|  
|`PROLOG`|<span data-ttu-id="fa58f-109">La plage d’instructions natives correspond au prologue.</span><span class="sxs-lookup"><span data-stu-id="fa58f-109">The range of native instructions corresponds to the prolog.</span></span>|  
|`EPILOG`|<span data-ttu-id="fa58f-110">La plage d’instructions natives correspond à l’épilogue.</span><span class="sxs-lookup"><span data-stu-id="fa58f-110">The range of native instructions corresponds to the epilog.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fa58f-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fa58f-111">Requirements</span></span>  
 <span data-ttu-id="fa58f-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fa58f-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fa58f-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fa58f-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fa58f-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fa58f-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fa58f-115">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fa58f-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa58f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa58f-116">See Also</span></span>  
 [<span data-ttu-id="fa58f-117">GetILToNativeMapping, méthode</span><span class="sxs-lookup"><span data-stu-id="fa58f-117">GetILToNativeMapping Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode-getiltonativemapping-method.md)  
 [<span data-ttu-id="fa58f-118">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="fa58f-118">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
