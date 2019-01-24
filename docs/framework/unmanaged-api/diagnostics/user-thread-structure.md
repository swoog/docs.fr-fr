---
title: USER_THREAD, structure
ms.date: 03/30/2017
api_name:
- USER_THREAD
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- USER_THREAD
helpviewer_keywords:
- USER_THREAD structure [.NET Framework debugging]
ms.assetid: a57c7d71-c4b0-41f9-a964-0c5ee84a3124
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: acc4da79796e975d349d1cb33c301c25c4791cb6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54709076"
---
# <a name="userthread-structure"></a><span data-ttu-id="26d5b-102">USER_THREAD, structure</span><span class="sxs-lookup"><span data-stu-id="26d5b-102">USER_THREAD Structure</span></span>
<span data-ttu-id="26d5b-103">Fournit des informations à un débogueur sur un thread.</span><span class="sxs-lookup"><span data-stu-id="26d5b-103">Provides information to a debugger about a thread.</span></span> <span data-ttu-id="26d5b-104">Pour plus d’informations, consultez le [INotifySource2::SetNotifyFilter](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-setnotifyfilter-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="26d5b-104">For more information, see the [INotifySource2::SetNotifyFilter](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-setnotifyfilter-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26d5b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26d5b-105">Syntax</span></span>  
  
```  
typedef struct tagUSER_THREAD  
{  
    BYTE    *pSidBuffer;  
    DWORD   dwSidLen;  
    DWORD   dwTid;  
} USER_THREAD;  
```  
  
## <a name="members"></a><span data-ttu-id="26d5b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="26d5b-106">Members</span></span>  
  
|<span data-ttu-id="26d5b-107">Membre</span><span class="sxs-lookup"><span data-stu-id="26d5b-107">Member</span></span>|<span data-ttu-id="26d5b-108">Description</span><span class="sxs-lookup"><span data-stu-id="26d5b-108">Description</span></span>|  
|------------|-----------------|  
|`pSidBuffer`|<span data-ttu-id="26d5b-109">Adresse de mémoire tampon de thread.</span><span class="sxs-lookup"><span data-stu-id="26d5b-109">Address of thread buffer.</span></span>|  
|`dwSidLen`|<span data-ttu-id="26d5b-110">Longueur de la mémoire tampon de thread, en octets.</span><span class="sxs-lookup"><span data-stu-id="26d5b-110">Length of thread buffer, in bytes.</span></span>|  
|`dwTid`|<span data-ttu-id="26d5b-111">ID de thread.</span><span class="sxs-lookup"><span data-stu-id="26d5b-111">Thread ID.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="26d5b-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="26d5b-112">Requirements</span></span>  
 <span data-ttu-id="26d5b-113">**En-tête :** ProtocolNotify2.idl</span><span class="sxs-lookup"><span data-stu-id="26d5b-113">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26d5b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26d5b-114">See also</span></span>
- [<span data-ttu-id="26d5b-115">SetNotifyFilter, méthode</span><span class="sxs-lookup"><span data-stu-id="26d5b-115">SetNotifyFilter Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-setnotifyfilter-method.md)
- [<span data-ttu-id="26d5b-116">Structures du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="26d5b-116">Diagnostics Symbol Store Structures</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-structures.md)
