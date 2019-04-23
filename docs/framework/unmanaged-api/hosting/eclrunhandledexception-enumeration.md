---
title: EClrUnhandledException, énumération
ms.date: 03/30/2017
api_name:
- EClrUnhandledException
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EClrUnhandledException
helpviewer_keywords:
- EClrUnhandledException enumeration [.NET Framework hosting]
ms.assetid: d231044e-2b53-4836-93f9-8117ff0e5c3a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7e5fb3ab1d2dedb220fd4a486409512414233021
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59176668"
---
# <a name="eclrunhandledexception-enumeration"></a><span data-ttu-id="5ec5a-102">EClrUnhandledException, énumération</span><span class="sxs-lookup"><span data-stu-id="5ec5a-102">EClrUnhandledException Enumeration</span></span>
<span data-ttu-id="5ec5a-103">Décrit les options disponibles pour la gestion des exceptions qui ne sont pas gérées dans le code utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5ec5a-103">Describes the available options for managing exceptions that are unhandled in user code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5ec5a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ec5a-104">Syntax</span></span>  
  
```  
typedef enum {  
    eRuntimeDeterminedPolicy,  
    eHostDeterminedPolicy  
} EClrUnhandledException;  
```  
  
## <a name="members"></a><span data-ttu-id="5ec5a-105">Membres</span><span class="sxs-lookup"><span data-stu-id="5ec5a-105">Members</span></span>  
  
|<span data-ttu-id="5ec5a-106">Membre</span><span class="sxs-lookup"><span data-stu-id="5ec5a-106">Member</span></span>|<span data-ttu-id="5ec5a-107">Description</span><span class="sxs-lookup"><span data-stu-id="5ec5a-107">Description</span></span>|  
|------------|-----------------|  
|`eRuntimeDeterminedPolicy`|<span data-ttu-id="5ec5a-108">Spécifie que le comportement par défaut se produit.</span><span class="sxs-lookup"><span data-stu-id="5ec5a-108">Specifies that the default behavior occurs.</span></span> <span data-ttu-id="5ec5a-109">Le processus est détruit.</span><span class="sxs-lookup"><span data-stu-id="5ec5a-109">The process is torn down.</span></span>|  
|`eHostDeterminedPolicy`|<span data-ttu-id="5ec5a-110">Spécifie que le common language runtime (CLR) ignore les exceptions non gérées et permet à l’hôte de déterminer toute action supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="5ec5a-110">Specifies that the common language runtime (CLR) ignores unhandled exceptions and lets the host determine any further action.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5ec5a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5ec5a-111">Remarks</span></span>  
 <span data-ttu-id="5ec5a-112">Pour spécifier que le CLR se comportent comme les versions antérieures, utilisez le `eHostDeterminedPolicy` membre.</span><span class="sxs-lookup"><span data-stu-id="5ec5a-112">To specify that the CLR behave like earlier versions, use the `eHostDeterminedPolicy` member.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5ec5a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ec5a-113">Requirements</span></span>  
 <span data-ttu-id="5ec5a-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5ec5a-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5ec5a-115">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="5ec5a-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5ec5a-116">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5ec5a-116">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5ec5a-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5ec5a-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5ec5a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ec5a-118">See also</span></span>

- [<span data-ttu-id="5ec5a-119">EClrFailure, énumération</span><span class="sxs-lookup"><span data-stu-id="5ec5a-119">EClrFailure Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md)
- [<span data-ttu-id="5ec5a-120">EClrOperation, énumération</span><span class="sxs-lookup"><span data-stu-id="5ec5a-120">EClrOperation Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md)
- [<span data-ttu-id="5ec5a-121">ICLRPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="5ec5a-121">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)
- [<span data-ttu-id="5ec5a-122">SetUnhandledExceptionPolicy, méthode</span><span class="sxs-lookup"><span data-stu-id="5ec5a-122">SetUnhandledExceptionPolicy Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setunhandledexceptionpolicy-method.md)
- [<span data-ttu-id="5ec5a-123">IHostPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="5ec5a-123">IHostPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostpolicymanager-interface.md)
- [<span data-ttu-id="5ec5a-124">Énumérations d’hébergement</span><span class="sxs-lookup"><span data-stu-id="5ec5a-124">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
