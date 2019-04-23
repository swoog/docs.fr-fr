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
ms.openlocfilehash: 8062ab151efc6175aa68cb0563cd2ad042ee9cd8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59189051"
---
# <a name="flockclrversioncallback-function-pointer"></a><span data-ttu-id="fe9df-102">FLockClrVersionCallback (pointeur fonction)</span><span class="sxs-lookup"><span data-stu-id="fe9df-102">FLockClrVersionCallback Function Pointer</span></span>
<span data-ttu-id="fe9df-103">Pointe vers une fonction que le common language runtime (CLR) appelle pour indiquer que l’initialisation a démarré ou terminé.</span><span class="sxs-lookup"><span data-stu-id="fe9df-103">Points to a function that the common language runtime (CLR) calls to indicate that initialization has either started or completed.</span></span>  
  
 <span data-ttu-id="fe9df-104">Ce pointeur de fonction a été déconseillé dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="fe9df-104">This function pointer has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe9df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe9df-105">Syntax</span></span>  
  
```  
typedef HRESULT (__stdcall *FLockClrVersionCallback) ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="fe9df-106">Notes</span><span class="sxs-lookup"><span data-stu-id="fe9df-106">Remarks</span></span>  
 <span data-ttu-id="fe9df-107">Cette fonction est implémentée par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fe9df-107">This function is implemented by the host.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe9df-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe9df-108">Requirements</span></span>  
 <span data-ttu-id="fe9df-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fe9df-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fe9df-110">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="fe9df-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fe9df-111">**Bibliothèque :** MSCorWks.dll</span><span class="sxs-lookup"><span data-stu-id="fe9df-111">**Library:** MSCorWks.dll</span></span>  
  
 <span data-ttu-id="fe9df-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fe9df-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe9df-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe9df-113">See also</span></span>

- [<span data-ttu-id="fe9df-114">LockClrVersion, fonction</span><span class="sxs-lookup"><span data-stu-id="fe9df-114">LockClrVersion Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/lockclrversion-function.md)
- [<span data-ttu-id="fe9df-115">Fonctions d’hébergement CLR dépréciées</span><span class="sxs-lookup"><span data-stu-id="fe9df-115">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
