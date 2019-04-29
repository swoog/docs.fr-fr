---
title: LPTHREAD_START_ROUTINE (pointeur fonction)
ms.date: 03/30/2017
api_name:
- LPTHREAD_START_ROUTINE
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- LPTHREAD_START_ROUTINE
helpviewer_keywords:
- LPTHREAD_START_ROUTINE function pointer [.NET Framework hosting]
ms.assetid: 7b9b93b0-fe92-42ba-8693-701168a29dde
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 27d1837f9f9f11ad34140f50ec41aa6fe8a62160
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61765243"
---
# <a name="lpthreadstartroutine-function-pointer"></a><span data-ttu-id="11919-102">LPTHREAD_START_ROUTINE (pointeur fonction)</span><span class="sxs-lookup"><span data-stu-id="11919-102">LPTHREAD_START_ROUTINE Function Pointer</span></span>
<span data-ttu-id="11919-103">Pointe vers une fonction qui avertit l’hôte qu’un thread a commencé à exécuter.</span><span class="sxs-lookup"><span data-stu-id="11919-103">Points to a function that notifies the host that a thread has started to execute.</span></span>  
  
 <span data-ttu-id="11919-104">Ce pointeur de fonction a été déconseillé dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="11919-104">This function pointer has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="11919-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11919-105">Syntax</span></span>  
  
```  
typedef DWORD (__stdcall *LPTHREAD_START_ROUTINE) (  
    [in] LPVOID lpThreadParameter  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="11919-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11919-106">Parameters</span></span>  
 `lpThreadParameter`  
 <span data-ttu-id="11919-107">[in] Pointeur vers le code qui a démarré l’exécution.</span><span class="sxs-lookup"><span data-stu-id="11919-107">[in] A pointer to the code that has started executing.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="11919-108">Notes</span><span class="sxs-lookup"><span data-stu-id="11919-108">Remarks</span></span>  
 <span data-ttu-id="11919-109">La fonction à laquelle `LPTHREAD_START_ROUTINE` points est une fonction de rappel et doit être implémentée par le writer de l’application d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="11919-109">The function to which `LPTHREAD_START_ROUTINE` points is a callback function and must be implemented by the writer of the hosting application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="11919-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11919-110">Requirements</span></span>  
 <span data-ttu-id="11919-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="11919-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="11919-112">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="11919-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="11919-113">**Bibliothèque :** MSCorWks.dll</span><span class="sxs-lookup"><span data-stu-id="11919-113">**Library:** MSCorWks.dll</span></span>  
  
 <span data-ttu-id="11919-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="11919-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="11919-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11919-115">See also</span></span>

- [<span data-ttu-id="11919-116">Fonctions d’hébergement CLR dépréciées</span><span class="sxs-lookup"><span data-stu-id="11919-116">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
