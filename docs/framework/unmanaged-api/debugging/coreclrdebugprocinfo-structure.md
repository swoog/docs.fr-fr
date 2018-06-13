---
title: Structure CoreClrDebugProcInfo
ms.date: 03/30/2017
api_name:
- CoreClrDebugProcInfo
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- CoreClrDebugProcInfo
helpviewer_keywords:
- remote debugging API [Silverlight]
- CoreClrDebugProcInfo structure
- Silverlight, remote debugging
ms.assetid: 4ddc37da-5c94-4beb-b61c-b54071c0e749
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b9d4b27ca0bf454b42f15b849008e5a3019bb09a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402189"
---
# <a name="coreclrdebugprocinfo-structure"></a><span data-ttu-id="19373-102">Structure CoreClrDebugProcInfo</span><span class="sxs-lookup"><span data-stu-id="19373-102">CoreClrDebugProcInfo Structure</span></span>
<span data-ttu-id="19373-103">Représente un processus qui s'exécute sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="19373-103">Represents a process that is running on a remote machine.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19373-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19373-104">Syntax</span></span>  
  
```  
struct  CoreClrDebugProcInfo {  
    DWORD m_dwPID;  
    DWORD m_dwInternalID;  
    WCHAR m_wszName[256];  
};  
```  
  
## <a name="members"></a><span data-ttu-id="19373-105">Membres</span><span class="sxs-lookup"><span data-stu-id="19373-105">Members</span></span>  
  
|<span data-ttu-id="19373-106">Membre</span><span class="sxs-lookup"><span data-stu-id="19373-106">Member</span></span>|<span data-ttu-id="19373-107">Description</span><span class="sxs-lookup"><span data-stu-id="19373-107">Description</span></span>|  
|------------|-----------------|  
|`m_dwPID`|<span data-ttu-id="19373-108">Identificateur de processus affecté par le système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="19373-108">OS-assigned process identifier.</span></span>|  
|`m_dwInternalID`|<span data-ttu-id="19373-109">Identificateur de processus affecté par le proxy de débogage distant en cours d'exécution sur l'ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="19373-109">Process identifier that is assigned by the remote debugging proxy running on the target machine.</span></span> <span data-ttu-id="19373-110">Cet identificateur est moins souvent recyclé que l'identificateur de système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="19373-110">This identifier recycles less often than the OS identifier.</span></span>|  
|`m_wszName`|<span data-ttu-id="19373-111">Ligne de commande du processus.</span><span class="sxs-lookup"><span data-stu-id="19373-111">Command-line of the process.</span></span> <span data-ttu-id="19373-112">Ce membre peut être tronqué.</span><span class="sxs-lookup"><span data-stu-id="19373-112">This member may be truncated.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="19373-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="19373-113">Requirements</span></span>  
 <span data-ttu-id="19373-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="19373-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="19373-115">**En-tête :** CoreClrRemoteDebuggingInterfaces.h</span><span class="sxs-lookup"><span data-stu-id="19373-115">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="19373-116">**Bibliothèque :** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="19373-116">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="19373-117">**Versions du .NET framework :** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="19373-117">**.NET Framework Versions:** 3.5 SP1</span></span>
