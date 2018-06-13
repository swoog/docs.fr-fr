---
title: LoggingLevelEnum, énumération
ms.date: 03/30/2017
api_name:
- LoggingLevelEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- LoggingLevelEnum
helpviewer_keywords:
- LoggingLevelEnum enumeration [.NET Framework debugging]
ms.assetid: 09daac08-005a-46b2-beab-408d0820c5e5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 331065d4aae82c66b9ebd82e99427501c3ba8a98
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33435953"
---
# <a name="logginglevelenum-enumeration"></a><span data-ttu-id="60445-102">LoggingLevelEnum, énumération</span><span class="sxs-lookup"><span data-stu-id="60445-102">LoggingLevelEnum Enumeration</span></span>
<span data-ttu-id="60445-103">Indique le niveau de gravité d'un message de description qui est écrit dans le journal des événements quand un thread managé consigne un événement.</span><span class="sxs-lookup"><span data-stu-id="60445-103">Indicates the severity level of a descriptive message that is written to the event log when a managed thread logs an event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="60445-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60445-104">Syntax</span></span>  
  
```  
typedef enum LoggingLevelEnum {  
    LTraceLevel0 = 0,  
    LTraceLevel1,  
    LTraceLevel2,  
    LTraceLevel3,  
    LTraceLevel4,  
    LStatusLevel0 = 20,  
    LStatusLevel1,  
    LStatusLevel2,  
    LStatusLevel3,  
    LStatusLevel4,  
    LWarningLevel = 40,  
    LErrorLevel = 50,  
    LPanicLevel = 100  
} LoggingLevelEnum;  
```  
  
## <a name="members"></a><span data-ttu-id="60445-105">Membres</span><span class="sxs-lookup"><span data-stu-id="60445-105">Members</span></span>  
  
|<span data-ttu-id="60445-106">Membre</span><span class="sxs-lookup"><span data-stu-id="60445-106">Member</span></span>|<span data-ttu-id="60445-107">Description</span><span class="sxs-lookup"><span data-stu-id="60445-107">Description</span></span>|  
|------------|-----------------|  
|`LTraceLevel0`|<span data-ttu-id="60445-108">Le message est un niveau de trace 0.</span><span class="sxs-lookup"><span data-stu-id="60445-108">The message is a trace level 0.</span></span>|  
|`LTraceLevel1`|<span data-ttu-id="60445-109">Le message est un niveau de trace 1.</span><span class="sxs-lookup"><span data-stu-id="60445-109">The message is a trace level 1.</span></span>|  
|`LTraceLevel2`|<span data-ttu-id="60445-110">Le message est un niveau de trace 2.</span><span class="sxs-lookup"><span data-stu-id="60445-110">The message is a trace level 2.</span></span>|  
|`LTraceLevel3`|<span data-ttu-id="60445-111">Le message est un niveau de trace 3.</span><span class="sxs-lookup"><span data-stu-id="60445-111">The message is a trace level 3.</span></span>|  
|`LTraceLevel4`|<span data-ttu-id="60445-112">Le message est un niveau de trace 4.</span><span class="sxs-lookup"><span data-stu-id="60445-112">The message is a trace level 4.</span></span>|  
|`LStatusLevel0`|<span data-ttu-id="60445-113">Le message est un niveau d’état 0.</span><span class="sxs-lookup"><span data-stu-id="60445-113">The message is a status level 0.</span></span>|  
|`LStatusLevel1`|<span data-ttu-id="60445-114">Le message est un niveau de statut 1.</span><span class="sxs-lookup"><span data-stu-id="60445-114">The message is a status level 1.</span></span>|  
|`LStatusLevel2`|<span data-ttu-id="60445-115">Le message est un niveau de statut 2.</span><span class="sxs-lookup"><span data-stu-id="60445-115">The message is a status level 2.</span></span>|  
|`LStatusLevel3`|<span data-ttu-id="60445-116">Le message est un niveau de statut 3.</span><span class="sxs-lookup"><span data-stu-id="60445-116">The message is a status level 3.</span></span>|  
|`LStatusLevel4`|<span data-ttu-id="60445-117">Le message est un niveau de statut 4.</span><span class="sxs-lookup"><span data-stu-id="60445-117">The message is a status level 4.</span></span>|  
|`LWarningLevel`|<span data-ttu-id="60445-118">Le message est un niveau d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="60445-118">The message is a warning level.</span></span>|  
|`LErrorLevel`|<span data-ttu-id="60445-119">Le message est un niveau d’erreur.</span><span class="sxs-lookup"><span data-stu-id="60445-119">The message is an error level.</span></span>|  
|`LPanicLevel`|<span data-ttu-id="60445-120">Le message est un niveau de panique.</span><span class="sxs-lookup"><span data-stu-id="60445-120">The message is a panic level.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="60445-121">Notes</span><span class="sxs-lookup"><span data-stu-id="60445-121">Remarks</span></span>  
 <span data-ttu-id="60445-122">Le common language runtime (CLR) appelle la [ICorDebugManagedCallback::LogMessage](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-logmessage-method.md) méthode pour informer le débogueur qu’un thread managé a enregistré un événement.</span><span class="sxs-lookup"><span data-stu-id="60445-122">The common language runtime (CLR) calls the [ICorDebugManagedCallback::LogMessage](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-logmessage-method.md) method to notify the debugger that a managed thread has logged an event.</span></span> <span data-ttu-id="60445-123">Le CLR passe une valeur de la `LoggingLevelEnum` énumération pour indiquer le niveau de gravité du message que le thread managé a écrit dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="60445-123">The CLR passes a value of the `LoggingLevelEnum` enumeration to indicate the severity level of the message that the managed thread wrote to the event log.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="60445-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="60445-124">Requirements</span></span>  
 <span data-ttu-id="60445-125">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="60445-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="60445-126">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="60445-126">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="60445-127">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="60445-127">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="60445-128">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="60445-128">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="60445-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60445-129">See Also</span></span>  
 <xref:System.Diagnostics.EventLog>  
 [<span data-ttu-id="60445-130">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="60445-130">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
