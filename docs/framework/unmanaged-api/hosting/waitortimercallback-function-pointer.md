---
title: WAITORTIMERCALLBACK (pointeur fonction)
ms.date: 03/30/2017
api_name:
- WAITORTIMERCALLBACK
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- WAITORTIMERCALLBACK
helpviewer_keywords:
- WAITORTIMERCALLBACK function pointer [.NET Framework hosting]
ms.assetid: 1fec4aef-0a06-4df0-bae7-d31a9ef9603d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f8cf12fc6828c5e439a6a86532f22b8a598a9f03
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59120989"
---
# <a name="waitortimercallback-function-pointer"></a><span data-ttu-id="2b27d-102">WAITORTIMERCALLBACK (pointeur fonction)</span><span class="sxs-lookup"><span data-stu-id="2b27d-102">WAITORTIMERCALLBACK Function Pointer</span></span>
<span data-ttu-id="2b27d-103">Pointe vers une fonction qui avertit l’hôte qu’un handle d’attente (<xref:System.Threading.WaitHandle>) a été signalé ou a expiré.</span><span class="sxs-lookup"><span data-stu-id="2b27d-103">Points to a function that notifies the host that a wait handle (<xref:System.Threading.WaitHandle>) has either been signaled or timed out.</span></span>  
  
 <span data-ttu-id="2b27d-104">Ce pointeur de fonction a été déconseillé dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="2b27d-104">This function pointer has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b27d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b27d-105">Syntax</span></span>  
  
```  
typedef VOID (__stdcall *WAITORTIMERCALLBACK) (  
    [in] PVOID lpParameter,  
    [in] BOOL  TimerOrWaitFired  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2b27d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b27d-106">Parameters</span></span>  
 `lpParameter`  
 <span data-ttu-id="2b27d-107">[in] Pointeur vers un objet qui contient les informations définies par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="2b27d-107">[in] A pointer to an object that contains information defined by the host.</span></span>  
  
 `TimerOrWaitFired`  
 <span data-ttu-id="2b27d-108">[in] `true` si le handle d’attente a expiré, ou `false` si elle a été signalée.</span><span class="sxs-lookup"><span data-stu-id="2b27d-108">[in] `true` if the wait handle timed out, or `false` if it was signaled.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2b27d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="2b27d-109">Remarks</span></span>  
 <span data-ttu-id="2b27d-110">La fonction à laquelle `WAITORTIMERCALLBACK` points est une fonction de rappel et doit être implémentée par le writer de l’application d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="2b27d-110">The function to which `WAITORTIMERCALLBACK` points is a callback function and must be implemented by the writer of the hosting application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2b27d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b27d-111">Requirements</span></span>  
 <span data-ttu-id="2b27d-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2b27d-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2b27d-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="2b27d-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2b27d-114">**Bibliothèque :** MSCorWks.dll</span><span class="sxs-lookup"><span data-stu-id="2b27d-114">**Library:** MSCorWks.dll</span></span>  
  
 **<span data-ttu-id="2b27d-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="2b27d-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="2b27d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b27d-116">See also</span></span>

- [<span data-ttu-id="2b27d-117">Fonction d'hébergement du CLR déconseillées</span><span class="sxs-lookup"><span data-stu-id="2b27d-117">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
