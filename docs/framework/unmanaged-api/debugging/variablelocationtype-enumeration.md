---
title: VariableLocationType, énumération
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
ms.openlocfilehash: 392254efcd099aca60e58b3cc0bc61ca85aa2c66
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61986516"
---
# <a name="variablelocationtype-enumeration"></a><span data-ttu-id="46176-102">VariableLocationType, énumération</span><span class="sxs-lookup"><span data-stu-id="46176-102">VariableLocationType Enumeration</span></span>
<span data-ttu-id="46176-103">Indique le type d’emplacement native d’une variable.</span><span class="sxs-lookup"><span data-stu-id="46176-103">Indicates the native location type of a variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46176-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46176-104">Syntax</span></span>  
  
```  
typedef enum VariableLocationType  
{  
    VLT_REGISTER,               
    VLT_REGISTER_RELATIVE,      
    VLT_INVALID  
} VariableLocationType;  
```  
  
## <a name="members"></a><span data-ttu-id="46176-105">Membres</span><span class="sxs-lookup"><span data-stu-id="46176-105">Members</span></span>  
  
|<span data-ttu-id="46176-106">Membre</span><span class="sxs-lookup"><span data-stu-id="46176-106">Member</span></span>|<span data-ttu-id="46176-107">Description</span><span class="sxs-lookup"><span data-stu-id="46176-107">Description</span></span>|  
|------------|-----------------|  
|`VLT_REGISTER`|<span data-ttu-id="46176-108">La variable est dans un Registre.</span><span class="sxs-lookup"><span data-stu-id="46176-108">The variable is in a register.</span></span>|  
|`VLT_REGISTER_RELATIVE`|<span data-ttu-id="46176-109">La variable est dans un emplacement de mémoire relative au Registre.</span><span class="sxs-lookup"><span data-stu-id="46176-109">The variable is in a register-relative memory location.</span></span>|  
|`VLT_INVALID`|<span data-ttu-id="46176-110">La variable n’est pas stockée dans un Registre ou un emplacement de mémoire relative au Registre.</span><span class="sxs-lookup"><span data-stu-id="46176-110">The variable is not stored in a register or a register-relative memory location.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="46176-111">Notes</span><span class="sxs-lookup"><span data-stu-id="46176-111">Remarks</span></span>  
 <span data-ttu-id="46176-112">Un membre de la `VariableLocationType` énumération est retournée par la [ICorDebugVariableHome::GetLocationType](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getlocationtype-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="46176-112">A member of the `VariableLocationType` enumeration is returned by the [ICorDebugVariableHome::GetLocationType](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getlocationtype-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="46176-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46176-113">Requirements</span></span>  
 <span data-ttu-id="46176-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="46176-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="46176-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="46176-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="46176-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="46176-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="46176-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="46176-117">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46176-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46176-118">See also</span></span>

- [<span data-ttu-id="46176-119">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="46176-119">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
