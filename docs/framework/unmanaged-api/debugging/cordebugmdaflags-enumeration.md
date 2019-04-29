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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61792715"
---
# <a name="cordebugmdaflags-enumeration"></a><span data-ttu-id="77c50-102">CorDebugMDAFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="77c50-102">CorDebugMDAFlags Enumeration</span></span>
<span data-ttu-id="77c50-103">Spécifie l'état du thread sur lequel l'Assistant Débogage managé est déclenché.</span><span class="sxs-lookup"><span data-stu-id="77c50-103">Specifies the status of the thread on which the managed debugging assistant (MDA) is fired.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77c50-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77c50-104">Syntax</span></span>  
  
```  
typedef enum CorDebugMDAFlags {  
    MDA_FLAG_SLIP = 0x2  
} CorDebugMDAFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="77c50-105">Membres</span><span class="sxs-lookup"><span data-stu-id="77c50-105">Members</span></span>  
  
|<span data-ttu-id="77c50-106">Membre</span><span class="sxs-lookup"><span data-stu-id="77c50-106">Member</span></span>|<span data-ttu-id="77c50-107">Description</span><span class="sxs-lookup"><span data-stu-id="77c50-107">Description</span></span>|  
|------------|-----------------|  
|`MDA_FLAG_SLIP`|<span data-ttu-id="77c50-108">Le thread sur lequel l’Assistant Débogage MANAGÉ a été lancé, a glissé depuis l’Assistant Débogage MANAGÉ a été déclenché.</span><span class="sxs-lookup"><span data-stu-id="77c50-108">The thread on which the MDA was fired has slipped since the MDA was fired.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="77c50-109">Notes</span><span class="sxs-lookup"><span data-stu-id="77c50-109">Remarks</span></span>  
 <span data-ttu-id="77c50-110">Lorsque la pile des appels ne décrit plus où l’Assistant Débogage MANAGÉ a été lancé à l’origine, le thread est considérée comme ayant *glissé*.</span><span class="sxs-lookup"><span data-stu-id="77c50-110">When the call stack no longer describes where the MDA was originally raised, the thread is considered to have *slipped*.</span></span> <span data-ttu-id="77c50-111">Il s’agit d’une circonstance exceptionnelle provoquée par l’exécution du thread d’une opération non valide en quittant.</span><span class="sxs-lookup"><span data-stu-id="77c50-111">This is an unusual circumstance brought about by the thread's execution of an invalid operation upon exiting.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="77c50-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77c50-112">Requirements</span></span>  
 <span data-ttu-id="77c50-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="77c50-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="77c50-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="77c50-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="77c50-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="77c50-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="77c50-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="77c50-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77c50-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77c50-117">See also</span></span>

- [<span data-ttu-id="77c50-118">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="77c50-118">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
