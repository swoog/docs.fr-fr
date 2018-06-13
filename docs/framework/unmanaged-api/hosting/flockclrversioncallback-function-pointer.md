---
title: FLockClrVersionCallback (pointeur fonction)
ms.date: 03/30/2017
api_name:
- FLockClrVersionCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- FLockClrVersionCallback
helpviewer_keywords:
- FLockClrVersionCallback function pointer [.NET Framework hosting]
ms.assetid: 98a4762d-9ad2-45bd-9d03-39064a028b44
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5c884d07fa35c053b1a3b65c04426ac0e3712621
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429671"
---
# <a name="flockclrversioncallback-function-pointer"></a><span data-ttu-id="7cc4c-102">FLockClrVersionCallback (pointeur fonction)</span><span class="sxs-lookup"><span data-stu-id="7cc4c-102">FLockClrVersionCallback Function Pointer</span></span>
<span data-ttu-id="7cc4c-103">Pointe vers une fonction que le common language runtime (CLR) appelle pour indiquer que l’initialisation a démarré ou s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="7cc4c-103">Points to a function that the common language runtime (CLR) calls to indicate that initialization has either started or completed.</span></span>  
  
 <span data-ttu-id="7cc4c-104">Ce pointeur de fonction a été déconseillé dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="7cc4c-104">This function pointer has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7cc4c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cc4c-105">Syntax</span></span>  
  
```  
typedef HRESULT (__stdcall *FLockClrVersionCallback) ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="7cc4c-106">Notes</span><span class="sxs-lookup"><span data-stu-id="7cc4c-106">Remarks</span></span>  
 <span data-ttu-id="7cc4c-107">Cette fonction est implémentée par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="7cc4c-107">This function is implemented by the host.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7cc4c-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7cc4c-108">Requirements</span></span>  
 <span data-ttu-id="7cc4c-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7cc4c-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7cc4c-110">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="7cc4c-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="7cc4c-111">**Bibliothèque :** MSCorWks.dll</span><span class="sxs-lookup"><span data-stu-id="7cc4c-111">**Library:** MSCorWks.dll</span></span>  
  
 <span data-ttu-id="7cc4c-112">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7cc4c-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7cc4c-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cc4c-113">See Also</span></span>  
 [<span data-ttu-id="7cc4c-114">LockClrVersion, fonction</span><span class="sxs-lookup"><span data-stu-id="7cc4c-114">LockClrVersion Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/lockclrversion-function.md)  
 [<span data-ttu-id="7cc4c-115">Fonctions d’hébergement CLR dépréciées</span><span class="sxs-lookup"><span data-stu-id="7cc4c-115">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
