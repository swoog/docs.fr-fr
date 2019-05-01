---
title: Structure CoreClrDebugRuntimeInfo
ms.date: 03/30/2017
api_name:
- CoreClrDebugRuntimeInfo
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- CoreClrDebugRuntimeInfo
helpviewer_keywords:
- remote debugging API [Silverlight]
- CoreDebugRuntimeInfo structure
- Silverlight, remote debugging
ms.assetid: bd01c30f-b7a8-4179-9497-622b6599b1a6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 88fcc5959054f1cdf7c9543674584a4bde26d896
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61966040"
---
# <a name="coreclrdebugruntimeinfo-structure"></a><span data-ttu-id="0cb31-102">Structure CoreClrDebugRuntimeInfo</span><span class="sxs-lookup"><span data-stu-id="0cb31-102">CoreClrDebugRuntimeInfo Structure</span></span>
<span data-ttu-id="0cb31-103">Représente une instance du Common Language Runtime (CLR) qui est chargée dans un processus sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="0cb31-103">Represents a common language runtime (CLR) instance that is loaded in a process on a remote machine.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0cb31-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cb31-104">Syntax</span></span>  
  
```  
struct  CoreClrDebugRuntimeInfo {  
    DWORD m_dwInternalID;  
};  
```  
  
## <a name="members"></a><span data-ttu-id="0cb31-105">Membres</span><span class="sxs-lookup"><span data-stu-id="0cb31-105">Members</span></span>  
  
|<span data-ttu-id="0cb31-106">Membre</span><span class="sxs-lookup"><span data-stu-id="0cb31-106">Member</span></span>|<span data-ttu-id="0cb31-107">Description</span><span class="sxs-lookup"><span data-stu-id="0cb31-107">Description</span></span>|  
|------------|-----------------|  
|`m_dwInternalID`|<span data-ttu-id="0cb31-108">Identificateur de runtime affecté par le proxy de débogage distant en cours d'exécution sur l'ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="0cb31-108">Runtime identifier that is assigned by the remote debugging proxy running on the target machine.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0cb31-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cb31-109">Requirements</span></span>  
 <span data-ttu-id="0cb31-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0cb31-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0cb31-111">**En-tête :** CoreClrRemoteDebuggingInterfaces.h</span><span class="sxs-lookup"><span data-stu-id="0cb31-111">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="0cb31-112">**Bibliothèque :** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="0cb31-112">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="0cb31-113">**Versions du .NET framework :** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="0cb31-113">**.NET Framework Versions:** 3.5 SP1</span></span>
