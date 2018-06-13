---
title: Énumération de VariableLocationType
ms.date: 03/30/2017
api_name:
- VariableLocationType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- VariableLocationType
helpviewer_keywords:
- VariableLocationType enumeration [.NET Framework debugging]
ms.assetid: 8635ee3a-c84b-4626-876c-416bee54f787
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1cc7a299e6be328095c0368acf0a4b767fb74d01
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33423947"
---
# <a name="variablelocationtype-enumeration"></a><span data-ttu-id="e5631-102">Énumération de VariableLocationType</span><span class="sxs-lookup"><span data-stu-id="e5631-102">VariableLocationType Enumeration</span></span>
<span data-ttu-id="e5631-103">Indique le type d’emplacement native d’une variable.</span><span class="sxs-lookup"><span data-stu-id="e5631-103">Indicates the native location type of a variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5631-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5631-104">Syntax</span></span>  
  
```  
typedef enum VariableLocationType  
{  
    VLT_REGISTER,               
    VLT_REGISTER_RELATIVE,      
    VLT_INVALID  
} VariableLocationType;  
```  
  
## <a name="members"></a><span data-ttu-id="e5631-105">Membres</span><span class="sxs-lookup"><span data-stu-id="e5631-105">Members</span></span>  
  
|<span data-ttu-id="e5631-106">Membre</span><span class="sxs-lookup"><span data-stu-id="e5631-106">Member</span></span>|<span data-ttu-id="e5631-107">Description</span><span class="sxs-lookup"><span data-stu-id="e5631-107">Description</span></span>|  
|------------|-----------------|  
|`VLT_REGISTER`|<span data-ttu-id="e5631-108">La variable est dans un Registre.</span><span class="sxs-lookup"><span data-stu-id="e5631-108">The variable is in a register.</span></span>|  
|`VLT_REGISTER_RELATIVE`|<span data-ttu-id="e5631-109">La variable est dans un emplacement de mémoire relative au Registre.</span><span class="sxs-lookup"><span data-stu-id="e5631-109">The variable is in a register-relative memory location.</span></span>|  
|`VLT_INVALID`|<span data-ttu-id="e5631-110">La variable n’est pas stockée dans un Registre ou un emplacement de mémoire relative au Registre.</span><span class="sxs-lookup"><span data-stu-id="e5631-110">The variable is not stored in a register or a register-relative memory location.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e5631-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e5631-111">Remarks</span></span>  
 <span data-ttu-id="e5631-112">Un membre de la `VariableLocationType` énumération retournée par le [ICorDebugVariableHome::GetLocationType](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getlocationtype-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="e5631-112">A member of the `VariableLocationType` enumeration is returned by the [ICorDebugVariableHome::GetLocationType](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getlocationtype-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e5631-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e5631-113">Requirements</span></span>  
 <span data-ttu-id="e5631-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e5631-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5631-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e5631-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e5631-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e5631-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e5631-117">**Versions du .NET framework :** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e5631-117">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5631-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5631-118">See Also</span></span>  
 [<span data-ttu-id="e5631-119">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="e5631-119">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
