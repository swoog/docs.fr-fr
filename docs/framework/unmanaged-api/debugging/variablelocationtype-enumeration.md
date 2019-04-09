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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59099948"
---
# <a name="variablelocationtype-enumeration"></a><span data-ttu-id="235b4-102">VariableLocationType, énumération</span><span class="sxs-lookup"><span data-stu-id="235b4-102">VariableLocationType Enumeration</span></span>
<span data-ttu-id="235b4-103">Indique le type d’emplacement native d’une variable.</span><span class="sxs-lookup"><span data-stu-id="235b4-103">Indicates the native location type of a variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="235b4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="235b4-104">Syntax</span></span>  
  
```  
typedef enum VariableLocationType  
{  
    VLT_REGISTER,               
    VLT_REGISTER_RELATIVE,      
    VLT_INVALID  
} VariableLocationType;  
```  
  
## <a name="members"></a><span data-ttu-id="235b4-105">Membres</span><span class="sxs-lookup"><span data-stu-id="235b4-105">Members</span></span>  
  
|<span data-ttu-id="235b4-106">Membre</span><span class="sxs-lookup"><span data-stu-id="235b4-106">Member</span></span>|<span data-ttu-id="235b4-107">Description</span><span class="sxs-lookup"><span data-stu-id="235b4-107">Description</span></span>|  
|------------|-----------------|  
|`VLT_REGISTER`|<span data-ttu-id="235b4-108">La variable est dans un Registre.</span><span class="sxs-lookup"><span data-stu-id="235b4-108">The variable is in a register.</span></span>|  
|`VLT_REGISTER_RELATIVE`|<span data-ttu-id="235b4-109">La variable est dans un emplacement de mémoire relative au Registre.</span><span class="sxs-lookup"><span data-stu-id="235b4-109">The variable is in a register-relative memory location.</span></span>|  
|`VLT_INVALID`|<span data-ttu-id="235b4-110">La variable n’est pas stockée dans un Registre ou un emplacement de mémoire relative au Registre.</span><span class="sxs-lookup"><span data-stu-id="235b4-110">The variable is not stored in a register or a register-relative memory location.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="235b4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="235b4-111">Remarks</span></span>  
 <span data-ttu-id="235b4-112">Un membre de la `VariableLocationType` énumération est retournée par la [ICorDebugVariableHome::GetLocationType](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getlocationtype-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="235b4-112">A member of the `VariableLocationType` enumeration is returned by the [ICorDebugVariableHome::GetLocationType](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getlocationtype-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="235b4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="235b4-113">Requirements</span></span>  
 <span data-ttu-id="235b4-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="235b4-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="235b4-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="235b4-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="235b4-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="235b4-116">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="235b4-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="235b4-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="235b4-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="235b4-118">See also</span></span>

- [<span data-ttu-id="235b4-119">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="235b4-119">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
