---
title: CorDebugMDAFlags, énumération
ms.date: 03/30/2017
api_name:
- CorDebugMDAFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugMDAFlags
helpviewer_keywords:
- CorDebugMDAFlags enumeration [.NET Framework debugging]
ms.assetid: 7c0c92fe-8bd2-477f-b307-aca0143732ca
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 732523935eec62bffbc15705bc93c97f14c90064
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59148419"
---
# <a name="cordebugmdaflags-enumeration"></a><span data-ttu-id="8b844-102">CorDebugMDAFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="8b844-102">CorDebugMDAFlags Enumeration</span></span>
<span data-ttu-id="8b844-103">Spécifie l'état du thread sur lequel l'Assistant Débogage managé est déclenché.</span><span class="sxs-lookup"><span data-stu-id="8b844-103">Specifies the status of the thread on which the managed debugging assistant (MDA) is fired.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8b844-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b844-104">Syntax</span></span>  
  
```  
typedef enum CorDebugMDAFlags {  
    MDA_FLAG_SLIP = 0x2  
} CorDebugMDAFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="8b844-105">Membres</span><span class="sxs-lookup"><span data-stu-id="8b844-105">Members</span></span>  
  
|<span data-ttu-id="8b844-106">Membre</span><span class="sxs-lookup"><span data-stu-id="8b844-106">Member</span></span>|<span data-ttu-id="8b844-107">Description</span><span class="sxs-lookup"><span data-stu-id="8b844-107">Description</span></span>|  
|------------|-----------------|  
|`MDA_FLAG_SLIP`|<span data-ttu-id="8b844-108">Le thread sur lequel l’Assistant Débogage MANAGÉ a été lancé, a glissé depuis l’Assistant Débogage MANAGÉ a été déclenché.</span><span class="sxs-lookup"><span data-stu-id="8b844-108">The thread on which the MDA was fired has slipped since the MDA was fired.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8b844-109">Notes</span><span class="sxs-lookup"><span data-stu-id="8b844-109">Remarks</span></span>  
 <span data-ttu-id="8b844-110">Lorsque la pile des appels ne décrit plus où l’Assistant Débogage MANAGÉ a été lancé à l’origine, le thread est considérée comme ayant *glissé*.</span><span class="sxs-lookup"><span data-stu-id="8b844-110">When the call stack no longer describes where the MDA was originally raised, the thread is considered to have *slipped*.</span></span> <span data-ttu-id="8b844-111">Il s’agit d’une circonstance exceptionnelle provoquée par l’exécution du thread d’une opération non valide en quittant.</span><span class="sxs-lookup"><span data-stu-id="8b844-111">This is an unusual circumstance brought about by the thread's execution of an invalid operation upon exiting.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8b844-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b844-112">Requirements</span></span>  
 <span data-ttu-id="8b844-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8b844-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8b844-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8b844-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8b844-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8b844-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="8b844-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="8b844-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="8b844-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b844-117">See also</span></span>

- [<span data-ttu-id="8b844-118">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="8b844-118">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
