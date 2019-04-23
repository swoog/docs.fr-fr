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
ms.openlocfilehash: 2fe8e1355382273a681e927897f4a8ff5814b8de
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59086505"
---
# <a name="logginglevelenum-enumeration"></a><span data-ttu-id="c87c3-102">LoggingLevelEnum, énumération</span><span class="sxs-lookup"><span data-stu-id="c87c3-102">LoggingLevelEnum Enumeration</span></span>
<span data-ttu-id="c87c3-103">Indique le niveau de gravité d'un message de description qui est écrit dans le journal des événements quand un thread managé consigne un événement.</span><span class="sxs-lookup"><span data-stu-id="c87c3-103">Indicates the severity level of a descriptive message that is written to the event log when a managed thread logs an event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c87c3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c87c3-104">Syntax</span></span>  
  
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
  
## <a name="members"></a><span data-ttu-id="c87c3-105">Membres</span><span class="sxs-lookup"><span data-stu-id="c87c3-105">Members</span></span>  
  
|<span data-ttu-id="c87c3-106">Membre</span><span class="sxs-lookup"><span data-stu-id="c87c3-106">Member</span></span>|<span data-ttu-id="c87c3-107">Description</span><span class="sxs-lookup"><span data-stu-id="c87c3-107">Description</span></span>|  
|------------|-----------------|  
|`LTraceLevel0`|<span data-ttu-id="c87c3-108">Le message est un niveau de trace 0.</span><span class="sxs-lookup"><span data-stu-id="c87c3-108">The message is a trace level 0.</span></span>|  
|`LTraceLevel1`|<span data-ttu-id="c87c3-109">Le message est un niveau de trace 1.</span><span class="sxs-lookup"><span data-stu-id="c87c3-109">The message is a trace level 1.</span></span>|  
|`LTraceLevel2`|<span data-ttu-id="c87c3-110">Le message est un niveau de trace 2.</span><span class="sxs-lookup"><span data-stu-id="c87c3-110">The message is a trace level 2.</span></span>|  
|`LTraceLevel3`|<span data-ttu-id="c87c3-111">Le message est un niveau de trace 3.</span><span class="sxs-lookup"><span data-stu-id="c87c3-111">The message is a trace level 3.</span></span>|  
|`LTraceLevel4`|<span data-ttu-id="c87c3-112">Le message est un niveau de trace 4.</span><span class="sxs-lookup"><span data-stu-id="c87c3-112">The message is a trace level 4.</span></span>|  
|`LStatusLevel0`|<span data-ttu-id="c87c3-113">Le message est un niveau d’état 0.</span><span class="sxs-lookup"><span data-stu-id="c87c3-113">The message is a status level 0.</span></span>|  
|`LStatusLevel1`|<span data-ttu-id="c87c3-114">Le message est un niveau de l’état 1.</span><span class="sxs-lookup"><span data-stu-id="c87c3-114">The message is a status level 1.</span></span>|  
|`LStatusLevel2`|<span data-ttu-id="c87c3-115">Le message est un niveau de l’état 2.</span><span class="sxs-lookup"><span data-stu-id="c87c3-115">The message is a status level 2.</span></span>|  
|`LStatusLevel3`|<span data-ttu-id="c87c3-116">Le message est un niveau d’état 3.</span><span class="sxs-lookup"><span data-stu-id="c87c3-116">The message is a status level 3.</span></span>|  
|`LStatusLevel4`|<span data-ttu-id="c87c3-117">Le message est un niveau de l’état 4.</span><span class="sxs-lookup"><span data-stu-id="c87c3-117">The message is a status level 4.</span></span>|  
|`LWarningLevel`|<span data-ttu-id="c87c3-118">Le message est un niveau d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="c87c3-118">The message is a warning level.</span></span>|  
|`LErrorLevel`|<span data-ttu-id="c87c3-119">Le message est un niveau d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c87c3-119">The message is an error level.</span></span>|  
|`LPanicLevel`|<span data-ttu-id="c87c3-120">Le message est un niveau de panique.</span><span class="sxs-lookup"><span data-stu-id="c87c3-120">The message is a panic level.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c87c3-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c87c3-121">Remarks</span></span>  
 <span data-ttu-id="c87c3-122">Le common language runtime (CLR) appelle le [ICorDebugManagedCallback::LogMessage](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-logmessage-method.md) méthode pour informer le débogueur qu’un thread managé a enregistré un événement.</span><span class="sxs-lookup"><span data-stu-id="c87c3-122">The common language runtime (CLR) calls the [ICorDebugManagedCallback::LogMessage](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-logmessage-method.md) method to notify the debugger that a managed thread has logged an event.</span></span> <span data-ttu-id="c87c3-123">Le CLR passe une valeur de la `LoggingLevelEnum` énumération pour indiquer le niveau de gravité du message que le thread managé a écrit dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="c87c3-123">The CLR passes a value of the `LoggingLevelEnum` enumeration to indicate the severity level of the message that the managed thread wrote to the event log.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c87c3-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c87c3-124">Requirements</span></span>  
 <span data-ttu-id="c87c3-125">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c87c3-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c87c3-126">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c87c3-126">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c87c3-127">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c87c3-127">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c87c3-128">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c87c3-128">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c87c3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c87c3-129">See also</span></span>

- <xref:System.Diagnostics.EventLog>
- [<span data-ttu-id="c87c3-130">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="c87c3-130">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
