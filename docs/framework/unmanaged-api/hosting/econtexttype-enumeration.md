---
title: EContextType, énumération
ms.date: 03/30/2017
api_name:
- EContextType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EContextType
helpviewer_keywords:
- EContextType enumeration [.NET Framework hosting]
ms.assetid: 92b926a9-b87e-408a-9036-df7b752c9492
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7a261d9164e8714531eab1fe9fc8148304e6d5bb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33432880"
---
# <a name="econtexttype-enumeration"></a><span data-ttu-id="4001f-102">EContextType, énumération</span><span class="sxs-lookup"><span data-stu-id="4001f-102">EContextType Enumeration</span></span>
<span data-ttu-id="4001f-103">Décrit le contexte de sécurité du thread en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4001f-103">Describes the security context of the currently executing thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4001f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4001f-104">Syntax</span></span>  
  
```  
typedef enum {  
    eCurrentContext    = 0x00,  
    eRestrictedContext = 0x01  
} EContextType;  
```  
  
## <a name="members"></a><span data-ttu-id="4001f-105">Membres</span><span class="sxs-lookup"><span data-stu-id="4001f-105">Members</span></span>  
  
|<span data-ttu-id="4001f-106">Membre</span><span class="sxs-lookup"><span data-stu-id="4001f-106">Member</span></span>|<span data-ttu-id="4001f-107">Description</span><span class="sxs-lookup"><span data-stu-id="4001f-107">Description</span></span>|  
|------------|-----------------|  
|`eCurrentContext`|<span data-ttu-id="4001f-108">Indique le contexte du thread actuel au moment où le common language runtime (CLR) appelle la [IHostSecurityManager::GetSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-getsecuritycontext-method.md) (méthode), ou le contexte demandé par le CLR dans un appel à la [ IHostSecurityManager::SetSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-setsecuritycontext-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="4001f-108">Indicates the context on the current thread at the time the common language runtime (CLR) calls the [IHostSecurityManager::GetSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-getsecuritycontext-method.md) method, or the context requested by the CLR in a call to the [IHostSecurityManager::SetSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-setsecuritycontext-method.md) method.</span></span>|  
|`eRestrictedContext`|<span data-ttu-id="4001f-109">Indique un contexte sur lequel l’ordinateur hôte possède des privilèges inférieurs, tels que le garbage collector, ou les constructeurs de classe ou module.</span><span class="sxs-lookup"><span data-stu-id="4001f-109">Indicates a context over which the host has lower privileges, such as the garbage collector, or class or module constructors.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4001f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4001f-110">Remarks</span></span>  
 <span data-ttu-id="4001f-111">Le CLR fournit l’une de le `EContextType` valeurs comme valeur de paramètre dans les appels à la `IHostSecurityManager::GetSecurityContext` et `IHostSecurityManager::SetSecurityContext` méthodes.</span><span class="sxs-lookup"><span data-stu-id="4001f-111">The CLR supplies one of the `EContextType` values as a parameter value in calls to the `IHostSecurityManager::GetSecurityContext` and `IHostSecurityManager::SetSecurityContext` methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4001f-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4001f-112">Requirements</span></span>  
 <span data-ttu-id="4001f-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4001f-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4001f-114">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="4001f-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="4001f-115">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4001f-115">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4001f-116">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4001f-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4001f-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4001f-117">See Also</span></span>  
 [<span data-ttu-id="4001f-118">IHostSecurityContext, interface</span><span class="sxs-lookup"><span data-stu-id="4001f-118">IHostSecurityContext Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md)  
 [<span data-ttu-id="4001f-119">IHostSecurityManager, interface</span><span class="sxs-lookup"><span data-stu-id="4001f-119">IHostSecurityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-interface.md)  
 [<span data-ttu-id="4001f-120">Énumérations d’hébergement</span><span class="sxs-lookup"><span data-stu-id="4001f-120">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
